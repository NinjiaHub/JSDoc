# @readonly

## 内容列表 🕊️

* [概述](#overview "overview")
* [示例](#examples "examples")

## <span id="overview">概述</span>

`@readonly` 标签表示一个标识符是只读的。注意这只是对于注释而言 - JSDoc 并不会检查你在代码中是否真的将该标识符作为只读的对待。

## <span id="examples">示例</span>

**使用 @readonly 标签**

```javascript
/**
 * A constant.
 * @readonly
 * @const {number}
 */
const FOO = 1;
```

**在 getter 中使用 @readonly 标签**

```javascript
/**
 * Options for ordering a delicious slice of pie.
 * @namespace
 */
var pieOptions = {
    /**
     * Plain.
     */
    plain: 'pie',
    /**
     * A la mode.
     * @readonly
     */
    get aLaMode() {
        return this.plain + ' with ice cream';
    }
};
```

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @readonly](http://usejsdoc.org/tags-readonly.html "tag @readonly")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>