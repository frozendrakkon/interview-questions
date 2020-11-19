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

```js
"" + 1 + 0; // 9

"" - 1 + 0; // 10

true + false; // 11

6 / "3"; // 12

"2" * "3"; // 13

4 + 5 + "px"; // 14

"$" + 4 + 5; //15

"4" - 2; //16

"4px" - 2; // 17

7 / 0 = Infinity; // 18

" -9 " + 5; // 19

" -9 " - 5; // 20

null + 1; // 21

undefined + 1; // 22

" \t \n" - 2; //23
```

24.

```js
let a = 0;
alert(Boolean(a)); // false

let b = "0";
alert(Boolean(b)); // true

alert(a == b);
```

25

```js
null == undefined; // 1
null === undefined; // 2
```

26.

```js
alert(null > 0); // (1)
alert(null == 0); // (2)
alert(null >= 0); // (3)
```

_ответы_

1.  - objects
2.  - false и false, потому что объекты сравниваются по ссылкам, а не по значениям внутри них
3.  - Hello
4.  - Ura-a-a-h
5.  - консоль выведет 3, 3, 3, потому что у var область видимости - вся функция. Чтобы исправить нужно поменять var на let.
6.  - undefined
7.  - undefined. Свойство length объекта массива имеет особое поведение. Из-за этого поведения length, когда JavaScript выполняет clothes.length = 0, все элементы массива clothes будут удалены.
8.  - sega. Object.freeze выполнит неглубокую заморозку объекта, но не защитит глубокие свойства от изменения. В этом примере мы не сможем изменить user.age, но у нас нет проблем с изменением user.pet.name. Если мы чувствуем, что нам нужно защитить объект от изменений "полностью вниз", мы можем рекурсивно применить Object.freeze или использовать существующую библиотеку "deep freeze".
9.  - "10"
10. - -1 Вычитание - (как и большинство математических операторов) работает только с числами, пустая строка "" приводится к 0.
11. - 1
12. - 2
13. - 6
14. - "9px"
15. - "\$45"
16. - 2
17. - NaN
18. - infinity
19. - " -9 -5"
20. - -14
21. - 1
22. - NaN
23. - -2
24. - true
25. - 1)true 2)false _при сравнении с числами null - 0, undefined - NaN_ (сравнение null и undefined)
26. - 1)false 2)false 3) true _Причина в том, что нестрогое равенство и сравнения > < >= <= работают по-разному. Сравнения преобразуют null в число, рассматривая его как 0. Поэтому выражение (3) null >= 0 истинно, а null > 0 ложно. С другой стороны, для нестрогого равенства == значений undefined и null действует особое правило: эти значения ни к чему не приводятся, они равны друг другу и не равны ничему другому. Поэтому (2) null == 0 ложно._

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
   - вывести на экран числа, находящиеся под главной диагональю матрицы

7. Используя конструкцию if..else, напишите код, который получает число через prompt, а затем выводит в alert:
   - 1, если значение больше нуля,
   - -1, если значение меньше нуля,
   - 0, если значение равно нулю.
   - Предполагается, что пользователь вводит только числа.

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

**численное преобразование**

- undefined - NaN
- null - 0
- true/false - 1/0

**Логическое преобразование Boolean**

- undefined - false
- number - true, кроме 0 и NaN
- string - true, кроме " "
- object - true
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
