# @property

## 内容列表 🕊️

* [同义词](#Synonyms "Synonyms")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="Synonyms">同义词</span>

`@prop`

## <span id="overview">概述</span>

`@property` 标签是标记类、命名空间和其他对象属性的便捷方式。

通常情况下 JSDoc 会创建一个全新的页面来展示嵌套命名空间继承等级关系的信息。有时确实需要将所有属性，包括嵌套属性，展示在同一个页面中。

注意，@property 标签必须用来给命名空间、类等的属性添加文档注释。该标签用于静态属性集合，除了类型、名字以及描述外，不允许提供 @examples 以及其他类似的复杂信息。

## <span id="examples">示例</span>

下面的例子中有一个命名空间 “config”。我们想让所有的默认属性，包括嵌套属性，与 “config” 的文档展示在同一个页面中。

**一个包含默认属性以及嵌套默认属性的命名空间**

```javascript
/**
 * @namespace
 * @property {object}  defaults               - The default values for parties.
 * @property {number}  defaults.players       - The default number of players.
 * @property {string}  defaults.level         - The default level for the party.
 * @property {object}  defaults.treasure      - The default treasure.
 * @property {number}  defaults.treasure.gold - How much gold the party starts with.
 */
var config = {
    defaults: {
        players: 1,
        level:   'beginner',
        treasure: {
            gold: 0
        }
    }
};
```

下面的例子展示了如何表示一个属性是可选的：

**包含必选属性以及可选属性的类型定义**

```javascript
/**
 * User type definition
 * @typedef {Object} User
 * @property {string} email
 * @property {string} [nickName]
 */
```

## <span id="related">相关链接</span>

* [@enum](https://ninjiahub.github.io/JSDoc/docs/tags/enum "tag @enum")
* [@member](https://ninjiahub.github.io/JSDoc/docs/tags/member "tag @member")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @property](http://usejsdoc.org/tags-property.html "@property")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>