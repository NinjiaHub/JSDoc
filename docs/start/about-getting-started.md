# 使用 JSDoc 3 添加文档注释

## 内容列表 🕊️

* [新手入门](#getting-started)
* [给代码添加文档注释](#add-documentation)
* [生成文档站](#generate-website)

## <span id="getting-started">新手入门</span>

**JSDoc 3** 是一个 JavaScript 文档生成器，做用同 **javadoc** 或者 **phpDocumentor**。在源码中的对应部分添加文档注释，**JSDoc** 中的工具会扫描源码并生成一个集中展示文档注释的HTML网站。

## <span id="add-documentation">给代码添加文档注释</span>

**JSDoc** 的目的是给 JavaScript 应用或者库的 API 添加文档注释，它假设你想给 **模块**、**命名空间**、**类**、**方法** 以及 **方法参数** 等添加文档注释。

**JSDoc** 注释应该放在要添加文档注释的代码的前面。每个注释必须以 `/**` 开头，以便于 **JSDoc 解析器** 识别。以`/*`、`/***`或则多于三个 **`*`** 的写法都会被 JSDoc 解析器忽略。这个特性可以方便在使用中书写单纯的注释。

**最简单的文档注释仅仅是一句描述，如：**

```javascript
/** This is a description of the foo function. */
function foo() {
}
```
添加描述很简单 - 只需要在 **注释块** 中写想要写的描述就行了。

特殊的 **JSDoc 标签** 可以用来传达更多的信息。例如，如果一个函数是一个类的构造器，可以使用 **[@constructor](https://ninjiahub.github.io/JSDoc/docs/tags/constructor "tag constructor") 标签** 来标识。

**使用 JSDoc 标签来描述代码**

```javascript
/**
 * Represents a book.
 * @constructor
 */
function Book(title, author) {
}
```
还有更多标签可以用来添加更多信息，**[首页](https://ninjiahub.github.io/JSDoc)** 中有记录 JSDoc3 支持的所有标签列表。

**使用 JSDoc 标签添加更多信息：**

```javascript
/**
 * Represents a book.
 * @constructor
 * @param {string} title - The title of the book.
 * @param {string} author - The author of the book.
 */
function Book(title, author) {
}
```

## <span id="generate-website">生成文档站</span> 📃

如果你的代码中添加了文档注释，则可以使用 JSDoc 3 中的工具来为你的源码生成一个 HTML 网站来展示文档。

默认情况下，JSDoc 使用内建的模版将文档转换为 HTML。你可以通过修改模版来满足你的需求，甚至可以写一个全新的模版来代替内建模版。

**命令行中运行文档生成器**

```shell
> jsdoc book.js
```
上面的命令会在当前路径中创建一个 `out/` 目录。JSDoc 文档生成器生成的 HTML 文件都在该目录下。

**译注：jsdoc generator 不会根据 JavaScript 中的 `import` 或者 `require` 等对依赖的文件也生成相应的 HTML 页面，只会分析命令行中给出的文件进行分析，所以如果相对多个文件或者一个目录下的所有文件做处理，可以使用 `jsdoc index.js dirname/**/*` 这种形式来给所有的 `.js` 文件生成对应的 HTML 页面文件。**

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - Getting Started with JSDoc 3](http://usejsdoc.org/about-getting-started.html "Getting Started with JSDoc 3")。

如有版权问题请联系译者。

侵删。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>