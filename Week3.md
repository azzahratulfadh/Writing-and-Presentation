**Writing Week 3**
***
***Array dan Multidimensional Array***
* Array adalah tipe variabel yang dapat menampung berbagai jenis data dengan tipe yang bermacam-macam, dengan jumlah yang tidak terbatas
* Array mampu menyimpan berbagai macam tipe data dan menyimpan banyak data
* Array dapat menyimpan tipe data String, Number, Boolean dan lainnya
* Array pada javascript dihitung dari index ke-0
* Array memiliki 5 properti yang digunakan yaitu constructor, length, index, input, dan prototype
* Array memiliki method atau biasa disebut dengan built-in methods
* Contoh Array Built-in Methods .push(), . pop(), .shift(), .unshift(),:
```
let arrBuah = [
  "jeruk", 
  "semangka", 
  "pepaya", 
  "rambutan",
  "melon",
  "belimbing"
]
```
* Menambahkan data di akhir menggunakan .push()
* contoh :
```
arrBuah.push("duku") 
```
* Menambahkah data di awal menggunakan .unshift()
* contoh :
```
arrBuah.unshift("anggur") 
```
* Menghapus data di akhir menggunakan .pop()
* contoh :
```
arrBuah.pop("duku")
```
* Menghapus data du awal menggunakan .shift()
* contoh :
```
arrBuah.shift("anggur")
```
* Menghapus data di tengah dengan .spilce()
* contoh :
```
arrBuah.splice(2, 0, "buah naga")
console.log(arrBuah)
```
* Mengambil data dengan cara mencopy menggunakan .slice()
* contoh :
```
console.log(arrBuah);
console.log(slice)
```
**Array Loop**
* Dapat menggunakan for , map dan forEach
```
console.log(arrBuah);
```
* Contoh for
```
for (let i = 0; i < arrBuah.length; i++) {
  console.log(arrBuah[i])
}

for (let i = arrBuah.length - 1; i >= 0; i--) {
  console.log(arrBuah[i])
}
```
* Contoh forEach
```
arrBuah.forEach((item) => {
  console.log(item)
})
```
* Contoh map 
```
let buahSegar = arrBuah.map((item) => {
  return item + " " + "segar"
})
console.log(buahSegar)
```

**Array Multidimensional**
* Array ini dapat dianalogikan dengan array of array
* Multidimensional array dapat menggunakan Property dan Method built-in array
* Contoh Multidimensional Array :
```
let arrMulti = [
  ["nama", "alpha"],
  ["umur", 17],
  ["kelas", "JS"],
]

console.log(arrMulti[0][1]);
console.log(arrMulti[2][1])

arrMulti[2][1] = "CSS"
console.log(arrMulti);
```

***JavaScript Object***
* Object adalah sesuatu yang dapat dilihat dan dirasakan
* Object dalam bahasa pemrograman adlah sebuah tipe data pada variabel yang menyimpan properti dan fungsi(method)
* Properti adalah data lengkap dari sebuah object 
* Method adalah action dari sebuah object
* Key pada object biasanya disebut dengan properti

**Create Object**
```
let siswa = {
    nama: 'terra',
    umur: 17,
    hobi: 'memancing',
    "nomor hanphone": 082367599,
};

console.log(siswa);
```
**Access Object**
* Cara akses object terbagi 2 yaitu :
* dot notation
```
console.log(siswa.nama);
```
* bracket
```
console.log(siswa['nama']);
console.log(siswa["nomor hanphone"]);
```
**Create Key**
* menambahkan properti baru kedalam object
```
let buku = {
    judul: "mantan jadi manten",
    penulis: "hayati",
    "jumlah halaman": 250,
};
console.log(buku);

buku.tahun = 2022;
buku.terjual = 3000;
console.log(buku);

buku["penerbit"] = "gramedia";
console.log(buku);
```
**Assign Object**
```
let hewan = {
    nama: "kucing",
    kaki: 4,
    warna: "putih",
};
console.log(hewan);

hewan.nama = "kelinci";
console.log(hewan);
```
**Delete Object**
```
let hewan = {
    nama: "kucing",
    kaki: 4,
    warna: "putih",
};
console.log(hewan);

delete hewan.warna;
delete hewan.kaki;
console.log(hewan);

hewan.suara = "meong";
console.log(hewan);
```
**Method Object**
```
const greeting = {
    welcome: function() {
        return "halo selamat datang";
    },
    afterPay: function() {
        return "Terimakasih sudah membeli produk kami";
    },
};
console.log(greeting.welcome());
console.log(greeting.afterPay()); 
```
**Nested Object**
```
let buku = {
    judul: 'tips jago javascript',
    tahun: 2022,
    penulis: {
        penulis1: {
            nama: "Reyhan",
            umur: 28,
            kota: "jakarta",
        },
        penulis2: {
            nama: "aby",
            umur: 25,
            kota: "bandung",
        }
    },
};
console.log(buku);
console.log(buku.penulis.penulis1.nama);
console.log(buku.penulis.penulis2.umur);
```
**Loop Object**
```
let siswa = {
    nama: "Reyhan",
    umur: 22,
    asal: "jakarta",
};

console.log(siswa);

for (let key in siswa){
    console.log(siswa[key]);
} 
```
**Array of object**
```
let users = [
    {
        nama: "aya",
        umur: 20,
        alamat: "padang"
    },
    {
        nama: "auzan",
        umur: 18,
        alamat: "jakarta"
    },
    {
        nama: "dila",
        umur: 17,
        alamat: "bandung"
    },  
];
console.log(users);

let data = users.map((el) => {
    console.log(el.nama);
});
```

***JS Inter Rekursif dan Mudules***
**JS Modules**
* Java script modules adalah cara untuk memisahkan code file yang berbeda
* Keuntungannya :
    + mudah untuk mengelola kode
    + kode menjadi tidak menumpuk dalam 1 file
* Export default digunakan untuk mengexport produk utamanya
* Langkah menggunakan JS Modules ialah :
    + Pertama tambahkan type="module" pada script utama
    + Kemudian siapkan script ke-2 dst untuk melakukan export
    + Lalu lakukan import pada file/script utama
* Contoh :
    + Indonesia --> Import
    + Jepang --> Export
    + Amerika --> Export
* Maka Indonesia tidak dapat melakukan export barang ke Jepang maupun Amerika
* Tetapi Jepang dan Amerika dapat mengexport barang ke Indonesia
* Dapat melakukan export pada variabel, function maupun class
* Kata kunci "export" dapat melakukan banyak export
* Kata kunci "export" ditangkap (import) menggunakan kurung {}
* Contoh :
* File index.html
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
    <script src="./indonesia.js" type="module"></script>
</body>
</html>
```
* file indonesia.js
```
import entertaiment, {motor, smartPhone} from "./jepang.js"

console.log(entertaiment);
console.log(motor);
console.log(smartPhone);

motor.splice(1,1)

console.log(motor);
```
* file jepang.js
```
export let motor = ["suzuki", "yamaha", "honda", "kawasaki"]

export let smartPhone = ["LG", "samsung", "fujitsu", "sony"]

let entertaiment = ["anime", "manga", "wibu", "dorama"]

export default entertaiment
```
**Recursive**
* sebuah algoritma sebagai pengganti perulangan dibuat dengan function yang memanggil dirinya sendiri
* Function recursive memiliki 
    + base case --> titik paling kecil(berhenti)
    + recursion case --> titik dia memanggil dirinya sendiri
* Contoh :
```
function faktorial(n) {
  if (n == 1) {
    return 1
  } else {
    return n * faktorial(n - 1)
  }
}
console.log(faktorial(5))
```

***Asynchronous Introduction & Promise***
* Asynchronous adalah sebuah proses yang dilakukan secara tidak berurutan
* Asynchronous menjalankan urutan perintah yang acak karena harus memanggil perintah yang belum selesai
* Terdapat JavaScript thread --> dimana cuma memiliki 1 jalur
* Multi-thread --> memiliki banyak jalur
* Non-Bocking terjadi ketika 1 proses lama maka mempersilahkan yang lain untuk diproses
* Contoh 
```
setTimeout(() => {
  console.log("B")
}, 1000)

console.log("C")
```
* Contoh Promises
```
console.log("PROMISES dari function")
let nonton = (kondisi) => {
  return new Promise((resolve, reject) => {
    if (kondisi == "jalan") {
      resolve("nonton terpenuhi")
    }
    reject("batal nonton")
  })
}

nonton("jalan")
.then(result => {
  console.log(result)
})
.catch(err => {
  console.log(err);
})
```

***Web Storage***
* Web Storage menyediakan mekanisme yang dengannya browser dapat menyimpan sebuah nilai
* Web Storage jauh lebih efektif daripada menggunakan cookie
* Jika ingin mengakses browser dijembatani oleh web API
* Contoh :
```
if (localStorage.getItem("theme") === "dark") {
  document.body.classList.add("dark");
} else {
  document.body.classList.remove("dark");
}

document.getElementById("toggle").onclick = () => {
  if (localStorage.getItem("theme")) {
    localStorage.removeItem("theme");
    document.body.classList.remove("dark");
  } else {
    localStorage.setItem("theme", "dark");
    document.body.classList.add("dark");
  }
};
```

    
