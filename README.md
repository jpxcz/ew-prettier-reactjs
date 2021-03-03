# Prettier EWM ReactJS

Installs all dependencies needed for prettier in EWM

```sh
npm i --save-dev @ewmarkets/prettier-reactjs
```

## Edit your package.json file

```sh
# package.json
{
  ...
  "prettier": "@ewmarkets/prettier-reactjs",
  "scripts": {
    ...
    "prettier": "prettier --write \"./**/*.{js,jsx}\""
  }
}

```
