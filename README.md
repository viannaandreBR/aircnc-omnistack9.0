"# aircnc-omnistack9.0"

## start

> /Backend
>> yarn dev


>> /Mobile
>> yarn start

---
## Unit 1 - Environment

> node
>> node -v
>> v 10.16.3

> npm
>> npm -v
>> 6.9.0

> yarn
>> yarn -v
>> 1.17.3

---
## Unit 2 - Backend

> mkdir backend

> cd backend

> yarn init -y

> code .
>> install command in path

### Terminal VS Code
>> <CTRL>+<SHIFT>+<'>
>> <CTRL>+<SHIFT>+<p>
>> Toggle Integrated Terminal


### Express Dependencies
>> Express is a Microframework inside Node.JS
>>yarn add express
>>
>> API REST
>> get, post, put, delete
>>
>> app.get('/', (req,res) => {
  return res.json({message: 'Hello World !'});
});

### New Files
>> yarn.lock => Dependencies Cache
>> node_modules => Repositories Dependencies with Code


### mkdir src
>> server.js


### nodemon Dependencies
>> yarn add nodemon -D


### script yarn dev

> package.json
"scripts":{
   "dev": "nodemon src/server.js"
 },

> yarn dev
>> npm run dev


### Insomnia.rest
>> https://insomnia.rest/
>> Debug & Test API´s


### Routes Get, Post, Put, delete
// Métodos Get, Post, Put, Delete
//
// Params
// req.query  => Acessar query params (para filtros)
// req.params => Acessar route params (para edição, delete)
// req.body   => Acessar corpo da requisição (para criação, edição)

app.use(express.json());

// Get
app.get('/users', (req,res) =>{
  return res.json( { idade: req.query.idade });
});

// Post
app.post('/users', (req,res) =>{
  return res.json(req.body);
});

//Put
app.put('/users/:id', (req,res) =>{
  return res.json( { id: req.params.id });
});


---

### Create Routes.js



---

### Connect MongoDB Atlas

https://cloud.mongodb.com

> yarn add mongoose

> Connection Test MongoDB Atlas
>>> http://portquiz.net:27017/


---

### MVC - Models, Views, Controllers


\src\models
\src\views => ReactJS, ReactNative
\src\controllers



---

### Models

\src\models\User.js

\src\models\Spot.js


---

### Controllers

>>> Business Rules

\src\controllers

>> SessionController.js
// index, show, store, update, destroy



\src\controllers\SessionController.js

\src\controllers\SpotController.js


Requisition with Image Upload => Use Multipart Form
### Library MultiPart Data // Uploads Images

> yarn add multer

>>> \config\upload.js


> JWT Autentication
>> Header
>> User 5d94beb7cc2cc533907d23c1



----

##  FrontEnd / Interface Web

> yarn create react-app frontend
> npmx create-react-app frontend
>> https://babeljs.io/
>> https://webpack.js.org/


> Execute Backend Services
>> cd Backend
>> yarn dev


> Iniciar Frontend Services
>> cd FrontEnd
>> yarn start


> Create folder \assets
>> \src\assets


> Roboto Font
>> https://fonts.google.com/specimen/Roboto?selection.family=Roboto

body, input, button {
  font-family: 'Roboto', Arial, Helvetica, sans-serif;
  font-size: 14px;
}



> Extension Color HighLight


> Library Call API
>> yarn add axios



> CORS Dependencies
>>> Access to XMLHttpRequest at 'http://localhost:3333/sessions' from origin 'http://localhost:3000' has been blocked by CORS policy: Response to preflight request doesn't pass access control check: No 'Access-Control-Allow-Origin' header is present on the requested resource.

>> yarn add cors




> Browser Database

    localStorage.setItem('user', _id);

    import { BrowserRouter } from 'react-router-dom';

    import { BrowserRouter, Switch, Route  } from 'react-router-dom';



> Bibliotecas de Rotas do ReactJS
>>> yarn add react-router-dom



> Virtual Schema mongodb
SpotSchema.virtual('thumbnail_url').get(function() {
  return `http://localhost:3333/files/${this.thumbnail}`
})




---

## Mobile - ReactNative

> Duas formas de iniciar o ReactNative

>>> Expo
>>>>> não precisa instalar as dependencias nativas: Android, iOS
>>>>> npm install -g expo-cli
>>>>> expo init mobile
>>>>> cd Mobile
>>>>> yarn start

>>> CLI



>> Install React-Navigation
>>>> yarn add react-navigation



> React navigation
>>>> https://reactnavigation.org/
>>>>https://reactnavigation.org/docs/en/getting-started.html
>>>>
>>>> expo install react-native-gesture-handler react-native-reanimated


> Axios Router Communication
>>> yarn add Axios


---

>> URL Address

https://pastebin.com/dB3hFgZw

<Image style={styles.thumbnail} source={{uri: "IP_LOCAL_COM_HTTP/files"+item.thumbnail_url.split('/files')[1]}}/>


>> mongodb

mongodb+srv://<username>:<password>@cluster0-fal35.mongodb.net/admin




---

## Advanced Functions

> yarn add socket.io

> Protocols
>> Http -> Assincrono
>> WebSocket -> Sincrono
