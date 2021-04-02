# 🚧 ReactJs-Electron template TypeScript 🚧

## 🚀 Creating project with typescript and webpack:

### 🔭 If you want a project with configured routes, you can run the command in your project's folder:

```
git clone https://github.com/diegobayerl/ReactJs-Electron.git create-react-electron
```
###  🔎 Or you can create from zero total:
```
yarn create electron-app my-new-app --template=typescript-webpack
```
```
npx create-electron-app my-new-app --template=typescript-webpack
```
In tsconfig.json, in the "compilerOptions" area add:
```json
"compilerOptions": {
  
  "jsx": "react"
}
```
## Add the React dependencies:
```
yarn add react react-dom
yarn add --dev @types/react @types/react-dom
```
```
npm install --save react react-dom
npm install --save-dev @types/react @types/react-dom
```
## Integrate React code:
create a file called app.tsx:
```javascript
import React from 'react';

import Routes from './routes';

function App(){
    return(
        <h1>Hello World</h1>
    );
};

export default App;
```
create a file called index.tsx:
```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import App from './app';

import './styles/global.css';

ReactDOM.render(
    <React.StrictMode>
        <App />
    </React.StrictMode>,
    document.getElementById('root'),
);
```
in the src/renderer.ts :
```javascript
// Add this to the end of the existing file
import './app';
```
To start the project:
```
yarn start
```
```
npm start
```
Building Distributables:
```
yarn make
```
```
npm run start
```
