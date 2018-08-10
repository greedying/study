# study
学习备忘录

## mysql
http://blog.51cto.com/lizhenliang/2095526

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
function test (x) {
  var sum = x * x;
  
  var tmp = function(y) {
    sum += y * y
    tmp.value = sum
    return tmp    
  } 
 
  var result = function (y) {
    sum += y * y
    tmp.value = sum;
    return tmp
  }
  result.value = x * x
  return result;
}
```
