# Code Questions

## Что будет в консоли? Объясните почему

1

```javascript
console.log(typeof null);
```

<details>
  <summary>Answer</summary>

  ```
  Object
  ```

</details>

2

```js
var a = {
  name: "test",
};
var b = {
  name: "test",
};
a == b;
a === b;
```

<details>
  <summary>Answer</summary>

  ```
  false
  false
  ```

</details>

3

```js
let word = "Hello";
const test = (a) => {
  a = "Ura-a-a-h";
};
test(word);
console.log(word);
// Hello
```

<details>
  <summary>Answer</summary>

  ```
  Hello
  ```

</details>
4

```js
const o = { s: "Hello" };
const G = (obj) => {
  obj.s = "Ura-a-a-h";
};
G(o);
console.log(o.s);
// Ura-a-a-h
```

<details>
  <summary>Answer</summary>

  ```
  Ura-a-a-h
  ```

</details>
5

```js
for (var i = 0; i < 3; i++) {
  setTimeout(function () {
    console.log(i);
  }, 0);
} 
// почему так происходит, и как это поправить?
```

<details>
  <summary>Answer</summary>

  ```
  3, 3, 3
  Чтобы поправить - поменять var на let
  ```

</details>
6

```js
var i = 10;
function foo(i) {
  console.log(i);
}
foo();
```

<details>
  <summary>Answer</summary>

  ```
  undefined
  ```

</details>
7

```js
const clothes = ["jacket", "t-shirt"];
clothes.length = 0;
console.log(clothes[0]);
```

<details>
  <summary>Answer</summary>

  ```
  undefined
  ```

</details>
8

```js
const user = {
  name: "Joe",
  age: 25,
  pet: {
    type: "dog",
    name: "Buttercup",
  },
};

Object.freeze(user);
user.pet.name = "sega";
console.log(user.pet.name);
```

<details>
  <summary>Answer</summary>

  ```
  sega
  ```

</details>
9

```js
"" + 1 + 0;
```

<details>
  <summary>Answer</summary>

  ```
  '10'
  ```

</details>
10

```js
"" - 1 + 0;
```

<details>
  <summary>Answer</summary>

  ```
  -1
  ```

</details>
11

```js
true + false;
```

<details>
  <summary>Answer</summary>

  ```
  1
  ```

</details>
12

```js
6 / "3";
```

<details>
  <summary>Answer</summary>

  ```
  2
  ```

</details>
13

```js
"2" * "3";
```

<details>
  <summary>Answer</summary>

  ```
  6
  ```

</details>
14

```js
4 + 5 + "px";
```

<details>
  <summary>Answer</summary>

  ```
  '9px'
  ```

</details>
15

```js
"$" + 4 + 5;
```

<details>
  <summary>Answer</summary>

  ```
  '$45'
  ```

</details>
16

```js
"4" - 2;
```

<details>
  <summary>Answer</summary>

  ```
  2
  ```

</details>
17

```js
"4px" - 2;
```

<details>
  <summary>Answer</summary>

  ```
  NaN
  ```

</details>
18

```js
7 / 0;
```

<details>
  <summary>Answer</summary>

  ```
  infinity
  ```

</details>
19

```js
" -9 " + 5;
```

<details>
  <summary>Answer</summary>

  ```
  '-9 5'
  ```

</details>
20

```js
" -9 " - 5;
```

<details>
  <summary>Answer</summary>

  ```
  -14
  ```

</details>
21

```js
null + 1;
```

<details>
  <summary>Answer</summary>

  ```
  1
  ```

</details>
22

```js
undefined + 1;
```

<details>
  <summary>Answer</summary>

  ```
  NaN
  ```

</details>
23

```js
" \t \n" - 2;
```

<details>
  <summary>Answer</summary>

  ```
  -2
  ```

</details>
24

```js
let a = 0;
alert(Boolean(a));

let b = "0";
alert(Boolean(b));

alert(a == b);
```

<details>
  <summary>Answer</summary>

  ```
  false
  true
  true
  ```

</details>

25

```js
null == undefined;
null === undefined;
```
<details>
  <summary>Answer</summary>

  ```
  true
  false
  ```

</details>

26

```js
alert(null > 0);
alert(null == 0);
alert(null >= 0);
```

<details>
  <summary>Answer</summary>

  ```
  false
  false
  true
  ```

</details>

27

```js
let i = 0;
while (++i < 5) alert(i);

let i = 0;
while (i++ < 5) alert(i);
```

<details>
  <summary>Answer</summary>

  ```
  1,2,3,4
  1,2,3,4,5
  ```

</details>

28

```js
function sayHi() {
  alert("Привет");
}

alert(sayHi());
```

<details>
  <summary>Answer</summary>

  ```
  Привет, потом undefined
  ```

</details>

29

```js
function sayHi() {
  alert("Привет");
}

let func = sayHi;

func();
sayHi();
```

<details>
  <summary>Answer</summary>

  ```
  Привет
  Привет
  ```

</details>

30

```js
console.log({} + {}) // "[object Object][object Object]"
console.log({} - {}) // NaN
console.log([{}] + [{}]) // "[object Object][object Object]"
}
```

<details>
  <summary>Answer</summary>

  ```
  [object Object][object Object]
  NaN
  [object Object][object Object]
  ```

</details>

31

```js

console.log( ({}).prototype === ({}).__proto__ ) // false

function some() {}
console.log( some.prototype === some.__proto__)  // false

function someOne() {} 
function someTwo() {}
console.log(someOne.__proto__ === someTwo.__proto__) // true
console.log(someOne.prototype === someTwo.prototype) // false

let Component = (props) => { 
  return '<div> Hi </div>'
}
console.log(Component.prototype === Object.prototype) // false

let age = 18
console.log(age.prototype === Number.prototype) // false
console.log(age.__proto__ === Number.prototype) // true

class Hacker {} 
console.log(Hacker.__proto__ === Function.prototype) // true

```


**Приведение типов**

```js
"1" + 2; //12
"7" + "7"; //14
[1, 2] + [3, 4]; //1,23,4
++2; // 3
2++; // 2
"5" > 3; // true
"sega" - 5; //NaN


const one = “1”;
const two = “2”;
console.log(+one + +two) // 3

undefined > 0; //false т.к undefined приводит к NaN == false
null == undefined; // true
null > 0; // false
"se" + "ga"; // sega
NaN === NaN; // false
```

**численное преобразование**

- undefined = NaN
- null = 0
- true/false = 1/0

**Логическое преобразование Boolean**

- undefined = false
- number = true, кроме 0 и NaN
- string = true, кроме ""
- object = true
- "0" === true

  **Работа с массивами**

```js
let cars = ["Honda", "Toyota", "Feat", "Opel"];
let nums = [1, 1, 1, 1, 2, 2, 2, 3, 3, 3, 55, 70];
let nums2 = [1, 4, 3, 5, 6, 2, 10, 35];
let arr = [0, false, undefined, null, "", true, 1, "sss", NaN];

// сумма чисел массива
let sum = nums.reduce((x, y) => x + y);
console.log(sum);

//удалить ложные значения в массиве
let newArr = arr.filter(Boolean);
console.log(newArr);

// конвертировать массив в объект
let obj = { ...cars };
console.log(obj);

// Удалить повторяющиеся элементы в массиве
let uniNums = [...new Set(nums)];

// Заменить значение в массиве
cars.splice(0, 2, "Nissan", "Tesla");
console.log(cars);

// перебор массива без метода map
let newCars = [
  { car: "Honda", color: "Red" },
  { car: "Toyota", color: "Green" },
  { car: "Feat", color: "Yellow" },
  { car: "Tesla", color: "Pink" },
];
let carName = Array.from(newCars, ({ car }) => car);
console.log(newCars);

// Очистить массив
nums.splice(0, nums.length);
console.log(nums);

// найти пересечения массивов из чисел
let newNums = [...new Set(nums)].filter((item) => nums2.includes(item));
console.log(newNums);

// найти индекс последнего вхождения числа
let lastIndex = nums.lastIndexOf(1);
console.log(lastIndex);

// способ создания массива с одинаковыми элементами
let newArr = new Array(10).fill(1);

// найти случайное число из массива
let randomNum = nums2[Math.floor(Math.random() * nums2.length)];
console.log(randomNum);
```
