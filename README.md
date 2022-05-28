# Installer Bootstrap

## import bootstrap

```bash
npm install bootstrap jquery popper.js --save
npm update
```

### tuto complet
[tuto complet](https://stevenwestmoreland.com/2018/01/how-to-include-bootstrap-in-your-project-with-webpack.html)

# Installer jquery
## dans webpack.prod.js et webpack.dev.js

```yaml
const webpack = require("webpack");
....
 plugins: [
    new webpack.ProvidePlugin({
        $: "jquery",
        jQuery: "jquery"
    })
 ],
 ```

## installer jquery

[astuce sur cette page](https://stackoverflow.com/questions/28969861/managing-jquery-plugin-dependency-in-webpack)

```yaml
npm i jquery --save
```

## dans index.js ajoute

```bash
import $ from 'jquery';
window.jQuery = $;
window.$ = $;
```

# Installer webp

[webpack webp](https://www.npmjs.com/package/imagemin-webp-webpack-plugin)

```bash
npm install imagemin-webp-webpack-plugin --save-dev
```

***à intégrer dans webpack.prod.js:***

```yaml
const ImageminWebpWebpackPlugin= require("imagemin-webp-webpack-plugin");
```

et

```yaml
** new ImageminPlugin({ test: /\.(jpe?g|png|gif|svg)$/i }), **
new ImageminWebpWebpackPlugin({
```

config: [{ test: /.(jpe?g|png|gif)/, options: { quality: 75 } }], overrideExtension: true, detailedLogs: false, silent: false, strict: true }),

# Installer fontawesome

[instruction]([https://cdnjs.cloudflare.com/ajax/libs/ionicons/4.5.6/css/ionicons.min.css](https://bytepursuits.com/using-webpack-5-with-font-awesome-5))
