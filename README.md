# Setup of react dependencies, packages and configs

- Contains all the required packages that is to be installed for a scalabale web application, from setup to testing the application.

## 1.  Getting started - Setup tools
```
- npm init
- npm install -D parcel                    [Bundler]
- npm i react
- npm i react-dom
- npm i react-router-dom                   [for routing]
  ```
## 2. Running the application
```
- npx parcel index.html / npm start       [for development]
- npm run build                           [for production]
```
## 3. Tailwind CSS [with parcel]
```
- npm install tailwindcss @tailwindcss/postcss
- for configs follow -[https://tailwindcss.com/docs/installation/framework-guides/parcel]
```
## 4. Redux Toolkit
```
- npm i -D @reduxjs/toolkit
- npm i -D react-redux
```
## 5. React Testing Library
```
- npm i -D @testing-library/react
- npm install -D jest
- npm install --save-dev babel-jest @babel/core @babel/preset-env
  ```
- configure Babel
  - in src create babel.config.js and add the following

```
  module.exports = {
  presets: [
    ['@babel/preset-env', {targets: {node: 'current'}}],
    '@babel/preset-typescript',
  ],
  };
  ```
- configure parcel config to disable default Babel transpilation
  
  ...
  
```
-  npx jest --init
```

-Render a component inside jest for testing purposes

```
- npm i -D @testing-library/jest-dom
```
