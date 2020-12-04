# 常用的JavaScript简写技巧

1、给多个变量赋值
```
  //bad 
  let a, b, c; 
  a = 5; 
  b = 8; 
  c = 12;
  
  //good 
  let [a, b, c] = [5, 8, 12];

```
2、三元运算符
```
//bad 
let marks = 26; 
let result; 
if(marks >= 30){
 result = 'Pass'; 
}else{ 
 result = 'Fail'; 
} 
//good 
let result = marks >= 30 ? 'Pass' : 'Fail';

```
3、赋默认值
```
let imagePath = getImagePath() || 'default.jpg';

```
4、与(&&) 短路运算
```
//bad 
if (isLoggedin) {
 goToHomepage(); 
} 

//good 
isLoggedin && goToHomepage();

```

5、交换2个变量
```
let x = 'Hello', y = 55; 
//bad 
const temp = x; 
x = y; 
y = temp; 

//good 
[x, y] = [y, x];

```

6、箭头函数
```
//bad 
function add(num1, num2) { 
   return num1 + num2; 
} 

//good 
const add = (num1, num2) => num1 + num2;

```

7、模板字符串
```
//bad 
console.log('You got a missed call from ' + number + ' at ' + time); 


//good 
console.log(`You got a missed call from ${number} at ${time}`);

```

8、多行字符串
```
//bad 
console.log('JavaScript, often abbreviated as JS, is a\n' +             'programming language that conforms to the \n' + 
'ECMAScript specification. JavaScript is high-level,\n' + 
'often just-in-time compiled, and multi-paradigm.' ); 

//good 
console.log(`JavaScript, often abbreviated as JS, is a programming language that conforms to the ECMAScript specification. JavaScript is high-level, often just-in-time compiled, and multi-paradigm.`);

```

9、多条件检查
```

//bad 
if (value === 1 || value === 'one' || value === 2 || value === 'two') { 
     // Execute some code 
} 


// good 1
if ([1, 'one', 2, 'two'].indexOf(value) >= 0) { 
    // Execute some code 
}
// good 2
if ([1, 'one', 2, 'two'].includes(value)) { 
    // Execute some code 
}

```