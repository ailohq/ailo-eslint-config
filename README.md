# Introduction

ESLint config to be used in some of our projects, that includes recommended rules of the following plugins:

- eslint-config-airbnb-typescript
- eslint-plugin-react (optionally)
- eslint-plugin-react-hooks (optionally)
- eslint-plugin-jsx-a11y (optionally)
- eslint-config-prettier (we assume that you `prettier` your files on your own, outside eslint)
- eslint-import-resolver-typescript
- eslint-plugin-import
- eslint-plugin-jest
- eslint-plugin-promise
- eslint-plugin-unicorn

With some slight modifications to some of the defaults on our side.

# Usage

1. Setup eslint as you would normally do.

2. `npm install -D github:ailohq/ailo-eslint-config`

3. Extend the config as in the following examples:

   ## Node.js

   ```js
   // .eslintrc.js
   module.exports = {
     parserOptions: {
       project: ["./tsconfig.json"],
     },

     extends: [require.resolve("ailo-eslint-config/configs/node")],

     env: {
       browser: true,
       jest: true,
     },
   };
   ```

   ## React

   ```js
   // .eslintrc.js
   module.exports = {
     parserOptions: {
       project: ["./tsconfig.json"],
     },

     extends: [require.resolve("ailo-eslint-config/configs/react-native")],

     env: {
       browser: true,
       jest: true,
     },
   };
   ```
