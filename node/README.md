### Node JS:
 - Install Node js on local VM.
 - Create 2 API's running on ports 6080 and 7080 with mesaages "Hello Node JS" and "Node JS installed successfully" respectively.
 -  Install pm2 tool and create 4 clusters of bothe Node's.
 - Delete all 4 clusters one-by-one
 Steps:
 ### Install Node js on local VM.
 ### Installing Node.js with Apt Using a NodeSource personal package archive
 <br/>
 <pre>sudo apt  install curl</pre> <br/>
<pre>curl -sL https://deb.nodesource.com/setup_16.x -o nodesource_setup.sh</pre><br/>
<pre>nano nodesource_setup.sh</pre><br/>
<pre>sudo apt install nodejs</pre><br/>
<pre>node -v</pre><br/>
16.13.0<br/>

![node version](https://user-images.githubusercontent.com/53372486/141770536-b944f045-ae98-4fc4-ab0e-55307bb50703.png)
<br/>
<pre>npm -version</pre><br/>
8.1.0<br/>

[npm version](https://user-images.githubusercontent.com/53372486/141770544-6ca11dd0-4b84-41af-86de-8954aad8fc04.png)
<br/>
### Create 2 API's running on ports 6080 and 7080 with mesaages "Hello Node JS" and "Node JS installed successfully" respectively.
<br/>
    <pre> mkdir node</pre><br/>
<pre>cd node</pre><br/>
Install package<br/>
<pre>npm init</pre><br/>
package name: (node) test<br/>
version: (1.0.0) <br/>
description: <br/>
entry point: (index.js) <br/>
test command: <br/>
git repository: <br/>
keywords: <br/>
author: rabindra<br/>
license: (ISC) <br/>
About to write to /home/rabindra/node/package.json:<br/>

{<br/>
  "name": "test",<br/>
  "version": "1.0.0",<br/>
  "description": "",<br/>
  "main": "index.js",<br/>
  "scripts": {<br/>
    "test": "echo \"Error: no test specified\" && exit 1"<br/>
  },
  "author": "rabindra",<br/>
  "license": "ISC"
}<br/>
Add message and change port number inside 6080.js

<pre>sudo nano 6080.js</pre><br/>

<pre>var http = require('http');<br/>
http.createServer(function(req,res){<br/>
 res.writeHead(200, { 'Content-Type': 'text/plain' });<br/>
 res.end('Hello Node JS');<br/>
}).listen(6080);<br/>
console.log('Server started on localhost:6080; press Ctrl-C to terminate...!');</pre>
<br/>

![port6080](https://user-images.githubusercontent.com/53372486/141770599-30a839ce-b4ca-4b43-9a95-122ededdb060.png)<br/>

Run 6080.js<br/>
<pre>node 6080.js</pre><br/>

![runing6080port](https://user-images.githubusercontent.com/53372486/141770608-bd02a96a-b761-43fc-b8a3-f85bc537ba47.png)<br/>

<pre>sudo nano 7080.js</pre><br/>

![port 70890](https://user-images.githubusercontent.com/53372486/141770592-8bd5bb11-1014-44e3-ab99-308b441261ff.png)<br/>


<pre>node 7080.js</pre><br/>

![runing7080port](https://user-images.githubusercontent.com/53372486/141770633-23e14afd-7bf8-46eb-9bdb-aa59d9f86c3e.png)
<br/>

###  Install pm2 tool and create 4 clusters of bothe Node's.
<br/>
install pm2 via NPM<br/>
<pre>sudo npm i -g pm2</pre><br/>

![pm2 version](https://user-images.githubusercontent.com/53372486/141771215-c572115a-b441-4d1f-88fc-897f2dbdfa94.png)<br/>

Run PM2<br/>
<pre>sudo pm2 start 6080.js</pre><br/>
start an application in 4 cluster mode using the -i flag<br/>
<pre>sudo pm2 start 6080.js -i 4</pre><br/>

![cluster6080](https://user-images.githubusercontent.com/53372486/141771222-6a37ae51-6dc3-43cb-aeb8-c6552c12b1b5.png)<br/>

<pre>sudo pm2 start 7080.js -i 4</pre><br/>

![pm2cluster](https://user-images.githubusercontent.com/53372486/141771248-7ce6df3c-df8c-439d-ab1e-595137eccea9.png)
<br/>
### Delete all 4 clusters one-by-one<br/>
Deleting the node with id from pm2<br/>
<pre>sudo pm2 delete 0</pre><br/>

![deletecluster0](https://user-images.githubusercontent.com/53372486/141771257-80f6582b-6778-450f-b1bd-9db6d58d8b61.png)
<br/>
<pre>sudo pm2 delete 1</pre><br/>

![deletecluster1](https://user-images.githubusercontent.com/53372486/141771264-9d87fcdf-79ea-4fd7-8c39-fc963fd1462a.png)
<br/>
<pre>sudo pm2 delete 2</pre><br/>
<pre>sudo pm2 delete 3</pre><br/>
