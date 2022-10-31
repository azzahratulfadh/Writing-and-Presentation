***Writing Week 5***

***Week 1 FrontEnd Bootcamp***
****
* React JS dibuat oleh tim Facebook menggunakan React JS pada sisi front-end
* React JS adalah framework view library untuk membuat tampilan UI(User Interface) pada website
* Alternatif yang bisa digunakan selain React seperti :
    + angular
    + vue
    + svelte
* Alasan kenapa menggunakan React JS
    + React JS is FAST
    --> React JS membuat Aplikasi front-end menjadi lebih cepat walaupun harus menghandle data
    + React JS is MODULAR
    --> React JS membagi 1 tampilan pada website menjadi komponen - komponen kecil
    + React JS is Scalable
    --> React JS dapat digunakan pada aplikasi berskala kecil hingga besar dan kompleks
    + React is Popular
    --> React JS sudah banyak digunakan sehingga mudah dicari dan mendapatkan pekerjaaan dengan menggunakan React JS
* Cara instalasi React JS 
    + Instal Node JS
    + Buat folder lalu buka git bash
    + lalu instal react dengan cara "npx create-react-app nama-folder "
    + lalu tunggu proses install
    + tunggu sampai ada tulisan "Happy Hacking"
* Selain itu bisa membuat folder dengan cara 
    + npm create vite@latest namafolder --template react
    + dimana lebih mempercepat proses instal
    
**React Component**
* Component adalah salah satu core React JS
* Component membagi UI dalam satuan - satuan kecil dimana dalam 1 page ada beberapa component yang bisa dibuat
* Cara membuat component
    + Menggunakan function
    + Mengguakan class
 ![image](https://user-images.githubusercontent.com/82355691/198987720-f22b782b-fefd-463e-a083-56fabca6247f.png)

* Buatlah file didalam components dengan huruf besar misalnya : Home.jsx
* JSX adalah sebuah sintax. JSX perlu di compile untuk menjadi Javascript
* Setiap JSX hanya bisa memiliki 1 parent element
```
import React from "react"

function App() {
  return(
    <p>Hi !!</>
    <p>Aku Azzah</p>
  )
}
export default App
```
* Sintax diatas akan eror karena memiliki 2 parent element
* Jika ingin membuat 2 parent element maka harus menggunakan tag element div dan tag fragment
```
import React from "react"

function App() {
  return(
  <div>
    <p>Hi !!</>
    <p>Aku Azzah</p>
</div>
  )
}
export default App
```
* atau tag fragment
```
import React from "react"

function App() {
  return(
 <>
    <p>Hi !!</>
    <p>Aku Azzah</p>
</>
  )
}
export default App
```
* Styling CSS dalam React JS
* Membuat sintax di App.css
```
.profile-img {
  width: 150px;
  height: 150px;
  overflow: hidden;
  border-radius: 100%;
  object-fit: cover;
}

.profile-info {
  margin-left: 20px;
}

.profile-container {
  margin-left: 100px;
  display: flex;
}
```
* lalu mengimport nya pada file App.jsx
```
import "./App.css";
import MemberInfo from "./components/MemberInfo";

function App(){
  return(
    <>
      <MemberInfo name={"Ratul"} age={"19"} info={"Peserta Bootcamp Frontend Skilvul"} 
      imgUrl={"https://www.rd.com/wp-content/uploads/2017/09/01-shutterstock_476340928-Irina-Bg.jpg?fit=640,427"}/>

      <MemberInfo name={"Fadhilah"} age={"25"} info={"Peserta Bootcamp Frontend Skilvul"} 
      imgUrl={"https://images.unsplash.com/photo-1628563694622-5a76957fd09c?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8aW5zdGFncmFtJTIwcHJvZmlsZXxlbnwwfHwwfHw%3D&w=1000&q=80"}/>
    </>
  )
}

export default App;
```
* Hasilnya ketika di run ouput
![image](https://user-images.githubusercontent.com/82355691/198987810-f11ea209-ee6d-48f1-ad95-ea3ed915ebc1.png)


**State dan Props**
* State adalah sebuah object untuk nyimpan data di react yang akan di render ulang ketika data mengalami perubahan
* useState dipanggil dalam function component untuk meanmbahkan suatu state lokal eact akan menyimpan state antar render. useState memberikan dua hal: nilai state saat ini dan fungsi untuk memperbarui nilai tersebut. Anda dapat memanggil fungsi ini dari sebuah event handler atau dimanapun
* Penggunaan useState
```
   import { useState } from 'react';
   import './App.css';
   import MemberInfo from './components/Memberinfo';

   function App() {
     const [name, setName]= useState("Aya");
     const [age, setAge]= useState(20);

     return (
       <>
         <MemberInfo name={name} age={age} info={"Siswa MSIB Skilvul"} imgUrl={"https://www.rd.com/wp-content/uploads/2017/09/01-shutterstock_476340928-Irina-Bg.jpg?fit=640,427"} nameColor={"red"} />

         <br />
         <button onClick={()=> setName("aya")}>Change Name</button>;
         <button onClick={()=> setAge(age + 1)}>Change Age</button>;
       </>
     );
   }

   export default App;
```
* Props digunakan untuk komunikasi pengiriman data
* Contoh penggunaan MemberInfo.jsx
```
const MemberInfo = ({name, age, info, imgUrl}) => {
    return (
        <div className="profile-container">
        <img src={imgUrl} alt="" className="profile-img"/>
        <div className="profile-info">
            <h2>{name}</h2>
            <h3>{age} tahun</h3>
            <p>{info}</p>
        </div>
        </div>
    );
};

export default MemberInfo;
```
* file App.jsx
```
import "./App.css";
import MemberInfo from "./components/MemberInfo";

function App(){
  return(
    <>
      <MemberInfo name={"Ratul"} age={"19"} info={"Peserta Bootcamp Frontend Skilvul"} 
      imgUrl={"https://www.rd.com/wp-content/uploads/2017/09/01-shutterstock_476340928-Irina-Bg.jpg?fit=640,427"}/>

      <MemberInfo name={"Fadhilah"} age={"25"} info={"Peserta Bootcamp Frontend Skilvul"} 
      imgUrl={"https://images.unsplash.com/photo-1628563694622-5a76957fd09c?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8aW5zdGFncmFtJTIwcHJvZmlsZXxlbnwwfHwwfHw%3D&w=1000&q=80"}/>
    </>
  )
}

export default App;
```
**Bootstrap di React**
* bisa dengan install bootsrap lalu memanggilnya di main
* atau bisa menggunakan link dan menyisipkan di index
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <link rel="icon" href="%PUBLIC_URL%/favicon.ico" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <meta name="theme-color" content="#000000" />
    <meta
      name="description"
      content="Web site created using create-react-app"
    />
    <link rel="apple-touch-icon" href="%PUBLIC_URL%/logo192.png" />

    <title>React App</title>
    
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-Zenh87qX5JnK2Jl0vWa8Ck2rdkQ2Bzep5IDxbcnCeuOxjzrPF/et3URy9Bv1WTRi" crossorigin="anonymous" /> <!-- Bootstrap CSS -->
  </head>
  <body>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-OERcA2EqjJCMA+/3y+gxIOqMEjwtxJY7qPCqsdltbNJuaOe923+mo//f6V8Qbsw3" crossorigin="anonymous"></script>
  </body>
</html>
```
* Stateless Component adalah component yang tidak memiliki state internal sendiri, melainkan data yang didapatkan oleh komponen tersebut berasal dari luar
* Statefull Component adalah component yang memiliki state sendiri sehingga stateful component harus menggunakan fungsi

**Handling Events**
* Event React dapat ditulis dalam sintax camelCase
* Seperti onClick bukan onclick
* Kemudian ditulis dengan kurung kribo {}
* Seperti onClick={coba} bukan onClick="coba()"
* Contoh penggunaan :
```
import React from 'react';
function Makan() {
  const lapar = () => {
    alert("ayo makan!");
  }

  return (
    <button onClick={lapar}>lapar</button>
  );
}

export default Makan;
```
