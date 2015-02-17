
### 1.Fibonacci--斐波那契数列

算法复杂度为[O(2n)](http://stackoverflow.com/questions/360748/computational-complexity-of-fibonacci-sequence/360773#360773)

```js
function fibonacci(n) {
  return n < 2 ? n : fibonacci(n-1) + fibonacci(n-2); 
}
```

### 2.求数组中的最大值

```js
function maxInArray(arr) {
  return Math.max.apply(Math, arr);
}
```

### 3. 字符串反转

```js
String.prototype.reverse = function() {
  return this.split('').reverse().join('');
}
```
or

```js
String.prototype.reverse = function() {
    var str = '';
    var len = this.length;
    while (len>0) {
        str += this.substring(len-1, len);
        len--;
    }
    return str;
}
```

注: 在类似'foo 𝌆 bar'这种astral symbol,将展示异。

可以使用[ Esrever](https://github.com/mathiasbynens/esrever) 来处理这种特殊字符的反转。

### 4.反转DOM
