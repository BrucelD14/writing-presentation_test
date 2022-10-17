# WRITING TEST WEEK 4

10 Oktober 2022 - 13 Oktober 2022
***

## Javascript Intermediate - Asynchronous - Fetch

Dalam javascript kita bisa mengirimkan network request dan juga bisa mengambil data dari server. Beberapa contoh network request yaitu: 

- Mengirimkan data dari sebuah form
- Mengambil data untuk ditampilkan dalam list/table
- Mendapatkan notifikasi

Untuk melakukan network request, javascript punya metode yaitu **fetch()**.

Terdapat dua cara untuk melakukan **fetch()** yaitu menggunakan *promise* atau *async/await*

Berikut contoh **fetch()** menggunakan *promise*:

```js
    fetch("https://jsonplaceholder.typicode.com/posts")
    .then(function (response) {
        return response.json();
    })
    .then(function (post) {
        console.log(post);
    })
```

contoh **fetch()** menggunakan *async/await*:

```js
    const tesFetchAsync = async () => {
        let response = await fetch("https://jsonplaceholder.typicode.com/posts");
        response = await response.json();
        console.log(response);
    };
    tesFetchAsync();
```

## Javascript Intermediate - Asynchronous - Async/Await

*Async/await* merupakan salah satu cara untuk menggunakan asynchronous pada javascript selain menggunakan *callback* dan *promise*.

Ada 2 kata kunci utama pada *async/await* yaitu:

- *async*, untuk mengubah synchronous menjadi asynchronous.
- *await*, menunda eksekusi hingga proses asynchronous selesai.

Sebuah *async* function bisa tidak berisi *await* sama sekali atau lebih dari satu *await*. Keyword *await* hanya bisa digunakan di dalam *async* function, jika digunakan  di luar *async* function makan akan terjadi error.

Berikut contoh penggunaan *async*:

```js
    // async menggunakan keyword function
    async function tesAsyncAwait() {
        return "FulFilled";
    }
    console.log(tesAsyncAwait());

    // async menggunakan arrow function
    const tesAsyncAwait = async () => {
        return "FulFilled";
    };
    console.log(tesAsyncAwait());

```

## Git & GitHub Lanjutan

