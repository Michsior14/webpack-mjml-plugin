<h1 align="center">Webpack MJML Plugin</h1>

<p align="center">Webpack <a href="https://mjml.io">MJML</a> Plugin for compiling MJML files.</p>

<p align="center">
  <a href="https://github.com/prettier/prettier">
    <img src="https://img.shields.io/badge/code_of-conduct-ff69b4.svg" alt="Prettier" />
  </a>
  <a href="https://snyk.io/test/github/matteobertoldo/mjml-webpack-plugin?targetFile=package.json">
    <img src="https://snyk.io/test/github/matteobertoldo/mjml-webpack-plugin/badge.svg?targetFile=package.json" alt="Known Vulnerabilities" />
  </a>
  <a href="https://app.travis-ci.com/matteobertoldo/mjml-webpack-plugin">
    <img src="https://app.travis-ci.com/matteobertoldo/mjml-webpack-plugin.svg?branch=master" alt="Travis CI Build">
  </a>
  <a href="https://www.npmjs.com/package/mjml-webpack-plugin">
    <img src="https://img.shields.io/npm/v/mjml-webpack-plugin.svg" alt="NPM Package Version" />
  </a>
</p>

---

## Installation :gift:

```sh
npm install webpack-mjml-plugin
```

## Usage :joystick:

In your `webpack.config.js` simply:

```javascript
const MJMLPlugin = require('webpack-mjml-plugin');

module.exports = {
  // ...
  plugins: [
    new MJMLPlugin('src/to/mjml', {
      extension: '.html',
      outputPath: path.resolve(__dirname, 'dist/to/mjml')
    });
  ]
};
```

## API :bee:

The plugin supports all `options` that can be found in [this documentation](https://documentation.mjml.io/#inside-node-js).

```js
// webpack.config.js

module.exports = {
  plugins: [
    new MJMLPlugin(inputPath, {
      extension: options.extension,
      outputPath: options.outputPath,
      // MJML options (https://documentation.mjml.io/#inside-node-js)
      filePath: path.resolve(__dirname, 'dist/to/mjml'),
      keepComments: false
    })
  ]
};
```

| Parameter            |   Type   |     Default     | Description                                         |
| -------------------- | :------: | :-------------: | --------------------------------------------------- |
| `inputPath`          | `string` |   `undefined`   | The path where `.mjml` files are located.           |
| `options.extensions` | `string` |     `.html`     | The default output extension.                       |
| `options.outputPath` | `string` | `process.cwd()` | The path where compiled files should be written to. |

## Contributing :busts_in_silhouette:

Please read [CONTRIBUTING.md](https://github.com/matteobertoldo/webpack-mjml-plugin/blob/main/CONTRIBUTING.md) for details on code of conduct, and the process for submitting pull requests.

## License :balance_scale:

[![npm](https://img.shields.io/npm/l/mjm-webpack-plugin.svg)](https://www.npmjs.com/package/mjm-webpack-plugin)

Webpack MJML Plugin is licensed under the MIT License - see the [LICENSE.md](https://github.com/matteobertoldo/mjml-webpack-plugin/blob/main/LICENSE) file for details.