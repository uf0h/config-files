# Webpack

An example implementation is below.
```console
webpack-demo
  |- /dist
    |- main.js
    |- main.css
    |- index.html
  |- /src
    |- /static
      |- style.css
      |- index.html
    |- index.js
+ |- webpack.common.js
+ |- webpack.dev.js
+ |- webpack.prod.js
  |- package.json
```

## Getting Started

Initialize node project

```console
npm init -y
```

Install webpack

```console
npm i -D webpack webpack-cli webpack-merge webpack-dev-server
```

Install webpack plugins and loaders

```console
npm i -D clean-webpack-plugin html-webpack-plugin css-loader \
         mini-css-extract-plugin optimize-css-assets-webpack-plugin \
         terser-webpack-plugin
```

Add the following to `package.json` scripts

```console
"start": "webpack-dev-server --open --config webpack.dev.js",
"build": "webpack --config webpack.prod.js"
```

Grab webpack config files

```console
for x in {'common','dev','prod'}; \
do wget https://raw.githubusercontent.com/uf0h/config-files/master/webpack/webpack.${x}.js; done
```
