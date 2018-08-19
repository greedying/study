# study
学习备忘录

## mysql
http://blog.51cto.com/lizhenliang/2095526
http://www.cnblogs.com/clsn/p/8038964.html#_label6

## php
 
### clean code php （代码整洁之道）
https://github.com/jupeter/clean-code-php

## 算法
https://github.com/JesseZhao1990/algorithm

## javascipt
### 面试
https://github.com/JesseZhao1990/algorithm

### 写出满足条件的函数
```javascript
  result = f(a)(b)(c)...
  result.value = a^2 + b^2 + c^2
````
我写出的答案
```javascript
function mySum (x) {
  var sum = x * x;
  var tmp = function(y) {
    sum += y * y
    tmp.value = sum
    return tmp    
  } 
  tmp.value = sum;
  return tmp
}
```
第二种写法，判断this
```javascript
var mySum = function () {
  var value = 0;
  return function (x) {
    if (this === mySum) {
      value += x*x
    } else {
      value = x*x
    }
    var that = arguments.callee
    var result = mySum.bind(that)
    result.value = value
    return result
  }
} ();
```
上面代码改善，不依赖具体函数名
```javascript
var mySum = function () {
  var value = 0;
  return function (x) {
    if (this === arguments.callee) {
      value += x*x
    } else {
      value = x*x
    }
    var result = arguments.callee.bind(arguments.callee)
    result.value = value
    return result
  }
} ();
```


### vue 源码分析
http://hcysun.me/vue-design/art/   
https://ustbhuangyi.github.io/vue-analysis/prepare/
