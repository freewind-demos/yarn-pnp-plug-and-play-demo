Yarn PnP (Plug'N'Play) Demo
===========================

在yarn中开启`pnp`后，yarn install时，将不会在当前目录下生成node_modules，而是通过link的方式，直接使用yarn cache中的包，
节省了空间。

需要在`package.json`中打开：

```
"installConfig": {
  "pnp": true
}
```

然后运行:

```
yarn
```

可以看到项目下并没有生成`node_modules`，但是`yarn list`却可以看到依赖关系。

然而，webpack等并不认识，需要一些额外的插件。

更麻烦的是，webstorm也不认，typing会有问题。

所以看起来现在还不太好用。
