# Setup of react dependencies, packages and configs

- Contains all the required packages that is to be installed for a scalabale web application, from setup to testing the application.

## 1.  Getting started - Setup tools
```
npm init
```
   - Bundler
```
npm install -D parcel
```
```                    
npm i react
npm i react-dom
```
  - For routing
```
npm i react-router-dom
```
              
## 2. Running the application
  - for development
```
npx parcel index.html / npm start
```
  - for production
```
npm run build                           
```

## 3. Tailwind CSS [with parcel]
```
npm install tailwindcss @tailwindcss/postcss
```
  -  for configs follow -[https://tailwindcss.com/docs/installation/framework-guides/parcel]

## 4. Redux Toolkit
```
npm i -D @reduxjs/toolkit
npm i -D react-redux
```

## 5. React Testing Library
```
npm i -D @testing-library/react
npm install -D jest
npm install --save-dev babel-jest @babel/core @babel/preset-env
  ```
- configure Babel
  - To make JSX work inside test case
  - in root create babel.config.js and add the following

```
  module.exports = {
  presets: [
    ['@babel/preset-env', {targets: {node: 'current'}}],
  ],
  };
  ```

- configure parcel config to disable default Babel transpilation
    - create .parcelrc in root and add the following
      
  ```
  {
  "extends": "@parcel/config-default",
  "transformers": {
    "*.{js,mjs,jsx,cjs,ts,tsx}": [
      "@parcel/transformer-js",
      "@parcel/transformer-react-refresh-wrap"
    ]
  }
  }
  ```

- initialize and configure the testing environment for jest.
```
npx jest --init
```

- JSDOM, it is a library which parses and interacts with assembled HTML just like broswer.
  - install JSDOM library (if using jest 28 and above, we need to manually install the library)
```
npm install -D jest-environment-jsdom
```

- to make JSX work inside jest, install-
```
npm i @babel/preset-react
```
- include it in the babel.config.js
```
    ['@babel/preset-react', { runtime: 'automatic' }],
```


- Render a component inside jest for testing purposes.
```
npm i -D @testing-library/jest-dom
```


### You are now good to go for building a SPA that is scalable and dynamic 🚀
