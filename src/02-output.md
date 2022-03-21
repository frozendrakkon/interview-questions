# Что будет выведено?

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
console.log({} + {});
console.log({} - {});
console.log([{}] + [{}]); 
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
[1, 2] + [3, 4];
```

<details>
  <summary>Answer</summary>

  ```
  1,23,4
  ```

</details>
32

```js
++2;

```

<details>
  <summary>Answer</summary>

  ```
  3
  ```

</details>
33

```js
2++;

```

<details>
  <summary>Answer</summary>

  ```
  2
  ```

</details>
34

```js
"5" > 3;

```

<details>
  <summary>Answer</summary>

  ```
  true
  ```

</details>
35

```js
"sega" - 5;

```

<details>
  <summary>Answer</summary>

  ```
  NaN
  ```

</details>
36

```js
  const one = “1”;
  const two = “2”;
  console.log(+one + +two);
```

<details>
  <summary>Answer</summary>

  ```
  3
  ```

</details>
37

```js
  undefined > 0;
```

<details>
  <summary>Answer</summary>

  ```
  false т.к undefined приводит к NaN == false
  ```

</details>
38

```js
  null == undefined;
```

<details>
  <summary>Answer</summary>

  ```
  true
  ```

</details>
39

```js
  null > 0;
```

<details>
  <summary>Answer</summary>

  ```
  false
  ```

</details>
40

```js
  "se" + "ga";
```

<details>
  <summary>Answer</summary>

  ```
  'sega'
  ```

</details>
41

```js
  NaN === NaN;
```

<details>
  <summary>Answer</summary>

  ```
  false
  ```

</details>
42

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

### численное преобразование

- undefined = NaN
- null = 0
- true/false = 1/0

### Логическое преобразование Boolean

Значения, которые приводятся к false: **0, -0, false, NaN, null, undefined, ''**
