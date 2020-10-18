## 学习笔记

### unshift, shift, pop, push

```
var a = [1, 2, 3];
                             
var b = a.unshift(0);
console.log(a); //[0, 1, 2, 3]
console.log(b); //4

var a = [1, 2, 3];
var b = a.shift();
console.log(a); //[2, 3]
console.log(b); //1

var a = [1, 2, 3];
var b = a.pop();
console.log(a); //[1, 2]
console.log(b); //3

var a = [1, 2, 3];
var b = a.push(4);
console.log(a); //[1, 2, 3, 4]
console.log(b); //4
```