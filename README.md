# react-app-rewire-yaml-flat

Add [yaml-flat-loader](https://github.com/akameco/yaml-flat-loader) together with
[json-loader](https://github.com/webpack-contrib/json-loader) to your
[create-react-app](https://github.com/facebookincubator/create-react-app) via
[react-app-rewired](https://github.com/timarney/react-app-rewired).

## Installation

```
yarn add --dev react-app-rewire-yaml-flat
```

OR

```
npm install --save-dev react-app-rewire-yaml-flat
```

## Usage

In your react-app-rewired configuration:
```js
/* config-overrides.js */

const rewireYamlFlat = require('react-app-rewire-yaml-flat');

module.exports = function override(config, env) {
    // ...
    config = rewireYamlFlat(config, env);
    // ...
    return config;
}
```

In your React application:
```js
import data from './data.yaml'

const App = () => (
  <div>
    {data['key.subkey']}
  </div>
);
```
