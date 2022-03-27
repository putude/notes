# Cara Setup PostCSS

**1. Init NPM**
`npm init -y`

**2. Download PostCSS**
`npm i -D postcss postcss-cli postcss-advanced-variables postcss-nested postcss-preset-env cssnano autoprefixer`

**3. Buat File postcss.config.js**
isinya sbb:

```js
module.exports = {
  parser: 'postcss-scss',
  plugins : [
    require('postcss-advanced-variables')(),
    require('postcss-nested'),
    require('postcss-preset-env')({stage: 1}),
    // require('postcss-import'),
    // require('cssnano'),
  
  ]
}
```

**4. Edit Package.json**

```json
{
  "name": "postcss",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "postcss:watch": "postcss src/style.css --dir css --watch"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "autoprefixer": "^10.4.4",
    "cssnano": "^5.1.5",
    "postcss": "^8.4.12",
    "postcss-advanced-variables": "^3.0.1",
    "postcss-cli": "^9.1.0",
    "postcss-import": "^14.1.0",
    "postcss-nested": "^5.0.6",
    "postcss-preset-env": "^7.4.3",
    "postcss-scss": "^4.0.3"
  }
}

```

pada bagian script

`"scripts": {
    "postcss:watch": "postcss src/style.css --dir css --watch"
  },`
