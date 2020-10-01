# New React App

## Process

- `npx create-react-app project-name`
- `cd ./project-name`
- `npm install`
- `rm ./src/serviceWorker.js ./src/App.css ./src/logo.svg`
- Change the content of `./src/App.js` to the following:
```jsx
import React from 'react';

export default function App() {
  return (
    <main className='App'>
 
    </main>
  );
}
```
- Change the content of `./src/index.js` to the following:
```jsx
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';
import './index.css';

ReactDOM.render(<App />, document.getElementById('root'));
```
- ( optional ) `mkdir ./src/components ./src/utils`
