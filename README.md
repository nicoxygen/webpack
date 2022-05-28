# Installer Bootstrap

## import bootstrap
npm install bootstrap jquery popper.js --save
npm install exports-loader --save-dev
npm install autoprefixer css-loader node-sass postcss-loader sass-loader style-loader --save-dev

npm update

### tuto complet
[tuto complet](https://stevenwestmoreland.com/2018/01/how-to-include-bootstrap-in-your-project-with-webpack.html)

# Installer jquery
## dans webpack.prod.js et webpack.dev.js

var webpack = require("webpack");
 plugins: [
    new webpack.ProvidePlugin({
        $: "jquery",
        jQuery: "jquery"
    })
 ],

## installer jquery

[astuce sur cette page](https://stackoverflow.com/questions/28969861/managing-jquery-plugin-dependency-in-webpack)

npm i jquery --save

## dans index.js ajoute

```bash
import $ from 'jquery';
window.jQuery = $;
window.$ = $;
```

# Installer webp

https://www.npmjs.com/package/imagemin-webp-webpack-plugin

```bash
npm install imagemin-webp-webpack-plugin --save-dev
```

à intégrer dans webpack.prod.js:

```yaml
const ImageminWebpWebpackPlugin= require("imagemin-webp-webpack-plugin");
```

et

```yaml
** new ImageminPlugin({ test: /\.(jpe?g|png|gif|svg)$/i }), **
new ImageminWebpWebpackPlugin({
```

config: [{ test: /.(jpe?g|png|gif)/, options: { quality: 75 } }], overrideExtension: true, detailedLogs: false, silent: false, strict: true }),
