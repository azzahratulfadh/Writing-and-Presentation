***Writing Week ***

***Week 3 FrontEnd Bootcamp***
****
**React Context**
* React Context dirancang untuk berbagi data yang dapat dianggap "global" pada pohon komponen React
* Pada React Context pengguna yang diautentikasi saat tema, atau bahasa pilihan
* Penggunaan React Context
    + Untuk membuat new Context, digunakan fungsi "createContext" baru React
    + Fungsi "createContext" mengembalikan "a Provider" dan "a Consumer" component
* Install React Context
```
npm install react-context --save
```
* React Context menyediakan cara untuk berbagi nilai seperti ini di antara komponen tanpa harus oper prop secara explisit melalui setiap tingkatan diagram
* Contoh penggunaan
```
import React, { createContext, useState } from 'react'

export const KeranjangCountContext = createContext()

function KeranjangCountProvider({children}) {
  const [keranjangCount, setKeranjangCount] = useState(0)

  return (
    <KeranjangCountContext.Provider value={{keranjangCount, setKeranjangCount}}>
      {children}
    </KeranjangCountContext.Provider>
  )
}

export default KeranjangCountProvider
```

**React Testing**
* React Testing digunakan mengetes komponen pada React tanpa bergantung pada detail implementasinya. Pendekatan ini membuat refactoring menjadi mudah dan juga mendorong Anda untuk menerapkan best practices untuk aksesbilitas
* React Testing terbagi menjadi :
    + Unit Testing
    + Integration Testing
    + UI Testing
* Unit Testing menggunakan Jest 
* Install React Testing
```
npm install --save-dev @testing-library/react
```
* contoh code react testing
```
<?xml version="1.0" encoding="UTF-8"?>
<coverage generated="1667966247614" clover="3.2.0">
  <project timestamp="1667966247614" name="All files">
    <metrics statements="7" coveredstatements="6" conditionals="4" coveredconditionals="3" methods="3" coveredmethods="3" elements="14" coveredelements="12" complexity="0" loc="7" ncloc="7" packages="1" files="1" classes="1"/>
    <file name="app.js" path="D:\skilvul\tech-for-impact\materi-FE\13-testing\01-testing-jest\app.js">
      <metrics statements="7" coveredstatements="6" conditionals="4" coveredconditionals="3" methods="3" coveredmethods="3"/>
      <line num="7" count="4" type="stmt"/>
      <line num="9" count="1" type="stmt"/>
      <line num="10" count="2" type="cond" truecount="1" falsecount="1"/>
      <line num="11" count="0" type="stmt"/>
      <line num="14" count="1" type="stmt"/>
      <line num="15" count="3" type="cond" truecount="2" falsecount="0"/>
      <line num="18" count="1" type="stmt"/>
    </file>
  </project>
</coverage>
```