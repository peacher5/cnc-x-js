## CNC X JS

### ติดตั้ง NodeJS

https://nodejs.org

### Let's say 'Hello World!'

```js
console.log('Hello World!')
```

## Operators

```js
==   // ไม่ใช้
!=   // ไม่ใช้
===
!==
>
<
>=
<=
++
--
```

### Example

```js
20 == '20'
20 === '20'
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

### Function

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
numberss.plice(2, 1) // ลบตั้งแต่ index ที่ 2 ไป 1 ตัว
```

#### วนดู element ใน list

```js
for (let i = 0; i < numbers.length; i++) {
    console.log(numbers[i])
}
```

```js
for (const i in numbers) {
    console.log(numbers[i])
}
```

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
numbers.map(n => n * 10)
```

#### filter

```js
numbers = [1, 3, 5, 7, 9]

numbers.map(n => n != 5)
```
