# {@link}

## 内容列表 🕊️

* [同义词](#synonyms "synonyms")
* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [链接格式](#link "link format")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="synonyms">同义词</span>

* `{@linkcode}`
* `{@linkplain}`

## <span id="syntax">语法</span>

```jsdoc
{@link namepathOrURL}
[link text]{@link namepathOrURL}
{@link namepathOrURL|link text}
{@link namepathOrURL link text (after the first space)}
```
## <span id="overview">概述</span>

`{@link}` 标签会创建一个指向你指定的 **命名路由(namepath)** 或者 **URL** 的链接。在使用 `{@link}` 标签时，可以手动指定链接文字，如果没有指定链接文字，JSDoc 会使用 **namepath** 或者 **URL** 作为链接文字。

如果要指向教程(tutorial)，请使用 [{@tutorial}](https://ninjiahub.github.io/JSDoc/docs/tags/inline-tutorial "tag inline-tutorial") 标签代替 `{@link}` 标签。

## <span id="link">链接格式</span>

`{@link}` 标签默认生成标准的 HTML 锚点。然而，你可能偏好将某个特定的链接显示为等宽字体(monospace font)，或者分别指定链接的样式。可以通过使用下面 `{@link}` 标签的同义词来控制链接的样式：

* `{@linkcode}`：强制链接文字使用等宽字体
* `{@linkplain}`：强制链接使用普通字体，不使用等宽字体

也可以在配置文件中设置下面中的一个选项；详情请戳 [JSDoc configuration](https://ninjiahub.github.io/JSDoc/docs/start/about-configuring-jsdoc "start about-configuring-jsdoc")。

* `templates.cleverLinks`：设置为 `true` 时，链接到 URL 的为普通字体，链接到代码的使用等宽字体
* `templates.monospaceLinks`：设置为 `true` 时，除 `{@linkplain}` 标签创建的链接之外的所有链接都使用等宽字体

**注意：**虽然 JSDoc 的默认模版可以正确地渲染这些标签，其他模版可能并不识别 `{@linkcode}` 和 `{@linkplain}` 标签。另外，其他模版在渲染链接时可能会忽略配置选项。

## <span id="examples">示例</span>

下面的例子展示了所有给 `{@link}` 标签添加链接文字的方法：

**提供链接文字**

```javascript
/**
 * See {@link MyClass} and [MyClass's foo property]{@link MyClass#foo}.
 * Also, check out {@link http://www.google.com|Google} and
 * {@link https://github.com GitHub}.
 */
function myFunction() {}
```

默认情况下，上面的例子经过 JSDoc 处理后会生成如下结果：

**{@link} 标签默认输出**

```html
See <a href="MyClass.html">MyClass</a> and <a href="MyClass.html#foo">MyClass's foo
property</a>. Also, check out <a href="http://www.google.com">Google</a> and
<a href="https://github.com">GitHub</a>.
```

如果配置中的 `templates.cleverLinks` 被设置为 `true`，则上面例子的输出结果如下：

**{@link} 标签开启 clever links 模式**

```html
See <a href="MyClass.html"><code>MyClass</code></a> and <a href="MyClass.html#foo">
<code>MyClass's foo property</code></a>. Also, check out
<a href="http://www.google.com">Google</a> and <a href="https://github.com">GitHub</a>.
```

## <span id="related">相关链接</span>

* [Configuring JSDoc with a configuration file
](https://ninjiahub.github.io/JSDoc/docs/start/about-configuring-jsdoc "start about-configuring-jsdoc")
* [Using namepaths with JSDoc 3](https://ninjiahub.github.io/JSDoc/docs/start/about-namepaths "start about-namepaths")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - Using namepaths with JSDoc 3](http://usejsdoc.org/about-namepaths.html "namepaths")。

如有版权问题请联系译者。

侵删。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>