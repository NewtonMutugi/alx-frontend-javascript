# 0x00. ES6 Basics

![alt text](image.png)

## Resources

**Read or watch:**

- [ECMAScript 6 - ECMAScript 2015](https://intranet.hbtn.io/rltoken/3Zp3zg8J9)
- [Statements and declarations](https://intranet.hbtn.io/rltoken/3Zp3zg8J9)
- [Arrow functions](https://intranet.hbtn.io/rltoken/3Zp3zg8J9)
- [Default parameters](https://intranet.hbtn.io/rltoken/3Zp3zg8J9)
- [Rest parameter](https://intranet.hbtn.io/rltoken/3Zp3zg8J9)
- [Demistyfying ES6 Generators](https://intranet.hbtn.io/rltoken/3Zp3zg8J9)

## Learning Objectives

At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

- What ES6 is
- New features introduced in ES6
- The difference between a constant and a variable
- Block-scoped variables
- Arrow functions and function parameters default to them
- Rest and spread function parameters
- String templating in ES6
- Object creation and their properties in ES6
- Iterators and for-of loops

## Requirements

### General

- All your files will be interpreted on Ubuntu 18.04 LTS using NodeJS 12.11.x
- All your files should end with a new line
- The first line of all your files should be exactly #!/usr/bin/node
- A README.md file, at the root of the folder of the project, is mandatory
- Your code should use the js extension
- Your code will be tested using Jest
- Your code will be analyzed using the linter ESLint along with specific rules that we’ll provide
- All of your functions must be exported

## Setup

### Install NodeJS 12.11.x

(in your home directory):

```sh
$ curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
$ sudo bash nodesource_setup.sh
$ sudo apt install nodejs
```

```sh
$ nodejs -v
v12.11.1
$ npm -v
6.11.3
```

### Install Jest, Babel, and ESLint

in your project directory, Install Jest, Babel, and ESLint by using the supplied `package.json` and `npm install`

## Configuration Files

Add the files below to yout project directory

### `package.json`

```json
{
  "scripts": {
    "test": "jest",
    "dev": "npx babel-node"
  },
  "devDependencies": {
    "@babel/core": "^7.6.0",
    "@babel/node": "^7.8.0",
    "@babel/preset-env": "^7.8.2",
    "eslint": "^6.6.0",
    "eslint-config-airbnb-base": "^14.0.0",
    "eslint-plugin-import": "^2.18.2",
    "jest": "^24.9.0"
  }
}
```

### `babel.config.js`

```js
module.exports = {
  presets: [
    [
      '@babel/preset-env',
      {
        targets: {
          node: 'current',
        },
      },
    ],
  ],
};
```

### `.eslintrc.js`

```js
module.exports = {
  env: {
    browser: false,
    es6: true,
    jest: true,
    node: true,
  },
  extends: 'airbnb-base',
  parserOptions: {
    ecmaVersion: 2018,
  },
  rules: {
    'no-console': 'off',
    'no-shadow': 'off',
    'no-restricted-syntax': ['error', 'LabeledStatement', 'WithStatement'],
  },
};
```
