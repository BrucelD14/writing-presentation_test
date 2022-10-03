# **WRITING TEST WEEK 02**

26 September 2022 - 30 September 2022

## **Javascript Dasar Scope**

Javascript scope yang berarti ruang lingkup dalam javascript,ada 2 jenis scope dalam javascript yaitu:

-   Local Scope yang berarti variable hanya bisa diakses
    dari dalam blocks,local scope ini tidak bisa dijangkau dari luar blocks nya

```js
    // dibagian ini variabel 'makanan' tidak dapat diakses

    function simpleFunction(){
    var makanan = "Nasi goreng";
    // jika variabel 'makanan' ditaruh di dalam sini maka variabel 'makanan' dapat diakses
    }
```

-   Gobal Scope yang berarti variable tersebut bisa diakses
    dimanapun,variable harus dideklarsaikan diluar bloks agar bisa diakses

```js
    var makanan = "Nasi goreng";
    // disini kamu bisa menggunakan variabel 'makanan'

    function simpleFunction() {
        // disini kamu bisa menggunakan variabel 'makanan'
    }
```

-   Blocks adalah code yang berada dalam tanda {
    conditional,function dan looping menggunakan blocks.

***

## **Javascript Dasar Function**

Function adalah blok kode dalam grup untuk menyelesaikan task atau fitur,Function dapat dipanggil cukup dengan menambahkan tanda kurung () setelah nama fungsi tersebut.

- Parameter merupakan syarat input yang harus dimasukkan kedalam fungsi,saat membuat fungsi kita harus tau data data yang dibutuhkan
- Argumen merupakan nilai yang dimasukkan kedalam fungsi yang digunakan saat memanggil function,jumlah nya harus sama dengan jumlah parameternya

```js
    function operasiPerkalian(angka1, angka2){
        return angka1 * angka2;
    }
    // angka 1 dan 2 adalah parameter,dalam hal ini parameter harus bertipe number agar bisa dioalah oleh fungsi nya yaitu perkalian

    console.log(operasiPerkalian(2, 6)) // Output: 12
    // 2 dan 6 adalah parameter nya
```

- Default Parameter adalah nilai awal pada parameter function,yang digunakan untuk menjaga jika terjadi error saat memanggil tanpa argumen
- Function Helper,berguna saat kita menggunakan function yang sudah ada pada function lain
- Arrow Function fitur terbaru dari ES6 yang berguna untuk menulis fungsi dengan singkat dan lebih mudah dibaca,syntax nya :

```js
    const namaFungsi = (parameter1, ..., parameterX) => {
        // kode yang ingin dijalankan dalam fungsi
    };
```

contohnya :

```js
    // fungsi dengan parameter
    const operasiPenjumlahan = (bilangan1, bilangan2) => {
        const hasil =  bilangan1 + bilangan2;
        return hasil;
    };
    console.log(operasiPenjumlahan(3, 4)); // Output: 7

    // fungsi yang tidak memiliki parameter
    const namaJenisAnjing = () => {
        const anjing = ["Pug", "Bulldog", "Poodle"];
        return anjing[Math.floor(Math.random()*(anjing.length))];
    }
    console.log(namaJenisAnjing()); // Output: Pug (hasil random)
```

***

## **Tipe Data di Javascript**

### Tipe Data Primitif

- Boolean adalah tipe data yang hanya berisi true dan false,tipe data ini hanya digunakan untuk nilai yang berupa 2 pilihan.
- Null adalah salah satu tipe data yang tidak memiliki nilai
- Undefined adalah tipe data yang sudah dideklarasikan namun belum diberi nilai
- Number adalah tipe data yang menunjukkan sebuah angka
- BigInt adalah tipe data yang digunakan untuk pengoperasian dengan bilangan bulat dalam jumlah besar,dengan menambahkan huruf n dibelakang bilangan bulat tersebut
- String adalah tipe data untuk menulis karakter,dengan menggunakan tanda kutip tunggal maupun ganda,biasa digunakan untuk membuat kalimat.

### Tipe Data Non Primitive

- Objek adalah tipe data yang memungkinkan anda menggunakan tipe data lain di dalamnya. Tipe data ini akan berisi nilai dari tipe data. Contoh penggunaan tipe data ini adalah dalam form formulir dimana mungkin akan ada nilai dari tipe data lain di situ.
- Array adalah tipe data yang digunakan untuk menyimpan banyak nilai pada suatu variable
- Function adalah tipe data yang berisi sebuah perintah untuk melakukan sesuatu

***

## DOM Manipulation

<img src="https://th.bing.com/th/id/R.b972aaae3c4ea5517ad94386867df37c?rik=%2bO1wLmaJKctbIg&riu=http%3a%2f%2fcfile27.uf.tistory.com%2fimage%2f2748FA4A525A911B31A08F&ehk=khwCEQUG7OTF7ujTL3zDYBTGhxywbGr8SH9a99xLdaI%3d&risl=&pid=ImgRaw&r=0" alt="DOM TREE" />

### Javascript DOM(Document Object Model) dapat membuat HTML menjadi dinamis,seperti:

- Mengubah element HTML pada halaman website.
- Mengubah attribute HTML pada halaman website.
- Mengubah CSS style pada halaman website.
- Menambah dan/atau menghapus element maupun attribute HTML.
- Menambah HTML event (contoh: efek klik pada mouse, hover pada mouse, dan lain-lain) pada halaman website.
- Berinteraksi dengan semua HTML event di website.Contoh penggunaanya:

```html
    <!-- File index.html -->
    <input id="umur" type="text" value="20" />
```

Utk mengakses value diatas,lakukan dengan cara berikut:

```js
    let umur = document.getElementById("umur").value;

    console.log(umur); // Output: 20
```

Penjelasan nya

- _document_ utk mengakses element HTML apapun pada website
- _getElementById_,method dari document
- _value_properti dari objek element HTML yang dikembalikan dari method getElementById yaitu input nya

### Mengubah Konten Elemen

- element.textContent,properti yang digunakan untuk mengatur atau mendapatkan konten teks.
- element.innerHTML,sama seperti textcontent yang menajadi pembeda,innerHTML mengubah konten HTML dalam sebuah element

### DOM Events

Ada banyak tipe HTML element di javascript,diantaranya :

- _onclick_,digunakan untuk user ngeklik elemen HTML
- _onload_,digunakan untuk menandakan browser berhasil di load

Contoh penggunaan onClick 

```html
    <!-- html -->
    <button id="demo">Click Me!<button>
```

```js
    let demo = document.getElementById("demo");
    demo.onclick = showMessage();

    function showMessage() {
        alert("Hello, World!");
    }
```

Ada EventListener yang memiliki fungsi:

- Bisa dihilangkan
- ada beberapa event listener yang sama untuk 1 element
- Memiliki argumen tambahan

Penggunaannya

```js
    // cari dulu kedua element tersebut berdasarkan id-nya

    const input = document.getElementById(“user-input”)
    const button = document.getElementById(“alert-button”)

    // tambahkan event listener
    button.addEventListener(“click”, function() {
        alert(input.value)
    })

    // atau

    button.onclick = function() { alert(input.value) }

```

Untuk menambahkan Javascript kedalam dokumen HTML tambahkan tag

```html

<script> dalam tag <head> atau <body> Namun umum nya terletak dalam tag <head>

<!-- jika diletakkan di dalam head, tampahkan atribut 'defer' -->

```


