# WRITING TEST WEEK 6

24 Oktober 2022 - 28 Oktober 2022
***

## React.js Basic - Javascript for React.js | Intro to React.js, Virtual DOM & JSX

React.js merupakan sebuah library javascript yang dapat digunakan untuk membantu pembuatan website dari sisi front-end, React.js dibuat dan dikembangkan oleh Facebook.

> React.js berbasis virtual DOM dan setiap element yang dibuat dengan React.js disebut react component.
> React.js memiliki ekstensi file ".jsx" untuk javascript dan ".tsx" untuk typescript.

### Instalasi React

Ada beberapa cara untuk menggunakan atau menginstalasi React dalam project kita. Menurut saya yang paling mudah adalah dengan menggunakan template yang telah dicustom oleh React yaitu create-react-app atau CRA.

>Berikut langkah - langkah menginstall React dengan CRA. Pastikan kita telah menginstall Node.js di device kita. 
>> Pertama buka terminal
>> masuk ke root folder
>> ketik npx create-react-app my-app, tunggu proses selesai
>> buka folder pada visual studio code atau code editor lain.

***

## React.js Basic- Functional Component | Props & State | Styling

### React Component

>React Component adalah sebuah *function* atau *class* yang mengembalikan kode jsx. React Component memungkinkan kita untuk memisahkan kode jsx menjadi beberapa bagian yang lebih kecil. Di React component kita bisa membuat komponen - komponen yang dapat digunakan kembali.

Untuk membuat React component, kita bisa menggunakan *function* atau *class*. Berikut adalah contoh penggunaan fungsi dan kelas untuk membuat React component:

```js
    // function component
    import React from "react"

    const App = () => {
        return (
            <div>
                <h1>Hello from Function</h1>
            </div>
        )

    }

    // class component
    class App extends React.Component {
        render() {
            return(
                <div>
                    <h1>Hello from Class</h1>
                </div>
            )
        }
    }
```

### Props 

>Props adalah sebuah object yang berisi data yang akan digunakan oleh react component. Props memungkinkan kita untuk mengirimkan data dari react component ke react component lainnya. Dengan props kita bisa menggunakan react component berulang kali.

**Mengirim Props**
Untuk mengirimkan Props, kita bisa menggunakan atribut HTML. Berikut adalah contoh penggunaannya:

```js
    import React from "react";
    import App from "./App";

    const Main = () => {
        return (
            <div>
                <App title="Hello Props" />
            </div>
        )
    }

    export default Main;
```

***Menerima Props**
Untuk menerima Props, kita bisa menggunakan parameter function atau parameter class. Berikut contoh penggunaannya:

```js
    import React from "react";

    const App = (props) => {
        return(
            <div>
                <h1>{props.title}</h1>
            </div>
        )
    }

    export default App;
```

### State

>State adalah sebuah object yang berisi data yang akan digunakan oleh React component. State memungkinkan kita untuk bisa membuat react component yang lebih dinamis dan interaktif.

**Membuat State**
Untuk membuat state, kita bisa menggunakan fungsi `useState()`. Fungsi `useState()` membutuhkan satu parameter, yaitu nilai awal dari state. Berikut contoh penggunaannya:

```js
    import React, {useState} from "react";

    const App = () => {
        const [count, setCount] = useState(0);

        return(
            <div>
                <h1>{count}</h1>
            </div>
        )
    }

    export default App;
```

## React.js Lanjutan - Lifecycle Method | Hooks

### React Lifecycle

- Lifecycle di dalam react memiliki tiga alur utama
- *Mount*, adalah sebuah siklus pertama ketika aplikasi dibuka
- *Update*, adalah sebuah siklus ketika terjadi perubahan data
- *Unmount*, adalah siklus setelah komponen dibuka
- Sebelum ada versi 16 atau adanya *Hooks* untuk memanipulasi lifecycle di dalam react harus menggunakan *componentDidMount()*, *componentWillUpdate()*, *componentWillUnMount()*
- Setelah adanya versi 16, kita dapat menggunakan *useEffect()* untuk menghandle lifecycle pada react.

### React Hooks

- *React hooks*, adalah fitur yang memungkinkan untuk menggunakan state dan fitur react lainnya tanpa menuliskan sebuah kelas. Hooks menggunakan konsep functional component.
- Untuk menggunakan hooks harus menggunakan react versi 16.8 atau diatasnya
- Ada beberapa hooks yang disediakan oleh react, berikut hooks yang paling populer dan sering digunakan
    - *useState()*, adalah hook yang digunakan untuk membuat dan memanipulasi sebuah state.
    - *useEffect()*, adalah hook yang digunakan untuk menghandle lifecycle.
    - *useRef()*, adalah hook untuk memanipulasi elemen DOM
    - *useContext()*, adalah hook untuk memanipulasi sebuah context API
- Cara menggunakan hooks yaitu kita meng-import terlebih dahulu dari react. Contohnya seperti berikut:

```js
    import {useState} from 'react';

    export default const Home = () => {
        const [name, setName] = useState('Brucel')

        return(
            <>
                <p>nama saya {name}</p>
            </>
        )
    }

    //expected result: nama saya Brucel
```

