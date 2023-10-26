@vechain/repo-config

to share prettier, eslint and tsconfig between repos

## import

import it in `package.json` devDependencies:

```json
"devDependencies": {
    "@vechain/repo-config": "https://github.com/vechainfoundation/repo-config", // main branch
},
```

you can also import a specific tag

```json
"devDependencies": {
    "@vechain/repo-config": "https://github.com/vechainfoundation/repo-config#v0.0.1", // tag v0.0.1
},
```

or a specific branch

```json
"devDependencies": {
    "@vechain/repo-config": "https://github.com/vechainfoundation/repo-config#custom-branch", // branch "custom-branch"
},
```

## prettier configuration

you can use it in your `prettier.config.js`:

```js
const Config = require('@vechain/repo-config');

module.exports = Config.Prettier;
```

## es-lint configuration

you can use it in your `.eslintrc.js`:

```js
const Config = require('@vechain/repo-config');
module.exports = Config.EslintLibrary; // for typescript libraries
```

you can also use others configs like

```js
    module.exports = Config.EslintReactNative; // for react native projects
    module.exports = Config.EslintReact; // for react projects
```


## tsconfig configuration

you can use it in your `tsconfig.json`:

```json
{
    "extends": "@vechain/repo-config/src/tsconfig/base.json" // this is a basic configuration
}
```

you can also use more specific configs like

```json
    "extends": "@vechain/repo-config/src/tsconfig/react-library.json" // for react libraries
    "extends": "@vechain/repo-config/src/tsconfig/react.json" // for react projects
```