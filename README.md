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