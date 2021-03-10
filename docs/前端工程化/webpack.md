# webpack

一个模块打包工具，将多个模块打包到生成一个最终的bundle.js

webpack主要由  `entry`,  `output`,  `loaders`,  `plugins`,  `chunk` 组成

webpack只能处理js文件，若要处理非js文件，则需要通过一些 `loader` 来兼容

`loader` 的主要作用：解决代码的兼容性；将无法处理的非js文件，处理成webpack能够处理的模块

`plugins` 的主要作用：代码的优化，提取精华（去重），压缩处理，对webpack功能的扩展

`chunk` 是webpack 4 的`Code Splitting` 产物，抛弃了webpack3的`CommonsChunkPlugin`,它最大的特点就是配置简单，当你设置 `mode` 是 `production`，那么 webpack 4 就会自动开启 `Code Splitting`，可以完成将某些公共模块去重，打包成一个单独的`chunk`。

### entry

用来指定构建入口

### output

包含 `filename` 和 `path` 两个字段

* filename - 输出文件名

* path -	​输出路径	

### rules

对象数组

对象中包含以下属性 :

* test - 值为正则，用来匹配希望被找到的文件类型的后缀

* includes - 值为路径，用来指定在哪些文件夹下需要去找指定后缀的文件

* use - 对象，包含以下属性：
    - loader - 指定使用的loader
    - options - loader的选项

### plugin

需要先安装插件之后，再来添加对应的字段。

### mode

可选值为：`development` , `production` , `none`

`development` 就是开发模式

`production` 就是生产模式