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
  
  ## Adding Routes
  
  To add a route, first import Route into the component
  
  `import { Route, Link } from 'react-router-dom';`
  
  Where you want the different components to render, you can add the `Route` components in
  
  ```jsx
  <main>
    <HomePage />
    <Route exact path="/" component={HomePage} />
    <Route path="/about" component={AboutPage} />
  </main>
  ```
  
  ### Linking to a Route
  
  ```jsx
    <Link to="/">
      Home
    </Link>
    <Link to="/about">
      About
    </Link>
  ```
