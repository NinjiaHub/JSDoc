# Including README

有两种方式将 `README` 文件合并到文档中：

* 1、在包含 JavaScript 文件的源路径之后，加上包含名为 `README.md` 的 markdown 格式的文件。JSDoc 将会使用源路径中找到的第一个 `README.md` 文件。
* 2、使用命令行选项 `-R/--readme` 指定 `README` 文件的路径。该选项在 **JSDoc 3.3.0** 及其之后的版本中有效。使用该选项时，`README` 文件可以具有任意的命名以及扩展名，但是必须以 markdown 格式书写。

命令行选项 `-R/--readme` 的优先级高于源路径。如果使用了 `-R/--readme` 选项，JSDoc 会忽略源路径中的 `README` 文件。

如果使用 JSDoc 的默认模版，`README` 文件的内容将被渲染为 HTML 格式并保存在生成文档的 `index.html` 文件中。

## 例子

**源码路径中包含 README 文件**

```javascript
jsdoc path/to/js path/to/readme/README.md
```

**使用 -R/--readme 选项**

```javascript
jsdoc --readme path/to/readme/README path/to/js
```

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - Including a README File](http://usejsdoc.org/about-including-readme.html "Including a README File")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>