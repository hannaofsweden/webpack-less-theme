# webpack-less-theme-plugin

Less theme variable injection by reference.

Works with HMR without generating duplicate CSS code.

## Installation

```bash
$ npm i webpack-less-theme --save-dev
```

## Usage

Add to webpack config.

```javascript
// webpack.config.js
const LessThemePlugin = require('webpack-less-theme');

module.exports = {
  ...,
  plugins: [
    new LessThemePlugin({ theme: './blue.less' }),
  ],
};
```

```less
// blue.less
@primary-color: blue;
```

## Options

- `test` - webpack's [Condation.rule](https://webpack.js.org/configuration/module/#condition). Default is `/\.less$/`.
- `theme` - less theme file.
- `cwd`  - Current working dir.

## License

MIT
