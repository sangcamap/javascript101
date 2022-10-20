# BASIC JAVASCRIPT

## Hello world


```javascript
console.log("Hello world!")
```

<details>
  <summary>🟢 Terminal</summary>

```javasript
Hello world!
```
</details>

---
<br/><br/>



## Variables Constant and Usage

> Có 3 cách khai báo biến trong javascript và mỗi cách khai báo có cách dùng riêng <br>
> - var: var là từ khóa lâu đời nhất để khai báo một biến trong JavaScript. Phạm vi của từ khóa var là phạm vi toàn cục hoặc phạm vi Function (hàm).
> - let: Phạm vi của một biến let chỉ là phạm vi khối. Nó không thể truy cập được bên ngoài khối cụ thể ({block}).
> - const: Khi người dùng khai báo một biến const , họ cần khởi tạo nó, nếu không, nó sẽ trả về một lỗi. Người dùng không thể cập nhật biến const sau khi nó được khai báo.


### Khai báo biến
```javascript
var a = 123
let b = 123
const c = 123
```

### Code ví dụ về var

```javascript
var times = 4
var a = 123
if (times > 3) {
    var a = "say Hello"
}
console.log(a)
a = 123456 
console.log(a)
```

<details>
  <summary>🟢 Terminal</summary>

```javascript
say Hello
123456
```

</details>

----
<br/><br/>


### Code ví dụ về let
```javascript
var times = 4
let a = 123
if (times > 3) {
    let b = "say Hello"
}
console.log(b)
b = 123456
console.log(b)
```

<details>
  <summary>🟢 Terminal</summary>

```javascript
123
123456
```
</details>

----
<br/><br/>

### Code ví dụ về const
```javascript
var times = 4
const a = 123
if (times > 3) {
    const c = "say Hello"
}
console.log(c)
c = 123456
console.log(c)
```

<details>
  <summary>🟢 Terminal</summary>

```javascript
c = 123456
  ^

TypeError: Assignment to constant variable.
    at Object.<anonymous> (D:\Code project\basic-js\test.js:8:3)
    at Module._compile (internal/modules/cjs/loader.js:1063:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1092:10)
    at Module.load (internal/modules/cjs/loader.js:928:32)
    at Function.Module._load (internal/modules/cjs/loader.js:769:14)
    at Function.executeUserEntryPoint [as runMain] (internal/modules/run_main.js:72:12)
    at internal/main/run_main_module.js:17:47

// không in ra 123 dù cho dòng đó đúng
```
</details>

---
<br/><br/>

## Working with String

### Khai báo chuỗi

```javascript
let str1 = 'hello world' 
let str2 = "hello world"
let str3 = `hello world` // -> sử dụng được cả khi chuỗi xuống dòng
```

---
<br/><br/>


### Nối chuỗi

```javascript
let my_str = "Hello" + " " + "world"
console.log(my_str)
```
<details>
  <summary>🟢 Terminal</summary>

```javasript
Hello world
```
</details>

---
<br/><br/>

### Ép kiểu chuỗi

```javascript
let num = 123
console.log(typeof num)
num = String(num)
console.log(typeof num)
```
<details>
  <summary>🟢 Terminal</summary>

```javasript
number
string
```
</details>

---
<br/><br/>

### String Menthods

#### **length**

```javascript
let txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
console.log(txt.length)
```
 
<details>
<summary>🟢 Terminal</summary>

```javasript
26
```
</details>
 
---
<br/><br/>

#### **slice()**
> slice() trả về một chuỗi được cắt từ chuỗi gốc bằng cách truyền vào các tham số chỉ vị trí

```javascript
let str = "Apple, Banana, Kiwi";
let part = str.slice(7, 13); //slice(start, end)
console.log(str)
console.log(part)
```
 
<details>
<summary>🟢 Terminal</summary>

```javasript
Apple, Banana, Kiwi
Banana
```
</details>
 
---


```javascript
let str = "Apple, Banana, Kiwi";
let part = str.slice(-12, -6); // có thể truyền các position âm để cắt ngược từ phía sau
console.log(part)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
Banana 
```
</details>
 
---
<br/><br/>

#### **substring()**

> substring() giống với slice() nhưng những vị trí <0 sẽ được xem là bằng 0

```javascript
let str = "Apple, Banana, Kiwi";
let part = str.substring(7, 13); //substring(start, end)
console.log(part)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
Banana
```
</details>
 
---
<br/><br/>

#### **substr()**

> substr() cũng tương tự như slice() nhưng giá trị thứ 2 truyền vào sẽ là độ dài chuỗi muốn cắt tính từ start

```javascript
let str = "Apple, Banana, Kiwi";
let part= str.substr(7, 13); //substr(start, length)
console.log(part)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
Banana
```
</details>
 
---
<br/><br/>

#### **replace()**

> replace() trả về một chuỗi được thay thế từ chuỗi gốc, và chỉ thay thế chuỗi đầu tiên tìm thấy

```javascript
let text = "Chào anh nhé! Chào anh nhé!";
let newText = text.replace("anh", "em");
console.log(newText)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
Chào em nhé! Chào anh nhé!
```
</details>
 
---
<br/><br/>

#### **toLowerCase()**

```javascript
let str = 'Xin cHào Mọi người'
let new_str = str.toLowerCase()
console.log(str)
console.log(new_str)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
Xin cHào Mọi người
xin chào mọi người
```
</details>
 
---
<br/><br/>

#### **toUpperCase()**


```javascript
let str = 'Xin cHào Mọi người'
let new_str = str.toUpperCase()
console.log(str)
console.log(new_str)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
Xin cHào Mọi người
XIN CHÀO MỌI NGƯỜI
```
</details>
 
---
<br/><br/>

#### **concat()**

```javascript
let text1 = "Sang";
let text2 = "Nguyễn";
let text3 = text1.concat(" ", text2);
console.log(text3)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
Sang Nguyễn
```
</details>
 
---
<br/><br/>


#### **trim()**

```javascript
let text1 = "      Xin chào      ";
let text2 = text1.trim();
console.log(text1)
console.log(text2)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
      Xin chào      
Xin chào
```
</details>
 
---
<br/><br/>

#### **trimStart()** và **strimEnd()**

```javascript
let text1 = "      Xin chào      ";
let text2 = text1.trimStart()
let text3 = text1.trimEnd()
console.log(text1)
console.log(text2 + '.')
console.log(text3 + '.')
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
Xin chào      
Xin chào      .
      Xin chào.
```
</details>
 
---
<br/><br/>

### String Search
> Các phương thức String Search trả về vị trí của chuỗi cần tìm ở trong chuỗi gốc nếu có, nếu không có sẽ trả về -1 <br>
> Các phương thức gồm:
> - lastIndexOf()
> - indexOf()
> - search()
> - match()

<br/><br/>

#### **lastIndexOf() & indexOf()**

```javascript
let str = "Sang đang ở nhà Sang";
let pos = str.lastIndexOf("Sang");
console.log(pos)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
16 
```
</details>
 
---


```javascript
let str = "Sang đang ở nhà Sang";
let pos = str.indexOf("Sang");
console.log(pos)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
0
```
</details>
 
---

```javascript
let str = "Sang đang ở nhà Sang";
let pos = str.indexOf("anh Duy");
console.log(pos)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
-1
```
</details>
 
---

```javascript
let str = "Sang đang ở nhà Sang";
let pos = str.indexOf("Sang", 5); // có thể thêm vào start_pos
console.log(pos)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
16
```
</details>
 
---
<br/><br/>

#### **search()**

> search() cũng trả về vị trí chuỗi nhưng điểm khác biệt là nó không nhận tham số vị trí bắt đầu. Ưu điểm của search là có thể kết hợp với [regular expressions](https://www.w3schools.com/jsref/jsref_obj_regexp.asp)

```javascript
let str = "Sang đang ở nhà Sang";
let pos = str.search("Sang");
console.log(pos)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
0
```
</details>
 
---
<br/><br/>

#### **match()**

> match() tương tự với search() nhưng hàm này này trả về 1 mảng.

```javascript
let str = "Sang đang ở nhà Sang";
let arr = str.match("Sang"); 
console.log(arr)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
[ 'Sang', index: 0, input: 'Sang đang ở nhà Sang', groups: undefined ]
```
</details>
 
---
<br/><br/>


## Working with Array

### Khai báo Array

```javascript
let arr = ['xin', 'chào', 'mọi', 'người']
```

<br/>

### Array Menthods

#### **toString()**

> Chuyển arr về dạng str

```javascript
let arr = ['xin', 'chào', 'mọi', 'người']
let str_arr = arr.toString()
console.log(str_arr)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
xin,chào,mọi,người
```
</details>
 
---
<br/><br/>

#### **join()**

> Chuyển arr về dạng str nhưng chèn vào giữa các phần tử là chuỗi truyền vào

```javascript
let arr = ['xin', 'chào', 'mọi', 'người']
let join_arr = arr.join(' ')
console.log(join_arr)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
xin chào mọi người
```
</details>
 
---
<br/><br/>

#### **pop()**

> Bỏ 1 phần tử cuối trong mảng

```javascript
let arr = ['xin', 'chào', 'mọi', 'người']
arr.pop()
console.log(arr)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
[ 'xin', 'chào', 'mọi' ]
```
</details>
 
---
<br/><br/>

#### **push()**

> Thêm 1 phần tử vào cuối mảng

```javascript
let arr = ['xin', 'chào', 'mọi', 'người']
arr.push('nhen')
console.log(arr)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
[ 'xin', 'chào', 'mọi', 'người', 'nhen' ]
```
</details>
 
---
<br/><br/>

#### **shift()**

> Bỏ phần tử đầu mảng

```javascript
let arr = ['xin', 'chào', 'mọi', 'người']
arr.shift()
console.log(arr)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
[ 'chào', 'mọi', 'người' ]
```
</details>
 
---
<br/><br/>

#### **unshift()**
> Thêm một phần tử vào đầu mảng

```javascript
let arr = ['xin', 'chào', 'mọi', 'người']
arr.unshift('hello')
console.log(arr)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
[ 'hello', 'xin', 'chào', 'mọi', 'người' ]
```
</details>
 
---
<br/><br/>

#### **concat()**

> Gộp mảng

```javascript
let arr1 = ["Sang", "Long"]
let arr2 = ["Hưng", "Quân", "Quỳnh Anh"]
let arr3 = ["anh Duy", "chị Châu"]
let arr4 = arr1.concat(arr2)
let arr5 = arr1.concat(arr2, arr3)
console.log(arr4)
console.log(arr5)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
[ 'Sang', 'Long', 'Hưng', 'Quân', 'Quỳnh Anh' ]
[ 'Sang', 'Long', 'Hưng', 'Quân', 'Quỳnh Anh', 'anh Duy', 'chị Châu' ]
```
</details>
 
---
<br/><br/>

#### **splice()**

> splice() có thể cắt mảng và thêm phần tử

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"]
fruits.splice(2, 0, "Lemon", "Kiwi") // thêm "Lemon" và "Kiwi" vào vị trí số 2
console.log(fruits)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
[ 'Banana', 'Orange', 'Lemon', 'Kiwi', 'Apple', 'Mango' ]
```
</details>
 
---

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 2, "Lemon", "Kiwi"); // xóa 2 phần tử cuối và thêm "Lemon" và "Kiwi" vào vị trí số 2
console.log(fruits)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
[ 'Banana', 'Orange', 'Lemon', 'Kiwi' ]
```
</details>
 
---

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"]
fruits.splice(0, 1) // xóa 1 phần tử tính vị trí số 0
console.log(fruits)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
[ 'Orange', 'Apple', 'Mango' ]
```
</details>
 
---
<br/><br/>

#### **slice()**

> Khác với splice() slice không xóa đi phần tử của mảng ban đầu

```javascript
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(1, 3);
console.log(fruits)
console.log(citrus)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
[ 'Banana', 'Orange', 'Lemon', 'Apple', 'Mango' ]
[ 'Orange', 'Lemon' ]
```
</details>
 
---
<br/><br/>

#### **sort()**

> Sắp xếp tăng dần

```javascript
let arr = [2, 3, 7, 8, 6, 4]
arr.sort()
console.log(arr)

```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
[ 2, 3, 4, 6, 7, 8 ]
```
</details>
 
---

<br/><br/>

#### **reverse()**

> Đảo ngược mảng

```javascript
let arr = [2, 3, 7, 8, 6, 4]
arr.reverse()
console.log(arr)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
[ 4, 6, 8, 7, 3, 2 ]
```
</details>
 
---
<br/><br/>


#### **forEach()**

> Đối với từng phần tử trong mảng, thực hiện từng hành vi tương ứng

```javascript
let arr = [1, 1, 1, 1, 1, 1]
arr.forEach(e => console.log(e + 1))
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
2
2
2
2
2
2
```
</details>
 
---
<br/><br/>


#### **map()**

> Trả về một mảng, được thực hiện hành vi nào đó từ mảng ban đầu

```javascript
let arr = [1, 1, 1, 1, 1, 1]
let new_arr = arr.map(e => e + 1)
console.log(new_arr)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
[ 2, 2, 2, 2, 2, 2 ]
```
</details>
 
---
<br/><br/>

#### **filter()**

> Trả về một mảng, gồm các phần tử trong mảng ban đầu thỏa điều kiện

```javascript
let arr = [-1, -2, -3, 1, 2, 3]
let new_arr = arr.filter(e => e > 0)
console.log(new_arr)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
[ 1, 2, 3 ]
```
</details>
 
---
<br/><br/>


## Working with If ... Else ...
<br>

```javascript
let age = 12
if (age < 18) {
    console.log("trẻ")
}
else{
    console.log("già")
}
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
trẻ
```
</details>
 
---

```javascript
let age = 20
if (age < 18) {
    console.log("trẻ")
}
else{
    console.log("già")
}
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
già
```
</details>
 
---
<br/><br/>


## Loop 
<br>

### For loop

```javascript
for (let i = 0; i < 5; i++) {
    console.log(i)
}
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
0
1
2
3
4
```
</details>
 
---

```javascript
arr = ["Sang", "Hưng", "Quỳnh Anh"]
for(let i=0; i<arr.length; i++){
    console.log(arr[i])
}
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
Sang
Hưng
Quỳnh Anh
```
</details>
 
---
<br/><br/>

### For-in loop

```javascript
arr = ["Sang", "Hưng", "Quỳnh Anh"]
for(i in arr){
    console.log(arr[i])
}
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
Sang
Hưng
Quỳnh Anh
```
</details>
 
---
<br/><br/>

### For-of loop

```javascript
arr = ["Sang", "Hưng", "Quỳnh Anh"]
for(child of arr){
    console.log(child)
}
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
Sang
Hưng
Quỳnh Anh
```
</details>
 
---
<br/><br/>

### While loop

```javascript
let arr = ["Sang", "Hưng", "Quỳnh Anh"]
let i = 0
while(i < arr.length){
    console.log(arr[i])
    i++
}
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
Sang
Hưng
Quỳnh Anh
```
</details>
 
---
<br/><br/>


### break & continute

> break sẽ dừng vòng lặp

```javascript
arr = ["Sang", "Hưng", "Quỳnh Anh", "anh Duy", "chị Châu"]
for(let i=0; i<arr.length; i++){
    if (arr[i] == "anh Duy") {
        break
    }
    console.log(arr[i])
}
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
Sang
Hưng
Quỳnh Anh
```
</details>
 
---
<br/><br/>

> continute sẽ bỏ qua đoạn code bên dưới và tiếp tục vòng lặp

```javascript
arr = ["Sang", "Hưng", "Quỳnh Anh", "anh Duy", "chị Châu"]
for(let i=0; i<arr.length; i++){
    if (arr[i] == "anh Duy") {
        continue
    }
    console.log(arr[i])
}
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
Sang
Hưng
Quỳnh Anh
chị Châu
```
</details>
 
---
<br/><br/>

## Working with function
<br>

### Declaration Function

> Loại func cơ bản trong javascript, có áp dụng hoisting

```javascript
function doSomething() {
    console.log('doSomething');
}

doSomething()
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
doSomething
```
</details>
 
---
<br/><br/>

### Expression Function (anonymous function)

> Func được gán vào một biến, không áp dụng hoisting

```javascript
let run = function() {
    console.log('run');
}

run()
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
run
```
</details>
 
---
<br/><br/>

### Arrow Function (ES6)

> Func được thêm từ ES6, có cách khai báo đơn giản, không áp dụng hoisting

```javascript
let run = () => console.log('run');
run()
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
run
```
</details>
 
---

```javascript
let run = (a,b) => a + b
let sum = run(10,10)
console.log(sum)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
20
```
</details>
 
---
<br/><br/>


### Hoisting trong javascript

```javascript
//Function declaration
speak();
function speak() {
	console.log("Chào mọi người");
}
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
Chào mọi người
```
</details>
 
---
<br/><br/>

```javascript
// Function expression
speak();
var speak = function () {
	console.log("Chào mọi người")
};
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
speak();
^

TypeError: speak is not a function
    at Object.<anonymous> (D:\Code project\basic-js\test.js:4:1)
    at Module._compile (internal/modules/cjs/loader.js:1063:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1092:10)
    at Module.load (internal/modules/cjs/loader.js:928:32)
    at Function.Module._load (internal/modules/cjs/loader.js:769:14)
    at Function.executeUserEntryPoint [as runMain] (internal/modules/run_main.js:72:12)
    at internal/main/run_main_module.js:17:47
```
</details>
 
---
<br/><br/>

### Immediately Invoked Function Expressions (IIFE)

> Các hàm IIFE sẽ được gọi ngay khi khởi tạo

```javascript
(function (){ 
    console.log("Hello mọi người") 
})();

(() => {
    console.log("Hello mọi người")
})();

```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
Hello mọi người
Hello mọi người
```
</details>
 
---


```javascript
(function(dt) {
    console.log(dt.toLocaleTimeString());
})(new Date());

((dt) => {
    console.log(dt.toLocaleTimeString());
})(new Date());

//IIFE cũng có thể nhận vào các parameter
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
8:56:07 AM
8:56:07 AM
```
</details>
 
---
<br/><br/>

## Object literals & JSON

### Object

#### **Cấu trúc của Object**

```javascript
let person = {
    name:"Sang", 
    age: 15, 
    job: "student"
};

console.log(person)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
{ name: 'Sang', age: 15, job: 'student' }
```
</details>
 
---

```javascript
let person = {
    name:"Sang", 
    age: 15, 
    job: "student"
};

console.log(person.name)
console.log(person.age)
console.log(person.job)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
Sang
15
student
```
</details>
 
---
<br/><br/>


### JSON

#### **Cấu trúc của JSON**

> Cú pháp của JSON rất đơn giản là mỗi thông tin dữ liệu sẽ có 2 phần đó là key và value

```JSON
{
    "students":[
        {"name":"Sang", "age":"15"},
        {"name":"Hưng", "age":"15"},
        {"name":"Quỳnh Anh", "age":"15"}
    ]
}
```

#### **JSON.parse()**

> Dùng JSON.parse() để chuyển JSON về object trong javascript

```javascript
// tạo file a.json
// terminal node --experimental-json-modules ./main.js
import data from './a.json';
console.log(data);
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
{
  students: [
    { name: 'Sang', age: '15' },
    { name: 'Hưng', age: '15' },
    { name: 'Quỳnh Anh', age: '15' }
  ]
}
```
</details>
 
---

```javascript
import data from './a.json';
console.log(data.students[0]);
console.log(data.students[0].name);
console.log(data.students[0].age);
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
{ name: 'Sang', age: '15' }
Sang
15
```
</details>
 
---
<br/><br/>

## Class & Constructor

### Khởi tạo

```javascript
// Tạo class human với constructor gồm 3 tham số gender, age, name
class Human {
    constructor(gender, age, name) {
      this.gender = gender;
      this.age = age;
      this.name = name;
    }

    say = () => {
      console.log("Xin chào mọi người")
    }
}
```

```javascript
// Khởi tạo class với constructor
const sang = new Human("Nam", 15, "Sang Nguyễn");
sang.say()
console.log(`Tôi là ${sang.name}, ${sang.age} tuổi`)
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
Xin chào mọi người
Tôi là Sang Nguyễn, 15 tuổi
```
</details>
 
---
<br/><br/>

### Kế thừa

```javascript
class Human {
    constructor(gender, age, name) {
      this.gender = gender;
      this.age = age;
      this.name = name;
    }

    say = () => {
      console.log("Xin chào mọi người")
    }
}

class Student extends Human{
    constructor(idSV, name, age, gender) {
        super(gender, age, name); // Điền các thuộc tính của class Human
        this.idSV = idSV;
    }
    
    get_info = () => {
        console.log(`${this.name}, MSSV là ${this.idSV}`)
    }
}


const sang = new Student('123', 'Sang Nguyễn', 15, 'Nam')
sang.say() // Student có thể sử dụng phương thức của Human
sang.get_info()
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
Xin chào mọi người
Sang Nguyễn, MSSV là 123
```
</details>
 
---
<br/><br/>

## Bất đồng bộ (CALLBACK, ASYNC AWAIT)

> CALLBACK, PROMISES, ASYNC AWAIT sinh ra để giải quyết vấn đề bất đồng bộ trong js. Mỗi cái có ưu nhược điểm riêng

```javascript
const run = () => {
    setTimeout(() => console.log(1), 0) 
    // Dòng này sẽ in ra sau cùng mặc dù nó nằm đầu tiên
    console.log(2)
    console.log(3)
}

run()
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
2
3
1
```
</details>
 
---
<br/><br/>

### CALLBACK
> Bằng cách dùng callback ta có thể giải quyết vấn đề bất đồng bộ, nhưng nhược điểm của phương pháp này là dễ gây ra "callback hell" nếu cấu trúc phức tạp

```javascript
const run = () => {
    setTimeout(() => {
        console.log(1);
        (() => {
            console.log(2);
            (() => {
                console.log(3);
            })();
        })();
    }, 0) 

}

run()
```
 
<details>
<summary>🟢 Terminal</summary>
 
```javasript
1
2
3
```
</details>
 
---
<br/><br/>

### ASYNC & AWAIT

> - **Async** được sử dụng để khai báo một hàm bất đồng bộ. <br>
> - **Await** được sử dụng để chờ một Promises trong một khối Async, await chỉ có công dụng thực hiện chức năng tạo ra sự không đồng bộ bằng cách chờ 1 khối trả kết quả


```javascript
// Declaration Function

async function run() {
    let promise = new Promise((resolve, reject) => {
      setTimeout(() => resolve(1), 1000)
    });
    let result = await promise; // Đợi cho đến khi promise được hoàn thành
    console.log(result) 
    console.log(2)
    console.log(3)
}
  
run();
```

<details>
<summary>🟢 Terminal</summary>

```javasript
1
2
3
```
</details>

---
<br/><br/>

```javascript
// Arrow Function

let run = async () => {
    let promise = new Promise((resolve, reject) => {
      setTimeout(() => resolve(1), 1000)
    });
    let result = await promise; // Đợi cho đến khi promise được hoàn thành
    console.log(result) 
    console.log(2)
    console.log(3)
}
  
run();
```

<details>
<summary>🟢 Terminal</summary>

```javasript
1
2
3
```
</details>

---
<br/><br/>