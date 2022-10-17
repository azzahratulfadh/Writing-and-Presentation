***Writing Week 4***

**Asyncronus Fetch dan Asyncronus Await**
* Asynchronous adalah proses jalannya program bisa dilakukan secara bersamaan tanpa harus menunggu proses antrian. Synchronous merupakan bagian dari Asynchronous (1 antrian) dimana proses akan dieksekusi secara bersamaan dan untuk hasil tergantung lama proses suatu fungsi synchronous
* Async merupakan sebuah sintax khusus yang digunakan untuk bekerja dengan promise agar lebih mudah untuk digunakan
* Await sendiri merupakan fungsi yang hanya berjalan dalam Async
* Contoh
```
//async await
//buat async function
async function asyncNonton() {
    try {
      let result = await nonton("jalan")
      console.log(result); //nonton terpenuhi
    } 
  asyncNonton()
```
* Proses Dalam Asyncronus fetch() Pertama, promise, dikembalikan oleh fetch, diselesaikan dengan objek kelas Respons bawaan segera setelah server merespons dengan header.
* Contoh
```
let response = await fetch(url);

if (response.ok) { // if HTTP-status is 200-299
  // get the response body (the method explained below)
  let json = await response.json();
} else {
  alert("HTTP-Error: " + response.status);
}
```
* 

**Responsive Web**
* Responsive web bertujuan membuat desain website dapat diakses dalam device apapun
* Chrome Dev Tools merupakan tools pada google chrome yang digunakan sebagai tools Responsive Web Design
* Dapat diakses dengan " ctrl + shift + j ctrl +shif + m" digunakan untuk melihat toggle bar
* Media query untuk responsive web design umunya menggunakan 2 jenis media query yaitu
    + min-width
    + max-width
* Media Query digunakan untuk membuat beberapa styles tergantung pada jenis device
* Ada 2 cara dalam menggunakan media query
    + Membuat file css berbeda untuk masing-masing device
    + Dapat menggabungkan CSS untuk setting styling berbagai device
* Contoh MediaQuery
``@media screen and (max-width: 500px)``
* Breakpoint adalah sebuah perubahan yang terjadi pada tampilan saat device atau ukuran width
* Terdapat 3 jenis breakpoint yaitu desktop, tablet, dan mobile phone
* Contoh breakpoint
```
@media screen and (min-width: 500px) and (max-width: 300px) {
body {
  background-color: black
  }
 }
```
* Flexbox bertujuan untuk membuat website yang lebih efisien dalam mengatur, menata dan item pada dalam sebuah wadah bahkan ketika ukurannya tidak diketahui dan/atau dinamis (dengan menggunakan kata "flex"
* Dalam Flexbox properties terdapat Flex direction, flex wrap,flex flow dan align items
* Grid merupakan sistem tata letak berbasis 2 dimensi
* Grid ada 2 jenis yaitu Grid Container dan Grid Item

**Git dan Github Lanjutan**
* Langkah - Langkah membuat sebuah organization
    + Membuat repository organization 
    + Menyiapkan repository
    + Kemudian memberi akses dan invite angota (dilakukan oleh leader)
    + Berikan akses owner untuk setiap member
    + kemudian buat branch dengan nama dev
* Kemudian setiap anggota melakukan git clone untuk mendownload repository ke folder
* setiap anggota membuat branch masing - masing
* contoh : A-login, B-register
* Kemudian membuat sebuah file 
* lalu lakukan git add .
* kemudian commit seperti biasa
* setelah itu lakukan push "git push -u origin (nama branch)"
* lalu ajukan pull request
* lalu tunggu ketua kelompok menyetujui dengan klik "merge pull request"
* kemudian lakukan switch ke dev untuk mengambil data dari anggota lain
* kemudian git pull

**Bootstrap 5**
* Bootstrap adalah framework web development berbasis HTML, CSS, dan JavaScript yang dirancang untuk mempercepat proses pengembangan web responsive dan mobile-first
* Bootstrap awalnya bernama Twitter Blueprint 
* Bootstrap dikembangkan oleh Mark Otto dan Jacob Thornton di Twitter sebagai kerangka kerja untuk mendorong konsistensi di perangkat internal yang sesuai
* Bootsrap berfungsi untuk membuat website responsive
* Kelebihan Bootstrap 
    + Mudah digunakan
    + Responsive Grid
    + Kompatibel dengan banyak browser
    + Bootstrap image system
* Bootstrap memiliki komponen utama yaitu
    + Bootsrap.css
    + Bootstrap.js
* Cara konfigurasi bootstrap
    + Membuat tag boostrap di head. Cara memanggil css bootstrap dengan menggunakan href lalu mengganti link href css lokal dengan link boostrap online 
* Breakpoints pada bootstrap ada 5 yaitu sm, md, lg, xl, xxl
* Setiap breakpoint dipilih untuk menampung container yang lebarnya 12 dengan sehingga tersusun rapi. Breakpoint juga mewakili subset ukuran perangkat umum dan dimensi area pandang
* Container adalah blok dasar atau pembungkus boostrap yang terdiri dari contain, pad dan align yang menyelaraskan konten website
* Ada 3 container pada bootstrap yaitu :
    + .container --> menerapkan maksimum pada setipa breakpoint responsif
    + .container-breakpoint --> lebar 100% sampai dengan breakpoint yang ditentukan
    + .container-fluid --> menerapkan 100% ukurannya dari breakpoints