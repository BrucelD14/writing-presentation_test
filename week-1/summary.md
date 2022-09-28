
# WRITING & PRESENTATION TEST WEEK 3

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

# **Algoritma**

> - perbedaan antara Algoritma dan Data Structures
> - manfaat dari algoritma dan data structure
> - membuat algoritma sederhana
> - menerapkan algoritma ke dalam bahasa pemrograman
> - memahami Big O Notation
> - mempraktikkan pendekatan menyelesaikan suatu masalah untuk diselesaikan melalui program
> - menerapkan salah satu algoritma dengan JavaScript
> - menerapkan salah satu struktur data dengan JavaScript

# **Javascript Dasar**

> - peran JavaScript pada web development
> - menjalankan JavaScript
> - membedakan berbagai tipe data
> - menggunakan operator
> - membedakan control flow (conditional dan looping)








