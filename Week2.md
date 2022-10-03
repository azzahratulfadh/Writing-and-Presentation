**Writing Week 2**
***
**JS Dasar Scope dan JS Dasar Function**

***JS Dasar Scope***
* Scope adalah konsep dalam flow data
* Menentukan suatu variabel bisa diakses pada scope tertentu atau tidak
* Blocks adalah code yang berada didalam curly braces {}
* Conditional, function dan looping menggunakan blocks
* Global scope variabel yang dapat diakses dimanapun dalam suatu file, agar menjadi Global Scope variabel harus dideklarasikan diluar Blocks
* Contoh
```
let myName = 'Aya';

function greeting(){
    return myName;
}
console.log(myName);//Aya
```

***JS Function***
* Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task atau 1 fitur
* Contoh
```
function greeting(){
    return 'Hello World';
}
```
* Parameter Function dapat menerima sebuah inputan data dan menggunakannya untuk melakukan tugas/task
```
function penambahan(a, b){
    return a + b;
}
```
* Argumen Function merupakan nilai yang digunakan saat memanggil function
* Jumlah argumen harus sama dengan jumlah parameter
```
function penambahan(a, b){
    return a + b;
}
console.log(penambahan(5, 5)
```
* Default parameter digunakan untuk memberikan nilai awal/ default pada parameter function
* Arrow function merupakan caa lain menuliskan function
* Conroh
```
const greeting = (a,b) => {
    return a + b;
}
```

**Tipe Data**
* string - deretan karakter yang diapit oleh sepasang tanda kutip;
* number - bilangan bulat, pecahan, dan lain-lain;
* boolean - nilai benar dari sebuah pernyataan yang dituliskan sebagai true atau false;
* null - sebuah nilai yang berarti kosong atau menunjuk pada nilai yang tidak ada;
* undefined - berbeda dari null, undefined menandakan kondisi variabel yang belum diberi sebuah nilai. Jadi pernyataan "nilai variabel itu adalah undefined" sebenarnya kurang tepat, sebab variabelnya memang tidak mempunyai sebuah nilai;
* symbol - sebuah nilai unik yang dihasilkan tiap kali kita memanggil fungsi Symbol(). Nilai unik ini memiliki beberapa kegunaan seperti memberi nomor * identifikasi unik dan berperan sebagai nama properti unik sebuah objek;
* object - sebuah kumpulan pasangan properti dan nilai. Seperti objek dalam kehidupan sehari-hari saja. Misalnya objek Apel memiliki properti warna dengan nilai merah.

**DOM (Document Object Model)**
* DOM adalah jembatan supaya bahasa pemrograman dapat berinteraksi dengan dokumen HTML
* Dengan adanya DOM JavaScript diberi akses untuk membuat HTML menjadi dinamis seperti :
    + Mengubah element HTML pada halaman website.
    + Mengubah attribute HTML pada halaman website.
    + Mengubah CSS style pada halaman website.
    + Menambah dan/atau menghapus element maupun attribute HTML.
    + Menambah HTML event (contoh: efek klik pada mouse, hover pada mouse, dan lain-lain) pada halaman website.
    + Berinteraksi dengan semua HTML event di website.
* Contoh Penggunaan DOM :
* Element HTML
```
<input id="umur" type="text" value="20" />
```
* Script JS
```
let umur = document.getElementById("umur").value;

console.log(umur); // Output: 20
```

* File HTML --> Load --> DOM
* DOM dalam bentuk tree structure
* Element
    + cuma HTML element
    + <spam>, <div>
* Node 
    + setiap bagian terkecil di HTML
    + text, comment, <span>
* Macam - Macam Tranversing
    + Ke Bawah
        1. getElementByID
        2. getElementsByClassName
        3. getElementsByTagName
        4. querySelector
        5. querySelectorAll
        6. children
    + Ke Atas
        1. parentElement
        2. closest()
    + Ke Samping
        1. nextElementSibling
        2. previousElementSibling
        
* Contoh getElementByTagName
```
<!-- html -->
<h1 id="title">Hello, World!</h1>
<p>Selamat Datang di Skilvul</p>
<h1 class="subtitle">Mari Belajar JavaScript</h1>
let semuaTagH1 = document.getElementsByTagName("h1");

console.log(semuaTagH1); // Output: HTMLCollection(2) [h1#title, h1.subtitle]
console.log(semuaTagH1[0]); // Output: <h1 id="title">Hello, World!</h1>
console.log(semuaTagH1[1]); // Output: <h1 class="subtitle">Mari Belajar JavaScript</h1>
```

* Contoh Traversing ke bawah
```
let title = document.getElementById("title")
console.log(title)

let items = document.getElementsByClassName("item")
console.log(items[2]);
```
* Contoh Traversing ke atas
```
console.log(itemQuery.parentElement);
console.log(itemQuery.closest(".list"));
```
* Contoh Traversing ke samping
```
console.log(itemQuery.previousElementSiblingc);
console.log(itemQuery.nextElementSibling);
```
* Memanipulasi Content :
    + Deklarasi variabel header sebagai wadah untuk menyimpan tag HTML
 ```
  let header = document.getElementById("header");  
 ```
* Memanipulasi Content pada Header content dari pemilik element dengan id header dengan text.Content
 ```
  document.getElementById("header").textContent = "Teks Heading" 
 ```
    
**DOM Event**
* Events adalah kejadian/kegiatan/interaksi yang terjadi pada website
* 3 cara memberikan event
    + HTML Attribute
    + Event Property
    + addEventListener()
* Macam - Macam Events 
    + click
    + submit
    + focus
    + blur
    + hover
    + change
    + scroll
    + dll
* Contoh DOM Events
```
<!-- html -->
<button id="demo">Click Me!<button>
// js
let demo = document.getElementById("demo");
demo.onclick = showMessage;

function showMessage() {
   alert("Hello, World!");
}
```

