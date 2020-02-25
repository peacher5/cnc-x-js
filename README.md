## CNC X JS

### หัวข้อทั้งหมด

- [Let's say 'Hello World!'](lets-say-hello-world)
- [Data Types](#data-types)
- [Operators](#operators)
- [การประกาศตัวแปร](#การประกาศตัวแปร)
- [เงื่อนไข](#เงื่อนไข)
- [Loop](#loop)
- [Function](#function)
- [List](#list)

### ติดตั้ง NodeJS

https://nodejs.org

## Let's say 'Hello World!'

```js
console.log('Hello World!')
```

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

#### หากไม่ใส่ {} จะ return statement นั้นให้เลย

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
                         // map จะ return list ใหม่ ไม่ไปแก้ list เดิม
```

#### filter

```js
numbers = [1, 3, 5, 7, 9]
numbers.filter(n => n != 5) // [1, 3, 7, 9]
                            // filter จะ return list ใหม่ ไม่ไปแก้ list เดิม
```
