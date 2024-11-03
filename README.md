*Índice*
- Descripción
- Tecnologías Utilizadas
- Funcionalidad
- Uso de la página

*Descripción*
- El siguiente desafío consiste en crear un servidor con express, que nos permita realizar consultas en una base de datos. El proyecto se enmarca dentro del desafío 4 del módulo 7 del BootCamp de DesafioLatam

*Tecnologías utilizadas*
- JavaScript
- Node
- Node Express JS
- PostgreSQL

*Funcionalidad*
- El desafío en si nos permite crear y mostrar publicaciones con imágenes y descripciones.

*Uso de la página*
## Backend
1. Requerimientos:
Ocupa las siguientes instrucciones SQL para crear una base de datos likeme y una tabla posts en PostgreSQL.

```bash
CREATE DATABASE likeme;
CREATE TABLE posts (id SERIAL, titulo VARCHAR(25), img VARCHAR(1000),
descripcion VARCHAR(255), likes INT);
```

Comando para instalacion de dependencias.
```bash
npm i
```

2. Configuraciones:
Conexion con pg con la base de datos ./database/consultas.js
```js
const pool = new Pool({
     host: 'localhost',
     user: 'postgres',
     password: '123456',
     database: 'likeme',
     port: 5432,
     allowExitOnIdle: true,
   });
```
Puerto del servidor ./index.js
```js
const PORT = process.env.PORT || 3000;
```

3. Uso:
Se pueden utilizar los siguientes comandos.
```bash
npm run start
```
```bash
npm run dev
```

## Frontend
1. Requerimientos:
Comando para instalacion de dependencias.
```bash
npm i
```

2. Configuraciones:
En este archivo `src\services\postService.js` tu puedes cambiar la API URL

```js
const URL_API = "http://localhost:3000/posts";
```

3. Uso:

Se pueden utilizar los siguientes comandos.
```bash
npm run dev
