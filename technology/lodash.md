
# 📘 Lodash 快速查阅手册（含示例）

> 所有示例默认已引入 Lodash：

```js
const _ = require('lodash'); // 或 import _ from 'lodash'
```

---

## 🧱 数组操作（Array）

---

### `_.chunk(array, size)`

将数组拆分成多个长度为 `size` 的数组块。

```js
_.chunk(['a', 'b', 'c', 'd'], 2);
// => [['a', 'b'], ['c', 'd']]
```

---

### `_.compact(array)`

移除数组中的假值（false、null、0、""、undefined、NaN）。

```js
_.compact([0, 1, false, 2, '', 3]);
// => [1, 2, 3]
```

---

### `_.difference(array, ...values)`

返回一个差集数组。

```js
_.difference([1, 2, 3], [2, 3]);
// => [1]
```

---

### `_.flatten(array)`

将嵌套数组扁平化一层。

```js
_.flatten([1, [2, [3, [4]]]]);
// => [1, 2, [3, [4]]]
```

---

### `_.flattenDeep(array)`

深度扁平化数组。

```js
_.flattenDeep([1, [2, [3, [4]]]]);
// => [1, 2, 3, 4]
```

---

### `_.uniq(array)`

去重。

```js
_.uniq([2, 1, 2]);
// => [2, 1]
```

---

### `_.zip(arr1, arr2)`

组合两个数组的值。

```js
_.zip(['a', 'b'], [1, 2]);
// => [['a', 1], ['b', 2]]
```

---

## 🧑‍🤝‍🧑 对象操作（Object）

---

### `_.get(object, path, [defaultValue])`

安全地获取嵌套属性。

```js
const obj = { a: { b: { c: 3 } } };
_.get(obj, 'a.b.c'); // => 3
_.get(obj, 'a.b.d', 'default'); // => 'default'
```

---

### `_.set(object, path, value)`

设置对象的嵌套属性。

```js
const obj = {};
_.set(obj, 'a.b.c', 4);
// obj => { a: { b: { c: 4 } } }
```

---

### `_.has(object, path)`

判断对象是否有某个属性。

```js
_.has({ a: { b: 2 } }, 'a.b'); // => true
```

---

### `_.merge(object, source)`

递归合并对象。

```js
_.merge({ a: { b: 1 } }, { a: { c: 2 } });
// => { a: { b: 1, c: 2 } }
```

---

### `_.pick(object, [paths])`

提取对象中指定属性。

```js
_.pick({ a: 1, b: 2, c: 3 }, ['a', 'c']);
// => { a: 1, c: 3 }
```

---

### `_.omit(object, [paths])`

移除对象中指定属性。

```js
_.omit({ a: 1, b: 2, c: 3 }, ['b']);
// => { a: 1, c: 3 }
```

---

## 🔁 集合操作（Collection）

---

### `_.map(collection, iteratee)`

类似 Array.map，但支持对象。

```js
_.map([1, 2, 3], n => n * 3); // => [3, 6, 9]
_.map({ a: 1, b: 2 }, n => n * 2); // => [2, 4]
```

---

### `_.filter(collection, predicate)`

过滤符合条件的值。

```js
_.filter([1, 2, 3, 4], n => n % 2 === 0);
// => [2, 4]
```

---

### `_.find(collection, predicate)`

返回第一个满足条件的元素。

```js
_.find([1, 2, 3, 4], n => n > 2);
// => 3
```

---

### `_.groupBy(collection, iteratee)`

根据条件分组。

```js
_.groupBy([6.1, 4.2, 6.3], Math.floor);
// => { '4': [4.2], '6': [6.1, 6.3] }
```

---

### `_.orderBy(collection, [iteratees], [orders])`

对集合排序。

```js
const users = [
  { name: 'Tom', age: 30 },
  { name: 'Jerry', age: 20 }
];
_.orderBy(users, ['age'], ['asc']);
// => [{name: 'Jerry'}, {name: 'Tom'}]
```

---

## 🧠 函数相关（Function）

---

### `_.debounce(func, wait)`

防抖函数（延迟触发）。

```js
const onResize = _.debounce(() => console.log('Resized!'), 500);
window.addEventListener('resize', onResize);
```

---

### `_.throttle(func, wait)`

节流函数（定期触发）。

```js
const onScroll = _.throttle(() => console.log('Scroll!'), 1000);
window.addEventListener('scroll', onScroll);
```

---

### `_.once(func)`

只执行一次。

```js
const init = _.once(() => console.log('Init!'));
init(); // 输出
init(); // 不输出
```

---

### `_.memoize(func)`

缓存函数调用结果。

```js
const add = (a, b) => a + b;
const memoizedAdd = _.memoize(add);

memoizedAdd(1, 2); // 计算
memoizedAdd(1, 2); // 缓存
```

---

## 🔢 数值相关（Number）

---

### `_.clamp(number, lower, upper)`

将数字限制在范围内。

```js
_.clamp(10, -5, 5); // => 5
_.clamp(-10, -5, 5); // => -5
```

---

### `_.random(lower, upper, floating)`

生成随机数。

```js
_.random(0, 5); // => 整数
_.random(0, 5, true); // => 浮点数
```

---

## 🔤 字符串操作（String）

---

### `_.camelCase(string)`

转为 camelCase（驼峰）。

```js
_.camelCase('Foo Bar'); // => 'fooBar'
```

---

### `_.kebabCase(string)`

转为 kebab-case（短横线）。

```js
_.kebabCase('Foo Bar'); // => 'foo-bar'
```

---

### `_.startCase(string)`

每个单词首字母大写。

```js
_.startCase('fooBar'); // => 'Foo Bar'
```

---

### `_.padStart(string, length, chars)`

左侧填充。

```js
_.padStart('5', 3, '0'); // => '005'
```

---

## ✅ 判断类（Lang）

---

### `_.isArray(value)`

是否为数组。

```js
_.isArray([1, 2]); // => true
```

---

### `_.isEmpty(value)`

是否为空（对象/数组/字符串等）。

```js
_.isEmpty({}); // => true
_.isEmpty([]); // => true
_.isEmpty(''); // => true
```

---

### `_.isEqual(a, b)`

深度比较两个值。

```js
_.isEqual({ a: 1 }, { a: 1 }); // => true
```

---

## 📦 实用工具（Util）

---

### `_.times(n, iteratee)`

执行函数 n 次。

```js
_.times(3, i => console.log(i));
// 输出：0 1 2
```

---

### `_.range([start=0], end, [step=1])`

生成数字范围数组。

```js
_.range(4); // => [0, 1, 2, 3]
_.range(1, 5); // => [1, 2, 3, 4]
```

---

### `_.noop()`

空函数，常用于默认回调。

```js
_.noop(); // 什么都不做
```

---

### `_.identity(value)`

返回接收到的参数。

```js
_.map([1, 2, 3], _.identity);
// => [1, 2, 3]
```

---
