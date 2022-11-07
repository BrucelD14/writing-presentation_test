# WRITING TEST WEEK 7

31 Oktober 2022 - 04 November 2022

## Prop Types

- prop types untuk mencegah kesalahan yang tidak diinginkan
- cara menggunakan prop types : 
  1. install prop types pada terminal
  2. ketik npm install prop-types pada terminal
  3. import prop-types di component

  ```jsx
    import PropTypes from "prop-types";
  ```

- jika ada kesalahan pada type data, maka prop-types akan memberitahu bahwa terjadi error di console
- type data string

```jsx
    StudentInfo.propTypes = {
    name: PropTypes.string,
};
```

- type data number

```jsx
    StudentInfo.propTypes = {
    age: PropTypes.number,
};
```

- type data any

```jsx
    StudentInfo.propTypes = {
    name: PropTypes.any.isRequired, //isRequired data harus ada
};
```

- memberikan opsi untuk type data

```jsx
    StudentInfo.propTypes = {
    age: PropTypes.oneOfType([PropTypes.string, PropTypes.number]), 
};
```

- type data array

```jsx
    StudentInfo.propTypes = {
    data: PropTypes.array, 
};
```

- mengecek value dari props

```jsx
    StudentInfo.propTypes = {
    data: PropTypes.arrayOf(PropTypes.number), 
};
```

- array dengan berbagai macam type data

```jsx
    StudentInfo.propTypes = {
    data: PropTypes.arrayOf(PropTypes.oneOfType[PropTypes.number, PropTypes.string]), 
};
```

- type data object

```jsx
    StudentInfo.propTypes = {
    info: PropTypes.shape({
    hobby: PropTypes.string,
    class: PropTypes.number,
  }), 
};
```

- mengecek nilai dan key dari object

```jsx
StudentInfo.propTypes = {
  info: PropTypes.exact({
    hobby: PropTypes.string,
    class: PropTypes.number,
  }).isRequired, 
};
```

## Router

- router : fungsi router untuk pindah2 halaman
- keunggulan router daripada tag a pada html adalah lebih cepat ketika berpindah halamn, tidak perlu refresh lama halaman
- React router banyak versinya tapi kita pakai yang versi 6
- cara menggunakan react router
  1. install react router didalam folder project

```jsx
    npm install reat-roter-dom
```

    1. import browser router di main.jsx

```jsx
    //main.jsx
    import { BrowserRouter } from "react-router-dom";
    ReactDOM.createRoot(document.getElementById("root")).render(
    <React.StrictMode>
    <BrowserRouter>
      <App />
    </BrowserRouter>
    </React.StrictMode>
    );
```
    1. import routes di app.jsx
```jsx
    //app.jsx
    import { Routes, Route, Link } from "react-router-dom";
    const App = () => {
    return (
    <>
    <nav>
        <Link to={"/"}>Home |</Link>  //Link seperti tag a pada html
        <Link to={"/about"}>About</Link>
    </nav>
      
    <Routes>
        <Route path="/" element={<HomePage />} />   //halaman pertama yang dimunculkan hanya diberi "/"
        <Route path="/detail/:id" element={<DetailPage />} />
    </Routes>
    </>
    );
    };

    export default App;       
```

## Redux

- Untuk mengatasi props drilling, bisa menggunakan state management seperti redux, context, jotai, zustand
- redux adalah sebuah third party untuk memanipulasi state management didalam react
- state management ini digunakan jika banyak komponen yang memerlukan 1 data yang sama
- Konsep redux : Akan membuat tempat terpusat, lalu ketika ada component yang membutuhkan tinggal ngambil dari tempat tersebut

 
### cara menggunakan React redux

1. Install redux : bisa menggunakan redux core, redux toolkit

```jsx
//ini menggunakan redux core
npm install redux
```

2. Install react redux
   
```jsx
npm install react-redux
```

3. install store
- Harus menyediakan storenya dahulu

```jsx
//index.js
import { createStore } from 'redux'
import keranjangReducer from '../reducer/keranjangReducer'

const store = createStore(keranjangReducer)

export default store
```

1. Buat reducer
```jsx
//KeranjangReducer.js
const initialState = {
  totalKeranjang: 0,
};
function keranjangReducer(state = initialState, action) {
  switch (action.type) {       //Action ; sebuah function yang memiliki objek property type. Action akan dikirim ke reducer
    default:state
    break;
  }
}

export default keranjangReducer;
```

5. Buat provider, menggunakan react redux di main jsx import provider

```jsx
//main.jsx
import { Provider } from 'react-redux'
```
```jsx
//main.jsx
import React from 'react'
import ReactDOM from 'react-dom/client'
import { Provider } from 'react-redux'
import App from './App'
import store from './redux/store'

ReactDOM.createRoot(document.getElementById('root')).render(
  // <React.StrictMode>
    <Provider store={store}>
      <App />
    </Provider>
  // </React.StrictMode>
)
```

6. Buat components
```
//Counter.jsx
//Keranjang.jsx
//ListProduct.jsx
//SummaryPembelian.jsx
```

7. useSelector
```jsx
import React from 'react'
import { useSelector } from 'react-redux'

function Keranjang() {
  const {totalKeranjang} = useSelector(state => state)

  // console.log(state)

  return (
    <div>
      <span>Keranjang</span>
      <span> {totalKeranjang}</span>
    </div>
  )
}

export default Keranjang
```

8. useDispatch
- Dispatch : mengirim action ke dalam reducer
```jsx
//Counter.jsx
import { useDispatch } from "react-redux";
```
### Combine Reducer
- Combine Reducer : agar bisa menampung banyak store
- karena createStore hanya bisa menampung 1 store
```jsx
//index.jsx
import { combineReducers, createStore } from "redux";
import counterReducer from "../reducer/counterReducer";
import todoReducer from "../reducer/todoReducer";

const allReducer = combineReducers({
  counter: counterReducer,
  todo: todoReducer
})

const store = createStore(allReducer);

export default store;
```