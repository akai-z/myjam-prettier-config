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
Just reference the Prettier config base in `package.json`:
```json
"prettier": "@myjam/prettier-config"
```
(With this method you don't have to create a Prettier config file.)

### Prettier JSON Or YAML Config File Method
Create a [Prettier JSON or YAML config file](https://prettier.io/docs/en/configuration.html) (e.g. `.prettierrc`) with the following config base reference string inside it:
```json
"@myjam/prettier-config"
```
(You don't have to add anything else to the config file.)

### Config Overwriting Method
This method allows to extend (and use) the Prettier config base and overwrite its options.  
Create a [Prettier JS config file that supports `module.exports`](https://prettier.io/docs/en/configuration.html) (e.g. `.prettierrc.js`) and use the following example to extend the config base inside it:
```js
module.exports = {
  ...require('@myjam/prettier-config'),
  printWidth: 120,
  semi: false,
};
```
