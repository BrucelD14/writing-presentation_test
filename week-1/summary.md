
# WRITING & PRESENTATION TEST WEEK 01

## Unix Commamnd Line

19 September 2022

### Shell

> Shell adalah program yang digunakan untuk berkomunikasi atau memberi perintah pada sistem.

### Command Line Interface (CLI)

> Command Line Interface (CLI) merupakan jenis shell yang berbasis text, contohnya command promt, powershell.

### Mengakses CLI

Ada beberapa cara untuk mengakses CLI atau terminal, disini sebagai contoh kita gunakan Command Promt. Caranya mudah, kita arahkan cursor ke arah taskbar dan klik icon kaca pembesar untuk mencari. Lalu ketik "command promt" maka secara otomatis kita akan diarahkan ke Command Promt lalu klik enter.

### Filesystem

Data yang tersimpan di dalam komputer atau direktori disimpan secara rapi menggunakan filesystem.
Pada sistem operasi Windows, file dan direktori disimpan dengan struktur yang menyerupai pohon (tree).

### Perintah dalam CLI

Ada banyak perintah/command dalam CLI, berikut adalah beberapa contoh perintah/command dasar dalam CLI

    - pwd (print working directory), untuk melihat current working directory.
    - ls (lists), untuk melihat isi file yang ada di sebuah direktori.
    - cd (change directory), perintah untuk berpindah direktori.
    - head, perintah untuk melihat beberapa baris awal dari sebuah file.
    -  tail, perintah untuk melihat beberapa baris akhir dari file.
    - cat, perintah untuk melihat file.
    - touch, perintah untuk membuat file.
    - mkdir, perintah untuk melihat.
    - cp, perintah untuk menyalin file atau direktori.
        - cp -R, untuk menyalin direktori
    - mv, perintah untuk memindahkan file atau direktori. Dan perintah ini juga bisa digunakan untuk merubah nama file atau direktori.
        - mv -R, untuk memindahkan direktori.
    - rm, perintah untuk menghapus file atau direktori.
        - rm, untuk menghapus file
        - rm -R atau rm -d untuk menghapus direktori

***

## Git & GitHub Dasar

19 September 2022

### Apa itu Git?

Git merupakan sebuah *version control system* yaitu sistem yang mengelola perubahan dari sebuah dokumen atau program komputer. 

### Pentingnya menggunakan Version Control System

1. Pengelola Versi Dokumen

    Version Control System memudahkan kita untuk menyimpan perubahan versi dokumen kita. Kita juga bisa melihat history perubahan dokumen.

2. Memudahkan Kolaborasi

    Contohnya saat kita mengerjakan project website bareng teman, dan kita berbagi tugas seperti kita mengerjakan front-end sedangkan si teman mengerjakan bagian back-end. Nah saat project di produksi pasti perlu digabungin, saat itulah kita memerlukan VCS (Version Control System)untuk memudahkan kita untuk menggabungkan project tersebut.

### Instalasi Git

Untuk download Git, klik [disini](https://git-scm.com/downloads "Download Git").

Setelah di download, install Git seperti menginstall aplikasi pada umumnya.

Setelah selesai di install, cek instalasi git di command promt dengan cara berikut.

```
    git --version
```

kalau berhasil, sistem akan menampilkan versi git yang ter-install.

### Setup Awal Git

```
    git config --global user.name "BrucelD14"
    git config --global user.email "contoh@brucel.com"
```

setelah itu, cek setup Git. Dengan cara berikut

```
    git config --list
```

jika berhasil, sistem akan menampikan list username dan email yang tadi sudah diinput.

### Repository Git

Repository atau biasa disebut repo adalah sebuah direktory proyek yang kita buat.

### Membuat Repository

Ada beberapa cara untuk membuat sebuah repo, salah satunya yaitu seperti dibawah ini.

```
    git init <nama repository>
```

### Git Commit

Perintah git commit digunakan untuk menyimpan perubahan pada version control. Untuk penulisan perintahnya seperti dibawah ini.

```
    git commit -m "commit pertama"
```

yang berada di dalam tanda petik adalah pesan commit, untuk memberi informasi perubahan apa yang telah terjadi.

### Publish Aplikasi ke GitHub

Ada beberapa langkah atau tahapan untuk mempublish aplikasi atau program kita ke GitHub, yaitu:

1. Git Remote

    Sebelum publish aplikasi atau program kita ke github, kita perlu membuat repository remote kita dulu di github. Langkah pertamanya yaitu kita harus login dulu di github. Atau cara lengkapnya bisa dilihat [disini](https://skilvul.com/courses/git-dan-github-dasar/lessons/kolaborasi-dengan-remote-repository-1/topics/git-remote "Git Remote").

    Setelah membuat repository remote di github, langkah selanjutnya adalah menghubungkan repo lokal kita dengan repo remote yang ada di github. caranya sebagai berikut

```
    git remote origin <link repo remote>
```

2. Git Push

    Setelah repo lokal kita dihubungkan dengan repo remote yang ada di github, kita bisa mempublish aplikasi atau program kita menggunakan perintah git push. Caranya sebagai berikut:

```
    git push --set-upstream origin master
```

### Git Clone

Biasanya saat pertama kali bergabung ke sebuah project di github kita akan membuat salinan project tersebut ke repo lokal kita. Nah cara untuk membuat salinan tersebut di git begini caranya:

```
    git clone <link repo> <nama repo>
```

***

## HTML

20 September 2022

HTML merupakan singkatan dari *Hypertext Markup Language*. HTML digunakan untuk 
menampilkan konten pada browser. Beberapa konten yang dapat ditampilkan oleh HTML yaitu text, image, video, link, dan banyak konten lainnya.

### Tools pendukung HTML

Ada 2 tools utama yang harus dipersiapkan untuk membuat HTML yaitu:

1. Browser (chrome, firefox, dll)
2. Code Editor (Sublime Text, Visual Studio Code, dll)

### Struktur HTML

Berikut adalah struktur HTML sederhana.

```
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
        this in my first page web
    </body>
    </html>
```

Beberapa tag utama yang ada pada struktur HTML adalah tag HTML, tag head dan tag body.

### Menjalankan HTML

Untuk menjalankan kode HTML kita memerlukan code editor, ada banyak code editor seperti sublime text, visual code studio, notepad ++ dan banyak lainnya.

Disini sebagai contoh kita akan menggunakan visual studio code. Untuk mendownload klik [disini](https://code.visualstudio.com/Download "Download Visual Studio Code").

> - peran HTML pada web development
> - tools pendukung dalam menggunakan HTML
> - membuat HTML sederhana
> - menjalankan HTML secara manual dan menggunakan live server dari VS Code
> - memahami dan mengimplementasikan tag HTML yang populer
> - memahami dan mengimplementasikan semantic HTML
> - mempublish website sampai ke tahap deployment

# **CSS**

> - peran CSS pada web development
> - beberapa cara menyisipkan CSS ke dalam HTML
> - menggunakan sintaks dasar dari CSS
> - menerapkan styling CSS pada sebuah halaman HTML
> - menggunakan metode responsive web design menggunakan CSS
> - menggunakan flexbox

CSS (Cascading Style Sheets) adalah bahasa yang digunakan untuk mendesain halaman website. Dengan CSS kita bisa mengubah warna, jenis font dan tata letak element HTML.

Di dalam CSS ada yang namanya konsep Flexbox. Flexbox adalah cara untuk mengatur layout. Penggunaan Flexbox direkomendasikan karena penggunaannya yang mudah dan didukung oleh kebanyakan browser.


# **Algoritma**

> - perbedaan antara Algoritma dan Data Structures
> - manfaat dari algoritma dan data structure
> - membuat algoritma sederhana
> - menerapkan algoritma ke dalam bahasa pemrograman
> - memahami Big O Notation
> - mempraktikkan pendekatan menyelesaikan suatu masalah untuk diselesaikan melalui program
> - menerapkan salah satu algoritma dengan JavaScript
> - menerapkan salah satu struktur data dengan JavaScript

Secara definisi `algoritma` adalah suatu urutan dari beberapa langkah logis (masuk akal) dan sistematis (terurut) yang digunakan untuk menyelesaikan masalah tertentu.

- jenis2 algoritma : deskriptif, pseudocode, flowchart

### Pseudocode

Pseudocode adalah menuliskan algoritma dengan umumnya bahasa inggris sebelum kita implementasikan ke bahasa pemograman tertentu. Pseudocode merupakan suatu bahasa yang memungkinkan programmer untuk berpikir terhadap permasalahan yang harus dipecahkan tanpa harus memikirkan syntax dari bahasa pemrograman yang tertentu.

***Membuat Algoritma Sederhana***

> Menghitung luas segitiga

Secara deskripsi dapat ditulis sebagai :
- membuat variabel untuk sisi alas segitiga
- membuat variabel untuk tinggi segitiga
- membuat variabel untuk rumus luas segitiga 
- menampilkan variabel luas segitiga

>Penulisan dengan pseudecode

```js
Judul
Program luas_segitiga

Deskripsi
var alas, tinggi;

Implementasi

alas ← 100;
tinggi ← 64;
luas_segitiga ← 1/2* alas * tinggi;

print luas_segitiga;
```

```js

STORE "alas" with any value
STORE "tinggi" with any value

STORE "luas_segitiga" with
CALCULATE 1/2 times "alas" times "tinggi"

DISPLAY "luas_segitiga"
```

>Penulisan menggunakan Javascript

```js
    let alas = 3;
    let tinggi = 6;
    let luas_segitiga = 1/2*alas*tinggi;
    console.log(luas_segitiga)

```
akan menghasilkan output : 9

# **Javascript Dasar**

> - peran JavaScript pada web development
> - menjalankan JavaScript
> - membedakan berbagai tipe data
> - menggunakan operator
> - membedakan control flow (conditional dan looping)

***Javascipt*** adalah bahasa pemrograman komputer yang dinamis. Pada umumnya Javascipt digunakan pada web browser untuk menciptakan halaman web yang menarik, interaktif serta merapkan berbagai fungsi pada halaman web.

### Tipe Data pada Javascript

- ***number*** : tipe data yang mengandung semua angka termasuk angka desimal.
- ***string*** : grup karakter yang ada pada keyboard laptop/PC kita yaitu letters (huruf), number (angka), spaces (spasi), symbol, dan lainnya.
- ***boolean*** : tipe data yang hanya mempunyai 2 buah nilai (TRUE dan FALSE).
- ***null*** : tipe data yang diartikan bahwa sebuah variable/data tidak memiliki nilai.
- ***undefined*** :tipe data yang merepresentasikan varibel/data yang tidak memiliki nilai. Tipe data undefined biasanya didapat dari hasil kesalahan program (error), kelalaian programmer, dan tidak direncanakan.
- ***object*** : koleksi data yang saling berhubungan (related).

### Operator Javascript

1. ***Assignment Operator***
   Assignment operator digunakan untuk menyimpan sebuah nila pada variabel. Tanda operatoin ini adalah sama denga (=)

2. ***Mathematical Assignment Operator***
   Menggunakan gabungan tanda operator matematika dan sama dengan, misal +=, -= dan lain sebagainya.

3. ***Increment dan Decrement***
   Gunakan increment atau decrement untuk menambah atau mengurangi sebesar 1 nilai. Tanda operatormya adalah ++  atau --.

4. ***Arithmetic Operator***
   Arithmetic operator adalah operator yang melibatkan operasi matematika.
   - Tambah (+)
   - Kuramg (-)
   - Perkalian (*)
   - Pembagian (/)
   - Modulus (%)

5. ***Comparison Operator***
   Comparison operator adalah operator yang membandingkan satu nilai dengan nilai lainnya. Hasil operasi yang melibatkan comparison operator adalah antara true or false
   
6. ***Simbol comparison operator***
   - Lebih kecil dari : <
   - Lebih besar dari: >
   - Lebih kecil atau sama dengan: <=
   - Lebih besar atau sama dengan: >=
   - Sama dengan: ===
   - Tidak sama dengan: !==


7. ***Logical Operator***
   Logical operator biasa digunakan untuk sebuah CONDITIONAL pada pemograman. Menghasilkan nilai BOOLEAN yaitu TRUE or FALSE. Simbol dari Logical Operator adalah sebagai berikut:
   - AND operator (&&) : AND akan menghasilkan nilai true jika kedua atau semua premis bernilai TRUE.
   - OR operator (||) : OR akan menghasilkan nilai true jika salah satu premis mengandung nilai TRUE
   - NOT operator (!) : NOT akan membalikkan sebuah nilai BOOLEAN. TRUE menjadi FALSE dan sebaliknya.

### Conditional
Conditional merupakan statement percabangan yang menggambarkan suatu kondisi.

***IF ... ELSE IF ... STATEMENT***

Perkondisan remote control (menggunakan if else). Else … If statement dapat kita gunakan jika kita mempunyai berbagai kondisi.

```js
let tombol = 4;

if (tombol === 1) {
    console.log('SCTV');
} else if (tombol === 2) {
    console.log('Indosiar');
}else if (tombol === 3) {
    console.log('Trans 7');
} else if (tombol === 4) {
    console.log('Trans TV');
} else {
    console.log('Channel tidak ditemukan');
}
```

Switch case :digunakan untuk mempermudah ketika pengkodisian lumayan panjang/banyak

```js
let tombol = 11;
switch(tombol) {
    case 1:
        console.log('SCTV');
        break;
    case 2:
        console.log('Indosiar');
        break;
    case 3:
        console.log('Trans 7');
        break;
    case 4:
        console.log('Trans TV');
        break;
    default:
        console.log('Channel tidak ditemukan');
}
```

***TRURHY AND FALSY***

Truthy and falsy digunakan untuk mengecek apakah variabel telah terisi namun tidak mementingkan nilainya.

```js
let data = 'Data';

// cek data by truthy
if (data) {
    console.log('Data ini tidak kosong');
} else {
    console.log('Data kosong');
}
```

***TERNARY OPERATOR***

Ternary operator - kurang cocok untuk mengecek banyak kondisi -kalau lebih dari 3 disarankan pake if else

```js
let makan = true;

makan ? console.log('sudah kenyang') : console.log('lapar');
```


### Looping

***FOR LOOP***

For loop  dapat digunakan ketika sudah tau batas awal dan akhir looping di angka berapa. Cara penulisan for :

> for (initialitation; condition; post-exression) { statement }

- Inisialisasi: Sebagai inisialisasi awal dari mana mulainya sebuah pengulangan. Kita memberikan nilai awal/default pada parameter ini
- Condition: For loop akan terus berjalan selama kondisi ini terpenuhi. Selama kondisi bernilai TRUE.
- Post-expression (Increment/Decrement): Iterasi statement yang digunakan untuk mengupdate variabel yang menjadi kontrol pada pengulangan

```js
let angka = 1;
for (angka; angka <= 10; angka++) {
    console.log(angka);
}
```


***WHILE LOOP***

Gunakan WHILE LOOP jika kita tidak mengetahui jumlah pasti pengulangan. WHILE LOOP akan menjalankan instruksi pengulangan kondisi bernilai TRUE.

> WHILE (expression) { statement }

```
let count = 1;
while (count <= 10 ) {
    console.log(count);
    count +=1;
}
```

***DO WHILE LOOP***

Do while cara penulisannya mirip seperti if statement tetapi kalau if statement hanya sekali atau tidak ada perulangan, maka do while akan diulang tetapi belum menegrti hasil dan titik akhirnya.

cara penulisan :

```js
do {
    statement(s);
}while (expression;)
```

contoh penggunaan :
Angka yang dapat dibagi dengan 2,3,4,5,6 

```js
let i = 1
let isKetemu = false

while (!isKetemu) {
    if (
        i % 2 == 0 &&
        i % 3 == 0 &&
        i % 4 == 0 &&
        i % 5 == 0 &&
        i % 6 == 0 
    ) {
        console.log(i);
        isKetemu = true
    }

    i++
}
```