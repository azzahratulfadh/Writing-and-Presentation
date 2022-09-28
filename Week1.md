**Writing and Presentation Test Week 1**

**Day 1 : Unix Command Line dan Git & GitHub Dasar**
A. Unix Command Line
* Unix Command Line merupakan shell yang berbasis teks
* Shell adalah program yang menerima perintah, kemudian meneruskan perintah tersebut ke system untuk dieksekusi
* cara mengakses CLI dan menggunakan terminal dengan menggunakan commandprompt(CMD)
* file system structure merupakan sebuah system mengatur bagaimana
* data disimpan didalam sebuah system
* pwd adalah command untuk melihat current working directory
* ls adalah command untuk melihat isi sebuah directory 
* cd adalah command untuk berpindah directory
* cat adalah command untuk melihat isi files 
* touch adalah command untuk membuat file
* mkdir adalah command untuk membuat direktori
* cp adalah command untuk menyalin file
* cp-R adalah command untuk menyalin direktori 
* mv adalah command untuk memindahkan atau me-rename file
* mv -R adalah command untuk memindahkan atau me-rename direktori 
* rm adalah command untuk menghapus file 
* rm -d adalah  command untuk menghapus direktori


B. Git & GitHub Dasar
* Git &GitHub merupakan tools yang berkolaborasi dalam mengerjakan proyek yang sama tanpa harus repot copy paste folder aplikasi yang terupdate
* Perbedaannya yaitu Git adalah pengubah kode dan dapat digabungkan menuju perangkat lokal. Github menyediakan interface grafis berbasis cloud sebagai tempat untuk melakukan seluruh tugas
* Repository adalah direktori proyek dimana
1 repository = 1 proyek = 1 direktori
    git init proyek
* commit adalah kondisi dimana revisi sudah disimpan pada version control
    git commit -m "Commit pertama"
* Melihat apakah terjadi perubahan atau tidak pada git
    git status
* Menambah filebaru atau yang telah dirubah
    git add
* Mempublish aplikasi ke Github
    + Buat Project misal : belajargit
    + Buka project dengan vscode
    + Buat file index.html
    + Buka terminal di vscode pilih yang bash
    + lalu git init (git init cuman dijalankan 1 kali)
    + lalu git add .
    + lalu git commit -m "initial commit"
    + lalu jika ada perubahan maka simpan lagi dengan git add . lalu di git commit kembali
    + Lalu simpan ke github
    + pilih new repositori dengan nama "belajargit"
    +lalu hubungkan project dilaptop dengan github
    + Dengan git remote add origin
    + terakhir upload dengan git push
* Melakukan Deploy ke Netlify
    + login bisa dengan akun github
    + pada sites pilih import an existing project
    + klik github, lalu pilih repository yang akan di upload
    + terakhir klik deploy

**Day 2 : HTML**
* HTML adalah singkatan dari Hyper Text Markup Language
* HTML adalah bahasa komputer yang digunakan untuk membuat kerangka atau struktur untuk halaman website di internet
* Fungsi HTML adalah sebagai kerangka
* Struktur Dasar HTML
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Week 1</title>
    <link href="coba.css" type="text/css" rel="stylesheet"/>
</head>
<body>
    <div>
        <h1>Writing and Presentation Week 1</h1>
    </div>
</body>
</html>
```
* 2 tools utama dalam membuat HTML yaitu Browser dan Code Editor
* HTML terdiri dari komponen yang disebut Tag. ada 2 tipe tag
        Opening tag : ``<p>``
        Closing tag : ``</p>``
        Contoh : ``<p> Week 1 </p>``
* Salah satu cara menjalankan HTML yaitu dengan menggunakan "Line Server"
* Semantic HTML yaitu seperti header, footer, nav, section dll
```
<body>
    <header>
        <h6>Week 1</h6>
    </header>
    
    <nav>
        <a href="#>Home</a>
    </nav>
    
    <footer>
        Copyright;2022 by azzahratulfadh
    </footer>
```
* Menjalankan HTML sederhana dengan line server di VSCode
    + Yaitu dengan download terlebih dahulu extensions di vsc terlebih dahulu
    + cara menjalankannya klik kanan pada file misal file index.html lalu pilih "Open with line server"

**Day 3 : CSS**
* CSS atau Cascading Style Sheets merupakan bahasa yang digunakan untuk mendesain halaman website
* CSS digunakan untuk mengubah warna, menggunakan font custom, editing text format, mengatur tata letak 
* Struktur CSS :
```
.elementHMTL {
    property : value
}
```
* Menyisipkan CSS didalam file HTML ada 3 yaitu
    1. Inline CSS, yaitu menggunakan attribute style untuk menyisipkan kode CSS langsung didalam HTML element
    2. Internal CSS, yaitu menggunakan element <style> untuk menyisipkan kode CSS. Element <style> tersebut diletakkan didalam element
    3. External CSS, yaitu sebuah file CSS terpisah yang disambungkan dengan file HTML dengan menggunakan element <link>
* Cara mengakses file CSS di HTML
```
<link href="styles.css" type="text/css" rel="stylesheet"/>
```
* Flexbox adalah cara untuk mengatur layout
* Flexbox memiliki kemampuan untuk menyesuaikan layout secara otomatis
* Flexbox memiliki 1 parent/container dan bisa beberapa child/item
* Flex-dirextion digunakan untuk mengatur letak item child
* Flex-wrap akan membuat tata letak item children dalam 1 line saja
* Flex-flow digunakan sebagai shortcut untuk set up flex-direction dan flex-wrap bersamaan
* Properti order pada flex berfungsi untuk ordering item mana yang ingin diatur posisinya berdasarkan urutan order
* Justify-content digunakan untuk mengatur tata letak dan sopace antar item child secara horizontal atau main axis
* Flex-grow digunakan untuk mengatur suatu item child pada flexbox
* Flex-shrink adalah properti yang membuat size suatu item child mengecil secara relatif terhadap item child yang lainnya
* Flex-basis adalah properti yang sama fungsinya seperti width

**Day 4 : Algoritma dan Data Structures**
* Algoritma adalah deskripsi berupa step-step yang dibutuhkan untuk menyelesaikan suatu masalah
* Data Struktur digunakan untuk mengelola data Sedangkan Algoritma yang akan menyelesaikan suatu permasalahan menggunakan data tersebut
* Pseudocode adalah menuliskan algoritma dengan umumnya bahasa inggris sebelum diimplementasikan ke bahasa pemograman tertentu
* Manfaat algoritma yaitu membantu untuk menyelesaikan masalah secara runtut
* Algoritma sederhana "Saat proses mengambil minum"
    + pertama pergi menambil gelas
    + lalu pergi ketempat galon
    + kemudian mengambil air
    + lalu meminumnya
* Algoritma dalam bahasa pemrograman
```
nilai1 = 15
nilai2 = 4
Output = Input1 + Input2
Print ("Result", output)
```


**Day 5 : JavaScript Dasar (Conditional & Looping)**
* Javascript adalah bahasa pemrograman yang digunakan untuk membuat suatu website menjadi interaktif
* Contoh Syntax Javascript :
    1. prompt
    2. alert
    3. confirm
* Tipe data pada javascript yaitu
    1. Number, yaitu tipe jenis angka. ada integer dan float
    2. String, yaitu terdiri dari huruf, angka, spasi dan simbol. ada char
    3. Boolean, yaitu tipe data yang memiliki nilai true or false
    4. Null, yaitu tipe data pada sebuah variabel yang tidak memiliki nilai
    5. Undefined, yaitu tipe data yang mempresentasikan variabel yang tidak memiliki nilai
    6. Object, yaitu tipe data yang berisi nilai dan berhubungan dengan dunia nyata
* 3 cara mendefinisikan variabel :
    1. var
    2. let
    3. const
* Contoh :
    let nama : "aya";
    let umur : 20:
    console.log(nama);//output : aya
    console.log(umur);//output : 20

***Conditional***
* Conditonal(persyaratan)
* 2 pernulisan perintah conditional
    + menggunakan if, else if dan else
    + menggunakan switch dan case
* Contoh :
```
let nilaiAndi = 95;

if (nilaiAndi > 80) {
  console.log("SANGAT MEMUASKAN");
} else if (nilaiAndi >= 60 && nilaiAndi <= 80) {
  console.log("MEMUASKAN");
} else {
  console.log("JANGAN MENYERAH, COBA LAGI!");
}

// Output: SANGAT MEMUASKAN
```

***Looping***
* looping(perulangan)
* 5 jenis loop di javascript
    + for
    + for...in
    + for...of
    + while
    + do...while
* Contoh : Perulangan 1-10
```
for(let i = 1; i<=10; i++){
    if(i == 6){
       console.log(i, "yeyy ketemu")
    }else{
       console.log(i)
    }
}
```
