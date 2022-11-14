# WEEK 8 - Front End Bootcamp

## React Context

Kegunaan react context ini hampir sama dengan react redux yaitu menghindari props drilling dan sebagai state managemen. React context tidak perlu menginstall depedencies tambahan hanya memanfaatkan fitur yang dimiliki react. Secara arti componen context digunakan untuk mengglobalkan suatu data.

Jika react redux harus membuat file javascript untuk menggunakannya, react context hanya perlu membuat component context. Dimana component context ini akan memprovide keseluruhan component yang telah kita miliki.

Cara membuat provider pada component context adalah :

```jsx
import React, { createContext } from 'react'

function KeranjangCountProvider({children}) {

  return (
    <KeranjangCountContext.Provider>
      
    </KeranjangCountContext.Provider>
  )
}

export default KeranjangCountProvider
```

Selanjutnya component context ini akan membungkus App pada Main.jsx, component context ini akan menjadi parent dan childernnya adalam componen App. Selanjutnya komponen App ini akan dikirim sebagai props dan ditampilkan kembali pada componen context.

```jsx
import React, { createContext, useState } from 'react'

export const KeranjangCountContext = createContext()

function KeranjangCountProvider({children}) {
  const [keranjangCount, setKeranjangCount] = useState(0)

  return (
    <KeranjangCountContext.Provider value={{keranjangCount, setKeranjangCount}}>
      {children}
    </KeranjangCountContext.Provider>
  )
}

export default KeranjangCountProvider
```

Cara memanggil data untuk digunakan pada component lain yaitu menggunakan ***useContext***.

### useReducer

- context biasa untuk menglobalkan datanya, dengan bantuan reducer datanya bisa di manage
1. import useReducer
2. buat function reducer(state, action)
3. buat switch case 
4. panggil useReducer di dalam function counterprovider
5. buat action untuk mengubah state 
6. buat const increment, decrement


```jsx
//Counter1Provider.jsx
import React, { createContext, useReducer, useState } from "react";

export const CounterContext = createContext();

function Counte1Provider({ children }) {
  const [count, setCount] = useState(0)

  return (
    <CounterContext.Provider value={{ count, setCount }}>
      {children}
    </CounterContext.Provider>
  );
}

export default Counte1Provider;

//Counter2Provider.jsx
import React, { createContext, useReducer, useState } from "react";

export const CounterContext = createContext();

const INCREMENT = "INCREMENT";
const DECREMENT = "DECREMENT";

const initialState = {
  count: 0,
};

function reducer(state, action) {
  switch (action.type) {
    case INCREMENT:
      return { count: state.count + 1 };
    case DECREMENT:
      return { count: state.count - 1 };
    default:
      return state;
  }
}

function Counter2Provider({ children }) {
  const [state, dispatch] = useReducer(reducer, initialState);

  const increment = () => {
    dispatch({ type: INCREMENT });
  };

  const decrement = () => {
    dispatch({ type: DECREMENT });
  };

  return (
    <CounterContext.Provider value={{ state, increment, decrement }}>
      {children}
    </CounterContext.Provider>
  );
}

export default Counter2Provider;

```

```jsx

import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App";
import Counter2Provider from "./context/Counter2Provider";
import Counter1Provider from "./context/Counter1Provider";
import TodoProvider from "./context/TodoProvider";

ReactDOM.createRoot(document.getElementById("root")).render(
  // <React.StrictMode>
  <TodoProvider>
    <Counter2Provider>
      <Counter1Provider>
        <App />
      </Counter1Provider>
    </Counter2Provider>
  </TodoProvider>
  // </React.StrictMode>
);
```
## Testing

Tipe testing ada 2 :
1. Manual : saat kita mengecek source code kita seperti mengecek variabel, data dll.
2. Automation (otomatis) : testing yang dikerjakan oleh suatu code

Secara umum ada 3 bagian dalam automation testing, yaitu :
1. unit test : menguji kode yang paling kecil
2. integration : melakukan pengujian jika terhubung ke apk lain, c/o database
3. end to end : secara sisi user
- semakin ke atas biayanya semakin mahal, yang dibutuhkan juga semakin banyak

### Jest

---
Jest merupakan library dari javascript yang digunakan untuk proses testing. Sebelum kita menggunakan jest kita harus menginstallnya terlebih dahulu : 
> npm install --save-dev jest

- Membuat file dengan nama sum.test.js

Kita membuat ekspetasinya terlebih dahulu :
```js
const sum = require('./sum'); //import fungsi

test('adds 1 + 2 to equal 3', () => {
  expect(sum(1, 2)).toBe(3);
  expect(sum(1, 3)).toBe(4);
  expect(sum(2, 3)).toBe(5);
});
```

- Membuat file dengan nama sum.js
- Lalu membuat fungsi dan mengeksport fungsi yang akan di import pada code testingnya.
```js
function sum(a, b) {
  return a + b;
}
module.exports = sum;
```

### RTL (React Testing Library)

---
Didalam RTL ini sudah include dengan jest. Penggunaan rtl ini kurang lebih sama dengan jest, tetapi RTL sudah langsung dapat digunakan tanpa menginstall library lagi.

Contoh penggunaan pada counter.js, kita akan mengecek apakah ada button + dan - pada counter tersebut. 

- Pada Counter.js
  ```js
    import React, { useState } from 'react'

    function Counter() {
      const [count, setCount] = useState(0)

      return (
        <div>
          <button>-</button>
          <span>0</span>
          <button>+</button>
        </div>
      )
    }

    export default Counter
  ```

- Pada Counter.test.js
  ```js
    import { fireEvent, render, screen } from '@testing-library/react';
    import Counter from './Counter';

    test("render counter", () => {
      render(<Counter/>)
      const decrementBtn = screen.getByText("-")
      const incrementBtn = screen.getByText("+")

      expect(decrementBtn).toBeInTheDocument()
      expect(incrementBtn).toBeInTheDocument()
    })

  ```