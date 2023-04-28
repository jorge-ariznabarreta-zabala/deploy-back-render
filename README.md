Backend deployment to Render

## Install servers and dependences
npm i json-server cors json-serve
npm i chokidar@3.4.3

## setup GIT ignore list
 .gitignore=> 
    node_modules
## setup server in INDEX.JS 
const jsonServer = require("json-server");
const server = jsonServer.create();
const router = jsonServer.router("db.json");

const middlewares = jsonServer.defaults();
const port = process.env.PORT || 3000;

server.use(middlewares);
server.use(router);

server.listen(port);

## setup start process in package.json
npm init -y //creates package.json
add this line bellow to the scripts array
"start": "node index.js"

"scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "node index.js"
  },

## upload to GITHUB
## setup RENDER.COM
NEW=> WEB SERVICES
