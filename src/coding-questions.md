# СODGOD

**Что выведет? Объясните почему**
```javascript
console.log(typeof null);
// Object
```

```js
var a = {
  name: "test",
};
var b = {
  name: "test",
};
a == b;
a === b;
//  false, false
```

```js
let word = "Hello";
const test = (a) => {
  a = "Ura-a-a-h";
};
test(word);
console.log(word);
// Hello
```

```js
const o = { s: "Hello" };
const G = (obj) => {
  obj.s = "Ura-a-a-h";
};
G(o);
console.log(o.s);
// Ura-a-a-h
```

```js
for (var i = 0; i < 3; i++) {
  setTimeout(function () {
    console.log(i);
  }, 0);
} 
// как это поправить?
// 3, 3, 3
// Чтобы поправить - поменять var на let
```

```js
var i = 10;
function foo(i) {
  console.log(i);
}
foo();
// undefined
```

```js
const clothes = ["jacket", "t-shirt"];
clothes.length = 0;
console.log(clothes[0]);
// undefined
```

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
// sega
```

```js
"" + 1 + 0; // '10'

"" - 1 + 0; // -1

true + false; // 1

6 / "3"; // 2

"2" * "3"; // 6

4 + 5 + "px"; // '9px'

"$" + 4 + 5; '$45'

"4" - 2; // 2

"4px" - 2; // 17

7 / 0 // Infinity

" -9 " + 5; // ' -9 5'

" -9 " - 5; // -14

null + 1; // 1

undefined + 1; // NaN

" \t \n" - 2; // -2
```

```js
let a = 0;
alert(Boolean(a)); // false

let b = "0";
alert(Boolean(b)); // true

alert(a == b);
// true
```

```js
null == undefined; // true
null === undefined; // false
```

```js
alert(null > 0); // false
alert(null == 0); // false
alert(null >= 0); // true
```

```js
let i = 0;
while (++i < 5) alert(i); // 1,2,3,4

let i = 0;
while (i++ < 5) alert(i); // 1,2,3,4,5
```

```js
function sayHi() {
  alert("Привет");
}

alert(sayHi()); // привет, потом undefined
```

```js
function sayHi() {
  alert("Привет");
}

let func = sayHi;

func(); // Привет
sayHi(); // Привет
```

```js
console.log({} + {}) // "[object Object][object Object]"
console.log({} - {}) // NaN
console.log([{}] + [{}]) // "[object Object][object Object]"
}
```
31.

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

**Задачи**

1. Есть массив чисел, нужно найти максимальное число

2. Есть список строк, найти те, которые являются палиндромами

3. Напишите рекурсивную функцию на примере поиска чисел Фибоначчи. На вход функция получает порядковый номер числа, а возвращает само число

4. Развернуть одномерный массив без создания дополнительного массива [1, 2, 3 ,4] => [4, 3, 2, 1]

5. Напишите решение задачи FizzBuzz

6. Напишите цикл, который предлагает prompt ввести число, большее 100. Если посетитель ввёл другое число – попросить ввести ещё раз, и так далее.

7. Напишите код, который выводит все простые числа из интервала от 2 до n.

8. Есть матрица

   - [ [1, 4, 8, 9,],
   - [6, 2, 11, 1,],
   - [8, 0, 3, -5,],
   - [-2, 10, 8, 1] ]`
   - вывести на экран числа, находящиеся под главной диагональю матрицы

9. Используя конструкцию if..else, напишите код, который получает число через prompt, а затем выводит в alert:

   - 1, если значение больше нуля,
   - -1, если значение меньше нуля,
   - 0, если значение равно нулю.
   - Предполагается, что пользователь вводит только числа.

10. - Есть объект salaries, в котором указаны зарплаты сотрудников - sergei: 500, roma: 300... Нужно написать код, который суммирует зарплаты всех сотрудников, если объект пустой, то возвращается 0

11. - Создайте функцию multiplyNumeric(obj), которая умножает все числовые свойства объекта obj на 2, не числовые оставляет без изменений.

12. - Создайте объект calculator (калькулятор) с тремя методами:
    - read() (читать) запрашивает два значения и сохраняет их как свойства объекта.
    - sum() (суммировать) возвращает сумму сохранённых значений.
    - mul() (умножить) перемножает сохранённые значения и возвращает результат.

    ```js
    let calculator = {
      // ... ваш код ...
    };

    calculator.read();
    alert(calculator.sum());
    alert(calculator.mul());
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
