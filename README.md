# README 📖

**注：文档正在翻译中，译者会逐步填充。**

## 阅读顺序 🕊️

* Index
	* 起步
		* [使用 JSDoc 3 添加文档注释](./docs/start/about-getting-started.html "Getting started using JSDoc 3") - 快速学习使用 JSDoc 给 JavaScript 添加文档注释
		* [License](https://ninjiahub.github.io/JSDoc/docs/start/about-license "license information for JSDoc 3") - JSDoc 3 软件许可
		* [package.json](https://ninjiahub.github.io/JSDoc/docs/start/about-including-package "How to show package details in your documentation.") - 如何在文档中添加 `package.json`
		* [README](https://ninjiahub.github.io/JSDoc/docs/start/about-including-readme "How to include a README file in your documentation.") - 如何在文档中添加 `README`
	* JSDoc 示例
		* [ES 2015 类](https://ninjiahub.github.io/JSDoc/docs/examples/es-2015-classes "ES 2015 classes") - 如何给 ECMAScript 2015中的类添加JSDoc注释
		* [ES 2015 模块](https://ninjiahub.github.io/JSDoc/docs/examples/es-2015-modules "ES 2015 Modules") - 如何给 ECMAScript 2015中的模块添加JSDoc注释
	* 块标签(Block Tags)
		* [@abstract](https://ninjiahub.github.io/JSDoc/docs/tags/abstract "tag @abstract")(同义词：@virtual) - 该标识符必须被继承者实现(或者复写)
		* [@access](https://ninjiahub.github.io/JSDoc/docs/tags/access "tag @access") - 指定成员的访问等级(private, package-private, public, 或者 protected)
		* [@alias](https://ninjiahub.github.io/JSDoc/docs/tags/alias "tag @alias") - 给一个变量添加别名
		* [@async](https://ninjiahub.github.io/JSDoc/docs/tags/async "tag @async") - 标示一个方法是异步的
		* [@augments](https://ninjiahub.github.io/JSDoc/docs/tags/augments "tag @augments")(同义词：@extends) - 标记一个标识符继承自、添加到父标识符
		* [@augments](https://ninjiahub.github.io/JSDoc/docs/tags/augments "tag @augments") - 标记某项的作者
		* [@borrows](https://ninjiahub.github.io/JSDoc/docs/tags/borrows "tag @borrows") - 一个对象引用另外一个对象的文档注释
		* [@class](https://ninjiahub.github.io/JSDoc/docs/tags/class "tag @class")(同义词：@constructor) - 该方法期望被 `new` 关键字进行构造调用
		* [@classdesc](https://ninjiahub.github.io/JSDoc/docs/tags/classdesc "tag @classdesc") - 使用下面的文字描述整个类
		* [@constant](https://ninjiahub.github.io/JSDoc/docs/tags/constant "tag @constant")(同义词：@const) - 将一个对象标记为常量
		* [@constructs](https://ninjiahub.github.io/JSDoc/docs/tags/constructs "tag @constructs") - 该方法是前面类的构造器函数
		* [@default](https://ninjiahub.github.io/JSDoc/docs/tags/default "tag @default")(同义词：@defaultvalue) - 标记默认值
		* [@enum](https://ninjiahub.github.io/JSDoc/docs/tags/enum "tag @enum") - 标记一组相关的属性
		* [@event](https://ninjiahub.github.io/JSDoc/docs/tags/event "tag @event") - 标记事件
		* [@example](https://ninjiahub.github.io/JSDoc/docs/tags/example "tag @example") - 提供一个如何使用已标记项目的示例
		* [@exports](https://ninjiahub.github.io/JSDoc/docs/tags/exports "tag @exports") - 标记模块导出的成员属性
		* [@file](https://ninjiahub.github.io/JSDoc/docs/tags/event "tag @event")(同义词：@fileoverview, @overview) - 描述文件
		* [@fires](https://ninjiahub.github.io/JSDoc/docs/tags/fires "tag @fires")(同义词：@func, @method) - 描述该方法会触发的事件
		* [@function](https://ninjiahub.github.io/JSDoc/docs/tags/function "tag @function")(同义词：@emits) - 描述一个函数或者方法
		* [@global](https://ninjiahub.github.io/JSDoc/docs/tags/global "tag @global") - 标记一个全局对象
		* [@ignore](https://ninjiahub.github.io/JSDoc/docs/tags/ignore "tag @ignore") - 使一个标识符不出现在文档中
		* [@inner](https://ninjiahub.github.io/JSDoc/docs/tags/inner "tag @inner") - 标记一个内部对象
		* [@kind](https://ninjiahub.github.io/JSDoc/docs/tags/kind "tag @kind") - 标识一个可以被其他标识符实现的接口
		* [@kind](https://ninjiahub.github.io/JSDoc/docs/tags/kind "tag @kind")(同义词：@emits) - 标示标识符的种类
		* [@lends](https://ninjiahub.github.io/JSDoc/docs/tags/lends "tag @lends") - 给对象字面量中的属性添加文档注释，就像这些属性属于一个给定名称的标识符一样
		* [@license](https://ninjiahub.github.io/JSDoc/docs/tags/license "tag @license") - 标识该项目中代码使用的软件许可
		* [@listens](https://ninjiahub.github.io/JSDoc/docs/tags/listens "tag @listens") - 列出一个标识符监听的所有事件
		* [@member](https://ninjiahub.github.io/JSDoc/docs/tags/member "tag @member") - 标记一个成员
		* [@mixes](https://ninjiahub.github.io/JSDoc/docs/tags/mixes "tag @mixes") - 该对象会将另外一个对象的所有成员混入
		* [@mixin](https://ninjiahub.github.io/JSDoc/docs/tags/mixin "tag @mixin") - 标记一个混入对象
		* [@name](https://ninjiahub.github.io/JSDoc/docs/tags/name "tag @name") - 标记对象的名字
		* [@package](https://ninjiahub.github.io/JSDoc/docs/tags/package "tag @package") - 标记一个标识符是 **包私有的**
		* [@readonly](https://ninjiahub.github.io/JSDoc/docs/tags/readonly "tag @readonly") - 标示该标识符是只读的
		* [@returns](https://ninjiahub.github.io/JSDoc/docs/tags/returns "tag @returns")(同义词：@return) - 给函数的返回值添加文档注释
		* [@see](https://ninjiahub.github.io/JSDoc/docs/tags/see "tag @see") - 引用其他文档注释
		* [@since](https://ninjiahub.github.io/JSDoc/docs/tags/since "tag @since") - 标记该特性是在哪个版本加入的
		* [@since](https://ninjiahub.github.io/JSDoc/docs/tags/static "tag @static") - 标记一个静态成员
		* [@summary](https://ninjiahub.github.io/JSDoc/docs/tags/summary "tag @summary") - 简短版的完整描述
		* [@this](https://ninjiahub.github.io/JSDoc/docs/tags/this "tag @this") - 关键字 'this' 的指向
		* [@throws](https://ninjiahub.github.io/JSDoc/docs/tags/throws "tag @throws")(同义词：@exception) - 标记可能抛出的异常
		* [@todo](https://ninjiahub.github.io/JSDoc/docs/tags/todo "tag @todo") - 标记未完成的任务
		* [@typedef](https://ninjiahub.github.io/JSDoc/docs/tags/typedef "tag @typedef") - 标记自定义类型
		* [@version](https://ninjiahub.github.io/JSDoc/docs/tags/version "tag @version") - 标记一个项的版本号
		* [@yields](https://ninjiahub.github.io/JSDoc/docs/tags/yields "tag @yields")(同义词：@yield) - 给 generator 函数的生成值添加文档注释
	* 内联标签(inline tags)
		* [@inline-link](https://ninjiahub.github.io/JSDoc/docs/tags/inline-link "tag @inline-link")(同义词： {@linkcode}, {@linkplain}) - 在文档内链接到其他项的文档

## 声明 ⛰️

该仓库所有文件翻译自[JSDoc英文文档](http://usejsdoc.org/index.html)，如有版权问题请联系作者。

侵删。

如内容有错误，敬请斧正。

译者邮箱：<web.taox@gmail.com>

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>
