"# aircnc-omnistack9.0"

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



---

### Controllers

>>> Business Rules

\src\Controllers
