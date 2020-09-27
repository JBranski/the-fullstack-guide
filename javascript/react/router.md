# React Router

## Installing React Router

`npm install react-router-dom`

_Note: other versions of router exist for  different purposes_

## Updating the index.js file

```jsx
  import React from 'react';
  import ReactDOM from 'react-dom';
+ import { BrowserRouter } from "react-router-dom";
  import './index.css';
  import App from './App';

  ReactDOM.render(
-   <App />,
+   <BrowserRouter>
+     <App />
+   </BrowserRouter>,
    document.getElementById('root')
  );
  ```
