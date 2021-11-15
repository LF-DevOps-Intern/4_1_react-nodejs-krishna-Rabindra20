### React JS:
 - Install React.js.
 - Creating a React Application and print message "Hello React.js"
 - Change the default port 3000 to 3001
 Steps:
### Install React.js.<br/>
check node version
    <pre>node -v</pre><br/>

![node version](https://user-images.githubusercontent.com/53372486/141771666-9614a20e-a541-4536-920c-fe0755db7f08.png)<br/>
    <pre>sudo npm -g install create-react-app</pre><br/>

![install create react app](https://user-images.githubusercontent.com/53372486/141771700-afbeb883-f2d1-4749-adcd-ee9db0988af2.png)<br/>

  <pre>create-react-app devops-internship</pre><br/>

![create devops](https://user-images.githubusercontent.com/53372486/141771712-772f733c-5c87-4b55-bdec-52fac31c1232.png)<br/>

  <pre>cd devops-internship</pre><br/>
    <pre>npm start</pre><br/>

![react start in 3000](https://user-images.githubusercontent.com/53372486/141771747-0a5261a7-0953-4a3c-b732-e6f342ef842f.png)<br/>

![web running in 3000](https://user-images.githubusercontent.com/53372486/141771757-633854a8-ff0e-4208-9dc3-a7de036d628b.png)<br/>

### Change the default port 3000 to 3001  <br/>
 we can change port from package.json or .env<br/>
   <pre>"scripts": {<br/>
    "start": “PORT=8000 react-scripts start",<br/>
    "build": "react-scripts build",<br/>
    "test": "react-scripts test --env=jsdom",<br/>
    "eject": "react-scripts eject"<br/>
  }</pre><br/>
   OR 
   create .env file and add below line
    <pre>PORT=8000</pre><br/>

![port 3001](https://user-images.githubusercontent.com/53372486/141771778-745a5d07-e80e-4de2-8fda-95a3e73a8576.png)<br/>

![running3001](https://user-images.githubusercontent.com/53372486/141771794-e35e38a1-cf7e-4167-9f9c-19e0fbbfa33a.png)<br/>
### Creating a React Application and print message "Hello React.js"
<pre>cd src</pre><br/>
<pre>nano App.js</pre><br/>
Add message in App.js
<pre>import './App.css';
function App() {
  return (
    <div className="App">
      <header className="App-header">
        <h1>Hello React.js</h1>
      </header>
    </div>
  );
}
export default App;</pre><br/>

![displaymessage](https://user-images.githubusercontent.com/53372486/141771813-371f878a-b361-409c-bbd7-bfd178dac967.png)
