# WRITING TEST WEEK 3

03 Oktober 2022 - 07 Oktober 2022
***

## Javascript Intermediate - Array & Multidimensional Array

### Array

Salah satu cara untuk mengakses array adalah menggunakan perulangan (array), bisa menggunakan for, while atau do while. Berikut cara mengakses array menggunakan for loop.

```js
    let arr = [1, 2, 3, 4, 5];
    for (let i = 0; i < arr.length; i++) {
        console.log(arr[i]);
    }

    /* output
    1
    2
    3
    4
    5
    */
```

Ada juga beberapa built-in method yang bisa digunakan untuk mengakses array, berikut contohnya:

```js
    // forEach()
    let colors = ['blue', 'red', 'yellow', 'green'];

    colors.forEach(data => {
        console.log(data)
    });

    /* output
    blue
    red
    yellow
    green
    */
```

```js
    // map()
    let input = [100, 50, 60, 10]

    let output = input.map(item => {
        return item;
    })

    // output [100, 50, 60, 10]

```

### Array Multidimensional

Array multidimensi merupakan array biasa yang di dalamnya terdapat data array, atau biasa dibilang array di dalam array.

berikut contoh array multidimensi:

```js
    let inventory = [
        ["kaos polos", 21],
        ["jaket hoodie", 13],
        ["topi", 7]
    ];
```

## Javascript Intermediate - Object & Array of Object

Array of object merupakan data data object yang berada di dalam array, berikut contohnya:

```js
    const flowerGarden = [
        {
            name: "jasmine",
            color: "white"
        },
        {
            name: "rose",
            color: "red"
        },
        {
            name: "violet",
            color: "blue"
        }
    ];

    console.log(flowerGarden);
```

## Javascript Intermediate - Rekursif

Rekursif adalah function yang memanggil dirinya sendiri terus menerus sampai pada kondisi tertentu.

berikut struktur rekursif:

```js
    function rekursif(){
        // kode lainnya
        rekursif()
    }
```

dan contoh rekursif sebagai berikut:

```js
    function faktorial(n) {
        if(n == 1) {
            return 1;
        }else{
            return n * faktorial(n-1);
        }
    }

    console.log(faktorial(4));
```

## Javascript Intermediate - Modules

Module adalah sebuah cara bagi Javascript untuk mengisolasi kode dari suatu file ke dalam sebuah file terpisah, sehingga kode tersebut dapat digunakan berulang kali dengan cara di export dari suatu file dan di import ke file lainnya.

Untuk membuat module pada direktori lokal kita bisa menggunakan cara berikut:

```js
    <script type="module" src="index.js"></script>
```

contoh export dan import:

```js
    // export
    export let orang = {
    nama: "Thoriq",
    umur: 25,
    alamat: "Jl. Kemang Raya"
};

    //import dari user.js
    import {orang} from "./user.js";
```

## Javascript Intermediate - Asynchronous - Introduction

Asynchronous atau non-blocking adalah proses yang mengizinkan komputer kita untuk memproses perintah lain sambil menunggu suatu proses lain yang berlangsung.

Berikut contoh asynchronous menggunakan setTimeout();

```js
    setTimeout(() => {
    console.log("Cuci baju"); // proses asynchronous
    }, 1000);
    console.log("Menyapu");
    console.log("Mengepel");
    console.log("Memasak");

    // 1000 ms = 1 second

    // Output:
    // Menyapu
    // Mengepel
    // Memasak
    // Cuci baju 
```

## Javascript Intermediate - Asynchronous - Promise

contoh penggunaan promise:

```js
    const condition = true;

    let newPromise = new Promise((resolve, reject) => {
    if (condition) {
    // apa yang dilakukan jika promise 'fulfilled'
    resolve("Berhasil");
    } else {
    // apa yang dilakukan jika promise 'rejected'
    reject(new Error("Error Gagal"));
    }
    });

    newPromise.then((result) => {
    console.log(result); // Output: "Berhasil"
    });
```

## Javascript Intermediate - Web Storage

Ada beberapa cara untuk menyimpan data pengguna seperti pencarian, artikel berita, dan lain lain ke lokal (browser) menggunakan web storage seperti cookies, local storage dan session storage.

Cookies adalah data kecil yang dikirim dari situs web dan disimpan di komputer kita oleh web browser saat kita menjelajah. Disebut data kecil karena maksimum data yang dapat disimpan dalam cookies adalah 4096 bytes (4 KB).

Dengan memanfaatkan local storage dan session storage, kita dapat menyimpan data lebih besar yaitu 5MB per page tanpa mempengaruhi kinerja situs web. 

Untuk menyimpan data di local storage kita bisa menggunakan method setItem(), strukturnya seperti berikut:

```js
    localStorage.setItem('key', value);
```

kita juga bisa mengambil data yang kita simpan menggunakan method getItem(), seperti berikut:

```js
    localStorage.getItem('key');
```