## CNC X JS

### หัวข้อทั้งหมด

- [Let's say 'Hello World!'](lets-say-hello-world)
- [Data Types](#data-types)
- [Operators](#operators)
- [การประกาศตัวแปร](#การประกาศตัวแปร)
- [เงื่อนไข](#เงื่อนไข)
- [Loop](#loop)
- [String](#string)
- [Function](#function)
- [List](#list)
- [Object](#object)

### ติดตั้ง Node.js

https://nodejs.org

## Let's say 'Hello World!'

```js
console.log('Hello World!')
```

### วิธี run ด้วย Node.js

- save ไฟล์เป็นนามสกุล `.js`
- ใช้คำสั่ง `node` ตามด้วยชื่อไฟล์ เช่น `node main.js`

## Data Types

### Data type ที่มีค่า

- string
- number
- boolean (true, false)
- object
- function

### Data type ที่ไม่มีค่า

- null
- undefined

## Operators

```js
==   // ไม่ค่อยใช้
!=   // ไม่ค่อยใช้
===
!==
>
<
>=
<=
++
--
```

### == กับ ===

```js
console.log(20 == '20')   // true
console.log(20 === '20')  // false
```

## การประกาศตัวแปร

- var (ไม่ใช้)
- **let**
- **const**

### let

สร้างตัวแปรที่สามารถ assign ค่าให้ใหม่ได้

```js
let message = 'hello'
message = 'hi
```

### const

สร้างตัวแปรที่**ไม่สามารถ** assign ค่าให้ใหม่ได้

```js
const message = 'hello'
message = 'hi' // Error
```

## เงื่อนไข

### if-else

```js
if (2 + 3 === 5) {
    console.log('Yes')
} else {
    console.log('No')
}
```

### if-else (short form)

```js
console.log(2 + 3 === 5 ? 'Yes' : 'No')
```

### switch
```js
switch (answer) {
  case 'YES':
    console.log('Sure.')
    break;
  case 'NO':
    console.log('No? ok.')
    break;
  default:
    console.log('what?')
}
```

## Loop

### while loop

```js
let i = 0

while (i < 5) {
    console.log(i)
    i++
}
```

### for loop

```js
for (let i = 0; i < 5; i++) {
    console.log(i)
}
```

## String

### ประกาศ String

```js
const dept1 = 'Computer Science'
const dept2 = "Computer Science"
const dept3 = `Computer Science`
```

> single quote (') กับ double quote (") เหมือนกัน

> back quote (`) สามารถทำ template string ได้

### Template String

สามารถแทรกตัวแปรหรือ expression ลงใน string ได้โดยใช้ `${}` อยู่ภายใน ``` `` ```

```js
const result = 2 * 5

console.log(`2 x 5 = ${result}`)
// ให้ผลลัพธ์เหมือนกับ
console.log('2 x 5 = ' + result)
```

### String Methods

```js
const txt = 'Hello World'
```

#### นับความยาว string

```js
txt.length
```

#### [ดู method อื่น ๆ](https://www.w3schools.com/js/js_string_methods.asp)

## Function

### Function ปกติ

```js
function add(a, b) {
    return a + b
}

console.log(add(2, 3))
```

### Arrow Function

```js
const add = (a, b) => {
    return a + b
}

console.log(add(2, 3))
```

#### หากไม่ใส่ {} จะ return คำสั่งนั้นให้เลย

```js
const add = (a, b) => a + b

console.log(add(2, 3))
```

## List

```js
const numbers = [20, 40, 60]
```

```js
const anythingJingleBell = ['abc', 20, 3.14, true]
```

#### เข้าถึงค่าใน list ตาม index

```js
console.log(numbers[0])
```

#### เปลี่ยนค่าใน list ตาม index

```js
numbers[0] = 'xyz'
```

#### ดูขนาดของ list

```js
numbers.length
```

#### เพิ่ม element ใน list

```js
numbers.push('Hello')
```

#### ลบ element ใน list

```js
numbers.pop() // ลบตัวสุดท้าย
```

```js
numbers.splice(2, 1) // ลบตั้งแต่ index ที่ 2 ไป 1 ตัว
```

#### วนดู element ใน list

#### for i

```js
for (let i = 0; i < numbers.length; i++) {
    console.log(numbers[i])
}
```

#### for in

```js
for (const i in numbers) {
    console.log(numbers[i])
}
```

#### for of

```js
for (const n of numbers) {
    console.log(n)
}
```

#### forEach

```js
numbers.forEach(n => console.log(n))
```

#### map

```js
numbers = [1, 2, 3, 4]
numbers.map(n => n * 10) // [10, 20, 30, 40]
```

> map จะ return list ใหม่ ไม่ไปแก้ list เดิม

#### filter

```js
numbers = [1, 3, 5, 7, 9]
numbers.filter(n => n != 5) // [1, 3, 7, 9]
```

> filter จะ return list ใหม่ ไม่ไปแก้ list เดิม

### List เป็น Mutable

```js
const numbers = [1, 2, 3]
const otherNumbers = numbers

console.log('Before: ' + numbers) // Before: [1, 2, 3]

otherNumbers[1] = 9

console.log('After: ' + numbers) // After: [1, 9, 3]
```


## Object

สามารถเก็บค่าหลาย ๆ ค่าไว้ใน object ได้ในรูปแบบ key-value pair

### สร้าง object

```js
const student = {
    id: '6010405360',
    name: 'Peach',
    university: 'KU'
}
```

### เข้าถึงค่าใน object

```js
console.log(student.name)
// หรือ
console.log(student['name'])
```

### เพิ่มค่าใน object

```js
student.dept = 'CS'
// หรือ
student['dept'] = 'CS'
```

### แก้ไขค่าใน object

```js
student.name = 'Peranut W.'
// หรือ
student['name'] = 'Peranut W.'
```

### Object เป็น Mutable

```js
const std2 = student

console.log('Before: ' + student.id) // Before: 6010405360

std2.id = '1234'

console.log('After: ' + student.id) // After: 1234
```
