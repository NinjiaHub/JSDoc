# Including a Package File

`package.json` 文件包含对项目文档有用的信息，比如项目名称、项目当前的版本号等。JSDoc 会在生成文档的过程中使用项目中 `package.json` 文件中记录的信息。比如，默认模版会在文档中显示项目名称以及版本号。

有两种方式将 `package.json` 文件合并到文档中：

* 1、在包含 JavaScript 文件的源路径之后，加上包含名为 `package.json` 文件的源路径。JSDoc 将会使用源路径中找到的第一个 `package.json` 文件。
* 2、使用命令行选项 `-P/--package` 指定 `package.json ` 文件的路径。该选项在 **JSDoc 3.3.0** 及其之后的版本中有效。

命令行选项 `-P/--package` 的优先级高于源路径。如果使用了 `-P/--package` 选项，JSDoc 会忽略源路径中的 `package.json` 文件。

`package.json` 文件必须遵循 [npm 中 package.json 文件的格式](https://docs.npmjs.com/files/package.json)。

## 例子

**源码路径中包含 package.json 文件**

```javascript
jsdoc path/to/js path/to/package/package.json
```

**使用 -P/--package 选项**

```javascript
jsdoc --package path/to/package/package-docs.json path/to/js
```

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - Including a Package File](http://usejsdoc.org/about-including-package.html "Including a Package File")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>