# @license

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")

## <span id="syntax">语法</span>

`@license <identifier>`

## <span id="overview">概述</span>

`@license` 标签用来标明应用于代码中任意一部分的软件许可(**software license**)。

你可以使用任意语言来阐述你在使用的许可。如果你的代码使用 **标准开源许可**，最好从 [Software Package Data Exchange (SPDX) License List](https://spdx.org/licenses/) 中列出的许可中挑选恰当标识来声明你在使用的许可。

一些 JavaScript 处理工具会自动保留任何包含 `@license` 标签的 JSDoc 文档注释，例如 **Google's Closure Compiler**。如果你在使用这些工具，你或许希望添加一个包含 `@license` 标签的单独的 JSDoc 文档注释，其中包含完整地许可内容，这样许可的完整内容就会出现在生成的 JavaScript 文件中了。

## <span id="examples">示例</span>

**一个基于 Apache License 2.0 许可的模块**

```javascript
/**
 * Utility functions for the foo package.
 * @module foo/util
 * @license Apache-2.0
 */
```

**一个具有完整 MIT license 的 JSDoc 文档注释**

```javascript
/**
 * @license
 * Copyright (c) 2015 Example Corporation Inc.
 *
 * Permission is hereby granted, free of charge, to any person obtaining a copy
 * of this software and associated documentation files (the "Software"), to deal
 * in the Software without restriction, including without limitation the rights
 * to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
 * copies of the Software, and to permit persons to whom the Software is
 * furnished to do so, subject to the following conditions:
 *
 * The above copyright notice and this permission notice shall be included in all
 * copies or substantial portions of the Software.
 *
 * THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
 * IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
 * FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
 * AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
 * LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
 * OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
 * SOFTWARE.
 */
```

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @license](http://usejsdoc.org/tags-license.html "tag license")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>