## 手写bind

```js
Fuction.prototype.bindFn = function() {
  // 获取原函数
  const fn = this
  ///换取原函数的参数列表
  const obj = arguments[0]
  const args = [].slice.call(arguments, 1)

  return function() {
    const returnArgs = [].slice.call(arguments)
    fn.apply(obj, args.concat(returnArgs))
  }
}
```