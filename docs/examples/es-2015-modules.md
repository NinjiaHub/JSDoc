# ES 2015 Modules

## 内容列表 🕊️

* [模块标识符 (Module identifiers)](#identifiers "Module Identifiers")
* [导出值](#export)
* [相关链接](#related "related links")

**JSDoc 3** 使给遵循[ECMAScript 2015 规范](http://www.ecma-international.org/ecma-262/6.0/#sec-modules)设计的模块添加文档注释成为可能。**JSDoc 3.4.0** 及其之后的版本支持给 ES 2015 模块添加文档注释。

## <span id="identifiers">模块标识符 (Module identifiers)</span>

当给一个 **ES 2015 模块** 添加文档注释时，需要使用 [@module 标签](https://ninjiahub.github.io/JSDoc/docs/tags/module "tag-module") 来给该模块的标识符添加文档注释。例如，如果用户通过使用 `import * as myShirt from 'my/shirt'` 来加载一个模块，可以写一个包含 `@module my/shirt` 标签的 **JSDoc 注释** 作为该模块的文档注释。

如果只使用了 `@module` 而没有声明该模块的标识符，**JSDoc** 会尝试根据文件路径来推测正确的模块标识符。

当使用 JSDoc 中的 [namepaths](https://ninjiahub.github.io/JSDoc/docs/start/about-namepaths "about namepaths") 来引用另外一个 JSDoc 注释中的模块时，需要加上 `module:` 前缀：例如，如果你想让 `my/pants` 模块中的文档链接到 `my/shirt` 模块，可以使用 [@see 标签](https://ninjiahub.github.io/JSDoc/docs/tags/see "tag see") 通过下面的方式来给 `my/pants` 模块添加文档注释：

```jsdoc
/**
 * Pants module
 * @module my/pants
 * @see module:my/shirt
 */
```
同样，对于模块中的每一个成员，其 **命名路径(namepath)** 都以 `module:` 开头，随后是模块名字。例如，有一个 `my/pants` 模块，导出了一个 `Jeans` 类，该类有一个实例方法 `hem`，则该实例方法的完整名为 `module:my/pants.Jeans#hem`。

## <span id="export">导出值</span>

下面的例子演示了如何给 **ES 2015 模块** 中的各种导出值添加文档注释。通常情况下，可以只给定义导出值的 `export` 表达式添加 JSDoc 注释。如果在导出时使用了别名，则可以在 `export` 块中单独给该导出值添加文档注释。

**给一个模块的导出值添加文档注释：**

```jsdoc
/** @module color/mixer */

/** The name of the module. */
export const name = 'mixer';

/** The most recent blended color. */
export var lastColor = null;

/**
 * Blend two colors together.
 * @param {string} color1 - The first color, in hexadecimal format.
 * @param {string} color2 - The second color, in hexadecimal format.
 * @return {string} The blended color.
 */
export function blend(color1, color2) {}

// convert color to array of RGB values (0-255)
function rgbify(color) {}

export {
    /**
     * Get the red, green, and blue values of a color.
     * @function
     * @param {string} color - A color, in hexadecimal format.
     * @returns {Array.<number>} An array of the red, green, and blue values,
     * each ranging from 0 to 255.
     */
    rgbify as toRgb
}
```

## <span id="related">相关链接</span> 🕸

* [Using namepaths with JSDoc 3](https://ninjiahub.github.io/JSDoc/docs/start/about-namepaths "Using namepaths with JSDoc 3")
* [@module](https://ninjiahub.github.io/JSDoc/docs/tags/augments "tags-module")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - ES 2015 Modules](http://usejsdoc.org/howto-es2015-modules.html)。

如有版权问题请联系译者。

侵删。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>