

# 📘 RxJS 快速查阅手册

---

## 🧱 创建类操作符（Creation Operators）

### `of(...)`

**作用：** 创建一个发出参数值的 observable。

```ts
import { of } from 'rxjs';

of(1, 2, 3).subscribe(console.log);
// 输出：1 2 3
```

---

### `from(...)`

**作用：** 从数组、Promise、类数组等创建 observable。

```ts
import { from } from 'rxjs';

from([10, 20, 30]).subscribe(console.log);
// 输出：10 20 30
```

---

### `interval(time)`

**作用：** 每隔一定时间发出递增的数值（从 0 开始）。

```ts
import { interval } from 'rxjs';

interval(1000).subscribe(console.log);
// 每秒输出：0 1 2 3 ...
```

---

### `timer(dueTime, period?)`

**作用：** 延迟发出第一个值，可设置是否定期发出。

```ts
import { timer } from 'rxjs';

// 3秒后开始，每1秒发一次
timer(3000, 1000).subscribe(console.log);
```

---

### `range(start, count)`

**作用：** 发出一个范围内的整数。

```ts
import { range } from 'rxjs';

range(5, 3).subscribe(console.log);
// 输出：5 6 7
```

---

### `EMPTY` / `empty()`

**作用：** 不发出任何值，立即完成。

```ts
import { EMPTY } from 'rxjs';

EMPTY.subscribe({
  next: () => console.log('next'),
  complete: () => console.log('完成')
});
// 输出：完成
```

---

### `throwError(error)`

**作用：** 发出错误并终止 observable。

```ts
import { throwError } from 'rxjs';

throwError(() => new Error('出错了')).subscribe({
  error: err => console.error(err.message)
});
// 输出：出错了
```

---

## 🔄 转换类操作符（Transformation Operators）

### `map(fn)`

**作用：** 将源 observable 中的值映射成新的值。

```ts
import { of } from 'rxjs';
import { map } from 'rxjs/operators';

of(1, 2, 3).pipe(map(x => x * 2)).subscribe(console.log);
// 输出：2 4 6
```

---

### `pluck('prop')`

**作用：** 提取对象中的指定属性值。

```ts
import { from } from 'rxjs';
import { pluck } from 'rxjs/operators';

from([{ name: 'Tom' }, { name: 'Jerry' }])
  .pipe(pluck('name'))
  .subscribe(console.log);
// 输出：Tom Jerry
```

---

### `scan(accFn, seed)`

**作用：** 类似于 `Array.reduce`，但会输出每次累加的结果。

```ts
import { of } from 'rxjs';
import { scan } from 'rxjs/operators';

of(1, 2, 3).pipe(scan((acc, val) => acc + val, 0))
  .subscribe(console.log);
// 输出：1 3 6
```

---

### `switchMap(fn)`

**作用：** 切换到新的 observable，自动取消前一个。

```ts
import { interval, fromEvent } from 'rxjs';
import { switchMap } from 'rxjs/operators';

fromEvent(document, 'click')
  .pipe(switchMap(() => interval(1000)))
  .subscribe(console.log);
// 每次点击后重新开始间隔流
```

---

### `mergeMap(fn)`

**作用：** 将每个值映射为 observable，并合并结果。

```ts
import { of } from 'rxjs';
import { mergeMap, delay } from 'rxjs/operators';

of(1, 2).pipe(
  mergeMap(x => of(x * 10).pipe(delay(1000)))
).subscribe(console.log);
// 大约同时输出：10 20
```

---

### `concatMap(fn)`

**作用：** 顺序执行映射后的 observable。

```ts
of(1, 2).pipe(
  concatMap(x => of(x * 10).pipe(delay(1000)))
).subscribe(console.log);
// 依次输出：10（延迟1s）→ 20（再延迟1s）
```

---

### `exhaustMap(fn)`

**作用：** 忽略新的内部 observable，直到前一个完成。

```ts
fromEvent(document, 'click')
  .pipe(
    exhaustMap(() => interval(1000).pipe(take(3)))
  )
  .subscribe(console.log);
// 第一次点击触发后，后续点击在3秒内无效
```

---

## 🚦 过滤类操作符（Filtering Operators）

### `filter(fn)`

**作用：** 过滤掉不符合条件的值。

```ts
of(1, 2, 3, 4).pipe(filter(x => x % 2 === 0))
  .subscribe(console.log);
// 输出：2 4
```

---

### `take(n)`

**作用：** 只取前 n 个值。

```ts
interval(1000).pipe(take(3)).subscribe(console.log);
// 输出：0 1 2（每秒一个）
```

---

### `takeUntil(obs)`

**作用：** 直到另一个 observable 发出值才停止。

```ts
const stop$ = fromEvent(document, 'click');

interval(1000)
  .pipe(takeUntil(stop$))
  .subscribe(console.log);
// 点击页面停止输出
```

---

### `skip(n)`

**作用：** 跳过前 n 个值。

```ts
of(1, 2, 3, 4).pipe(skip(2)).subscribe(console.log);
// 输出：3 4
```

---

### `distinct()`

**作用：** 忽略已经出现过的值。

```ts
of(1, 2, 2, 3).pipe(distinct()).subscribe(console.log);
// 输出：1 2 3
```

---

### `distinctUntilChanged()`

**作用：** 忽略连续重复的值。

```ts
of(1, 1, 2, 2, 3).pipe(distinctUntilChanged()).subscribe(console.log);
// 输出：1 2 3
```

---

## 🔗 组合类操作符（Combination Operators）

### `merge(...)`

**作用：** 合并多个 observable，同时进行。

```ts
merge(interval(1000), interval(1500)).subscribe(console.log);
// 混合输出：0 0 1 1 2 ...
```

---

### `concat(...)`

**作用：** 按顺序执行 observable。

```ts
concat(of(1, 2), of(3, 4)).subscribe(console.log);
// 输出：1 2 3 4
```

---

### `combineLatest([a$, b$])`

**作用：** 只要其中一个发出，组合最新值。

```ts
combineLatest([interval(1000), interval(1500)])
  .pipe(take(5))
  .subscribe(console.log);
```

---

### `zip(a$, b$)`

**作用：** 按顺序组合，每组一个。

```ts
zip(of('A', 'B'), of(1, 2, 3)).subscribe(console.log);
// 输出：['A',1] ['B',2]
```

---

### `withLatestFrom(other$)`

**作用：** 触发主 observable 时，获取最新的其他 observable 值。

```ts
click$
  .pipe(withLatestFrom(input$))
  .subscribe(([click, inputValue]) => {
    console.log(inputValue);
  });
```

---

### `forkJoin([...])`

**作用：** 等所有 observable 完成后发出最终值。

```ts
forkJoin([
  of(1),
  of(2),
  of(3).pipe(delay(1000))
]).subscribe(console.log);
// 输出：[1, 2, 3]（延迟1秒）
```

---

## 🧪 工具类操作符（Utility）

### `tap(fn)`

**作用：** 不改变值，仅用于副作用/调试。

```ts
of(1, 2, 3).pipe(
  tap(x => console.log('中间值', x)),
  map(x => x * 10)
).subscribe(console.log);
```

---

### `delay(time)`

**作用：** 延迟发出值。

```ts
of('Hello').pipe(delay(1000)).subscribe(console.log);
// 1秒后输出 Hello
```

---

### `startWith(value)`

**作用：** 在源 observable 之前先发一个值。

```ts
of(2, 3).pipe(startWith(1)).subscribe(console.log);
// 输出：1 2 3
```

---

## 🧯 错误处理类操作符

### `catchError(fn)`

**作用：** 捕获错误并返回新的 observable。

```ts
throwError(() => 'Oops!').pipe(
  catchError(err => of('出错了：' + err))
).subscribe(console.log);
// 输出：出错了：Oops!
```

---

### `retry(n)`

**作用：** 出错时重试 n 次。

```ts
ajax('/wrong-url')
  .pipe(retry(3))
  .subscribe({
    error: err => console.error('最终失败')
  });
```

---

## 🔁 Subject 类型

| 类型                | 特点               | 示例                               |
| ----------------- | ---------------- | -------------------------------- |
| `Subject`         | 手动 `.next()`，多播  | `subject.next(value)`            |
| `BehaviorSubject` | 有初始值，订阅即获得最新值    | `new BehaviorSubject('default')` |
| `ReplaySubject`   | 缓存历史值            | `new ReplaySubject(2)`           |
| `AsyncSubject`    | 只发出最后一个值，且完成后才发出 | `new AsyncSubject()`             |

---
