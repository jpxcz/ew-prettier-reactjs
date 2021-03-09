# Prettier ReactJS

Adds the Prettier and ESLINT format that we use for ReactJS.  
If [husky](#husky-configuration) is added, then it will run on every new commit for the staged files

```sh
npm i --save-dev @ewmarkets/prettier-reactjs
```

## Prettier

```sh
# package.json
{
  ...
  "prettier": "@ewmarkets/prettier-reactjs",
  # to run it manually
  "scripts": {
    ...
    "prettier": "prettier --write \"./**/*.{js,jsx}\""
  }
}

```

## Husky Configuration
To run on every commit, you can modify the current `package.json`

```sh
# package.json
{
  ...
  "prettier": "@ewmarkets/prettier-reactjs",
  "scripts": {
    ...
    "prepare": "husky install",
    "prettier": "pretty-quick --staged", # remember to modify this!
  },
}

```

### Create a new file for running the husky hooks
```sh
$ echo "npm run prettier" > .husky/pre-commit && chmod +x .husky/pre-commit
$ npm install # this command is only to ensure the `prepare` script inside the package.json is run 
```
