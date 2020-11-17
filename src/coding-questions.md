# СODGOD

**Что выведет?**

1.

```javascript
console.log(typeof null);
```

2.

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

3.

```js
let s = "Hello";
const F = (a) => {
  a = "Ura-a-a-h";
};
F(s);
console.log(s);
```

4.

```js
const o = { s: "Hello" };
const G = (obj) => {
  obj.s = "Ura-a-a-h";
};
G(o);
console.log(o.s);
```

5.

```js
for (var i = 0; i < 3; i++) {
  setTimeout(function () {
    console.log(i);
  }, 0);
} // как это поправить?
```

6.

```js
var i = 10;
function foo(i) {
  console.log(i);
}
foo();
```

7.

```js
const clothes = ["jacket", "t-shirt"];
clothes.length = 0;
console.log(clothes[0]);
```

8.

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

_ответы_

1. - objects
2. - false и false, потому что объекты сравниваются по ссылкам, а не по значениям внутри них
3. - Hello
4. - Ura-a-a-h
5. - консоль выведет 3, 3, 3, потому что у var область видимости - вся функция. Чтобы исправить нужно поменять var на let.
6. - undefined
7. - undefined. Свойство length объекта массива имеет особое поведение. Из-за этого поведения length, когда JavaScript выполняет clothes.length = 0, все элементы массива clothes будут удалены.
8. - sega. Object.freeze выполнит неглубокую заморозку объекта, но не защитит глубокие свойства от изменения. В этом примере мы не сможем изменить user.age, но у нас нет проблем с изменением user.pet.name. Если мы чувствуем, что нам нужно защитить объект от изменений "полностью вниз", мы можем рекурсивно применить Object.freeze или использовать существующую библиотеку "deep freeze".

**Задачи**

1. Есть массив чисел, нужно найти максимальное число
2. Есть список строк, найти те, которые являются палиндромами
3. Напишите рекурсивную функцию на примере поиска чисел Фибоначчи. На вход функция получает порядковый номер числа, а возвращает само число
4. Развернуть одномерный массив без создания дополнительного массива [1, 2, 3 ,4] => [4, 3, 2, 1]
5. Напишите решение задачи FizzBuzz

6. Есть матрица

   - [ [1, 4, 8, 9,],
   - [6, 2, 11, 1,],
   - [8, 0, 3, -5,],
   - [-2, 10, 8, 1] ]`

Вывести на экран числа, находящиеся под главной диагональю матрицы

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
null === undefined; // true
null > 0; // true
"se" + "ga"; // sega
NaN === NaN; //false
```

_Логическое преобразование Boolean_

- undefined - false
- number - true, кроме 0 и NaN
- string - true, кроме " "
- object - true

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
