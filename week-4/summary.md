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

### Branch

Branch adalah sebuah cabang dari repository. Branch digunakan untuk mengembangkan fitur tanpa mengganggu branch utama. Branch juga digunakan untuk mengembangkan fitur baru secara bersamaan.

### Merge

Merge adalah sebuah proses untuk menggabungkan branch yang berbeda. Merge hanya dapat dilakukan jika branch yang akan digabungkan memiliki parent.

### Merge Conflict

Merge coflict adalah sebuah kondisi dimana branch yang akan digabungkan memiliki parent yang berbeda. Merge conflict bisa diatasi dengan cara menghapus kode yang tidak diperlukan.

### Pull Request

Pull request adalah sebuah proses untuk menggabungkan branch yang berbeda. Pull request dilakukan di github.

### Checkout 

git checkout adalah perintah untuk mengganti branch head yang ada pada git local.

***

## Responsive Web Design

Responsive web design adalah design web yang dapat menyesuaikan ukuran layar yang digunakan pada device yang digunakan oleh user. Responsive web design dapat dibuat menggunakan CSS.

### Media Query

Media query adalah sebuah kode CSS yang dapat menyesuaikan ukuran layar yang digunakan untuk membuat responsive web design.

### Mobile First

Mobile first adalah sebuah design web yang memprioritaskan penggunaan layar mobile.

### Desktop First

Desktop first adalah sebuah desain web yang memprioritaskan penggunaan layar dekstop.

### Breakpoint

Breakpoint adalah sebuah titik dimana media query akan berjalan.

Contoh penggunaan media query

```css
    @media (max-width: 600px) {
        body {
            background-color: lightcoral;
        }
    }
```

## Bootstrap 5

Bootstrap adalah sebuah framework CSS yang dapat digunakan untuk membuat responsive web design. Bootstrap dapat digunakan untuk membuat responsive web design.

### Grid System

Grid system adalah sebuah sistem grid yang dimiliki bootsrap yang terdiri dari 12 column, grid system dapat digunakan untuk membuat responsive web design.

Berikut starting template untuk menggunakan Boostrap 5:

```html
    <!doctype html>
    <html lang="en">
    <head>
        <!-- Required meta tags -->
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">

        <!-- Bootstrap CSS -->
        <link href="https://cdn.jsdelivr.net/npm/  bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">

        <title>Hello, world!</title>
    </head>
    <body>
        <h1>Hello, world!</h1>

        <!-- Optional JavaScript; choose one of the two! -->

        <!-- Option 1: Bootstrap Bundle with Popper -->
        <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM" crossorigin="anonymous"></script>

        <!-- Option 2: Separate Popper and Bootstrap JS -->
        <!--
        <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.2/dist/umd/popper.min.js" integrity="sha384-IQsoLXl5PILFhosVNubq5LC7Qb9DXgDA9i+tQ8Zj3iwWAwPtgFTxbJ8NT4GN1R8p" crossorigin="anonymous"></script>
        <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.min.js" integrity="sha384-cVKIPhGWiC2Al4u+LWgxfKTRIcfu0JTxR+EQDz/bgldoEyl4H0zUF0QKbrJ0EcQF" crossorigin="anonymous"></script>
        -->
    </body>
    </html>
```

Menggunakan Bootstrap dengan CDN:

```html
    <!-- css -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">

    <!-- js -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM" crossorigin="anonymous"></script>
```

Setelah file HTML kita dihubungkan dengan Bootstrap, maka kita menggunakan component apapun yang ada di Bootstrap. Untuk lengkapnya dapat dilihat pada link berikut [Bootstrap 5](https://getbootstrap.com/docs/5.0/getting-started/introduction/ "Bootstrap 5 Documentation").

