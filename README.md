# Myjam Prettier Config Base

This is a Prettier config that is used as a base in Myjam JavaScript (and TypeScript) projects Prettier config files.

## Requirements

- Node.js 8 or higher.
- Prettier 1.17.0 or higher.

## Installation

Add the package to `package.json` file `devDependencies`.

#### npm
```shell
npm i --save-dev https://git@github.com/my-jam-store/prettier-config
```

#### Yarn
```shell
yarn add --dev my-jam-store/prettier-config
```

## Usage

Use the Prettier config base with one of the following methods:

### `package.json` Method
Reference the config base in `package.json`:
```json
"prettier": "@myjam/prettier-config"
```
(You don't need to create a a Prettier config file after that.)

### Prettier Config JSON File Method
Create a Prettier config JSON file with the following config base reference inside it:
```json
"@myjam/prettier-config"
```

### Config Overwriting Method
This method allows to use the config base and also overwrite its options.  
Create a JS config file named `.prettierrc.js` and use the following example to extend the config base inside it:
```js
module.exports = {
  ...require('@myjam/prettier-config'),
  semi: false,
};
```
