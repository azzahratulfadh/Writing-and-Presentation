***Writing Week 6***

***Week 2 FrontEnd Bootcamp***
****

**React JS Lanjutan PropTypes**
* Prop Types merupakan sebuah lib yang dapat membantu untuk memeriksa data props yang dikirim agar sesuai ekspetasi
* Jika tidak sesuai, maka akan muncul pesan eror
* Prop Types digunakan untuk men-check type data yang dikirim
* Prop Types berfungsi untuk memastikan tipe data yang dikirim sesuai atau tidak
* Menginstall PropTypes
```
npm install prop-types
```
* Contoh penggunaan PropTypes
```
import PropTypes from "prop-types";

const StudentInfo = ({name, age}) => {
    return (
        <>
        <h2>{name}</h2>
        <h2>{age + 5}</h2>
        </>
    )
}

StudentInfo.propTypes = {
    name: PropTypes.string,
    age: PropTypes.number,
};

export default StudentInfo
```

**React Router**
* React Router merupakan library untuk melakukan routing pada React
* Router digunakan untuk pindah halaman
* Dimana Router membantuk berpindah dari page satu ke page yang lain berdasarkan path url nya
* Cara install / akses React Router
```
npm install react-router-dom@6
```
* Tambahkan code dibawah pada bagian main.jsx
```
import {BrowserRouter} from "react-router-dom";
```
```
<BrowserRouter>
    <App />
</BrowserRouter>
```
* Browser Router digunakan untuk menjalankan react di browser atau untuk membuat router - router sederhana
* 3 cara penggunaan Router
    + Routing dasar
    + Dynamic Router
    + Nested Router
* Contoh penggunaan Dynamic Router dan Nested Router
```
import {Routes, Route, Link} from "react-router-dom"
import HomePage from "./pages/HomePage";
import AboutPage from "./pages/AboutPage";
import DetailPage from "./pages/DetailPage";
import AboutTeacher from "./pages/AboutTeacher";
import AboutStudent from "./pages/AboutStudent";

const App = () => {
  return (
    <>
      <nav>
        <Link to={"/"}>Home |</Link>
        <Link to={"/about"}>About</Link>
      </nav>
      <Routes>
        <Route path="/" element={<HomePage/>}/>
        <Route path="/detail/:id" element={<DetailPage/>}/>
        <Route path="/about" element={<AboutPage/>}/>
        
        {/* Nested Router */}
        <Route path="/about/student" element={<AboutStudent/>}/>
        <Route path="/about/teacher" element={<AboutTeacher/>}/>
      </Routes>
    </>
  )
}

export default App;
```

**State Management React Redux**
* Redux adalah sebuah third party untuk memanipulasi state management didalam react
* Redux merupakan suatu wadah buat menyimpan sebuah data
* Cara kerja Redux :
    + Action merupakan sebuah function yang mereturn sebuah object
    + Reducer merupakan sebuah fungsi yang digunakan untuk mengolah state yang ada di store
    + Store merupakan tempat untuk menampung state
* Hal pertama yang dilakukan ialah install react-redux
```
npm install react-redux
```
* Membuat folder redux dimana berisi folder action, reducer dan store
* Dapat menambahkan sebuah file didalam folder action
* Kemudian 1 file didalam folder reducer lalu import method combineReducer   
* Lalu pada file store import sebuah method createStore

* Setup store di App.jsx
```
 import { createStore } from "redux";
 import { composeWithDevTools } from "redux-devtools-extension";
 import rootReducer from "./reducers"; 
 const store = createStore(
 rootReducer,
 composeWithDevTools()
 )
 export default store;
```
* Membuat folder reducer utuk todolist src/store/reducers/todoReducer.js
```
   const initialState = {
   todos: [
     {
       id: 1,
       title: "title one",
       completed: false
     },
     {
       id: 1,
       title: "title one",
       completed: false
     }
   ]
 }
 const todoReducer = (state = initialState, action) => {
   const { type, payload} = action;
   switch(type){
     default:
       return {
         ...state
       }
   }
 }
 export default todoReducer;
```
* Menggabungkan reducer - reducer didalam file src/store/reducers/index.js
```
  import { combineReducers} from "redux";
  import todoReducer from "./todoReducer";
  export default combineReducers({
  todoReducer
  })
```
* Menghubungkan redux dan app reeact di file app.js
```
  import React from "react";
  import { Provider} from "react-redux";
  import store from "./store"
  const App= () => {
    return(
      <Provider store={store}>
        <div>
          <TodoApp/>
        </div>
      </Provider>
    )
  }
  export default App;
```
* Kemudian mengambil data store
```
  import React from "react";
  import { connect } from "react-redux";
  const TodoApp= ({ todos }) => {
    return(
      <div>
        <h1>todo app</h1>
        {todos.map(todo =>
          <div key={todo.id}>
            <p>{todo.title}</p>
          </div>
        )}
      </div>
    )
  }
  const mapStateToProps = state => ({
    todos: state.todoReducer.todos
  })
  export default connect(mapStateToProps)(TodoApp);
```

**Async Actions with Middleware and Thunk**
* Redux-Thunk adalah sebuah middleware yang memungkinkan kita memanggil pembuat aksi yang mengembalikan fungsi sebagai ganti objek aksi
* Redux-Thunk solusi ketika kita menggunakan fetch data dari sebuah External API atau yang memiliki side effect (proses ashynchronous)
* Lakukan isntall pada react thunk
```
npm install redux-thunk
```
* Lalu lakukan combine pada store/index.js
```
import { createStore, combineReducers, applyMiddleware } from 'redux';
import thunk from 'redux-thunk';
import todoReducer from '../reducer/todoReducer';

const allReducer = combineReducers({
  todo: todoReducer,
  // user: userReducer,
  // product: productReducer
})

const store = createStore(allReducer, applyMiddleware(thunk))

export default store
```