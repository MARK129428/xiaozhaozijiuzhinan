## max最大值

```js
const array = [1,2,3,4,5]

const res = Math.max.apply(null, array)
console.log(`res`, res)
```


```js
function getMax(arr) {
  return array.reduce((prev, cur) => {
    return cur > prev ? cur : prev
  })
}
```