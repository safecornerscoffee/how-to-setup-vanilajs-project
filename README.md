# How to Set Up Vanilla.js Project
## Requirement
- [ ] Webpack
- [ ] Babel7
- [ ] Eslint
- [ ] Prettier
- [ ] Jest
- [ ] Configure Webstorm

## Babel7
```shell
npm install --save-dev @babel/core @babel/cli
npm install --save-dev @babel/preset-env
npm install --save core-js@3.12.1
```
.babelrc
```json
{
  "presets": [
    ["@babel/preset-env", {
      "useBuiltIns": "usage",
      "corejs": "3.12",
      "shippedProposals": true
    }]
  ]
}
```
>

## Eslint
```shell
npm install --save-dev eslint babel-eslint
npx eslint --init
```
.eslintrc.json
```json
{
  "parser": "babel-eslint",
  "rules": {
    "no-console": "off"
  }
}
```
> In Webstorm, Preferences > Languages & Frameworks > JavaScript > Code Quality Tools > ESLint > "Automatic ESLint configuration"

## Prettier
```shell
npm install --save-dev prettier
```
[.prettierrc](https://prettier.io/docs/en/configuration.html)
```json
{
  "trailingComma": "es5",
  "tabWidth": 4,
  "semi": false,
  "singleQuote": true
}
```
[Integrating with Linters](https://prettier.io/docs/en/integrating-with-linters.html)
```shell
npm install --save-dev eslint-config-prettier
```
add "prettier" to the "extends" array in your
`.eslintrc.json`
```
{
    "extends": [
        "eslint:recommended",
        "prettier"
    ]
}
```
> Preferences > Languages & Frameworks > JavaScript > Prettier > "On save"

## Configure Webstorm
1. Preferences > Languages & Frameworks > JavaScript > Code Quality Tools > ESLint > "Automatic ESLint configuration"
2. Preferences > Languages & Frameworks > JavaScript > Prettier > "On save"

