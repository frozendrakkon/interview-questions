# HTML

1. **Что делает doctype?**

2. **как обслуживать страницу на нескольких языках?**

3. **Чего следует опасаться при проектировании или разработке многоязычных сайтов?**

4. **Для чего нужны data-атрибуты?**

5. **Рассматривайте HTML как открытую веб-платформу. Какие строительные блоки есть у HTML?**

6. **Опишите разницу между cookie, sessionStorageи localStorage.**

   _Cookie_

   > - Инициатор: клиент или сервер. Сервер может использовать заголовок Set-Cookie.
   > - Срок хранения: устанавливается вручную.
   > - Хранение между сессиями: зависит от установки срока хранения.
   > - Связь с доменом: да.
   > - Отправка на сервер с каждым HTTP-запросом: автоматически, с помощью заголовка Cookie.
   > - Емкость, на один домен: 4 КБ.
   > - Доступность: в любом окне.

   _Local Storage:_

   > - Инициатор: клиент.
   > - Срок хранения: всегда.
   > - Хранение между сессиями: да.
   > - Связь с доменом: нет.
   > - Отправка на сервер с каждым HTTP-запросом: нет.
   > - Емкость, на один домен: 5 МБ.
   > - Доступность: в любом окне.

   _Session Storage:_

   > - Инициатор: клиент.
   > - Срок хранения: до закрытия вкладки.
   > - Хранение между сессиями: нет.
   > - Связь с доменом: нет.
   > - Отправка на сервер с каждым HTTP-запросом: нет.
   > - Емкость, на один домен: 5 МБ.
   > - Доступность: в той же вкладке.

7. **Опишите разницу между _script_, _script async_ и _script defer_.**

8. **Почему обычно рекомендуется размещать CSS _link_ между _head_ _/head_ и JS _script_ непосредственно перед этим _/body_ ? Вы знаете исключения?**

9. **Что такое прогрессивный рендеринг?**
   Прогрессивный рендеринг - имя, данное технологиям, используемым для ускорения отрисовки страниц

Ленивая загрузка картинок. Картинки на странице не загружаются все разом. JavaScript подгрузит картинки тогда, когда пользователь доскроллит до той части страницы, на которой они расположены.
Приоритизация видимого контента. Только минимум CSS, контента, скриптов, необходимых для отрисовки той части страницы, которую пользователь увидит первой. Вы можете использовать отложенные скрипты или слушать события DOMContentLoaded или load, чтобы загрузить остальные ресурсы и контент.
Асинхронные фрагменты HTML. Отправка в браузер частей HTML-страницы, созданной на бэкенде.

10. **Зачем использовать srcsetатрибут в теге изображения? Объясните процесс, который использует браузер при оценке содержимого этого атрибута.**

11. **В чем разница между canvasи svg?**
    | Svg | Canvas
    | ------------- |:------------------
    | SVG действует по принципу «нарисовал и запомнил». Другими словами любая фигура, нарисованная с помощью SVG, запоминается, допускает манипуляции над собой, и браузер может нарисовать её снова. | Canvas действует по принципу «нарисовал и забыл». После того, как что-то нарисовано, вы не можете получить доступ к этому изображению и манипулировать им.
    | SVG подходит для создания графики такой, как в программах CAD, где пользователь может манипулировать однажды нарисованным изображением. | Canvas хороша для сценариев «нарисовал и забыл», таких как анимация и игры.
    | Медленный формат, т.к. ему требуется запоминать координаты для будущих манипуляций. | Более быстрый формат, т.к. нет надобности запоминать что-либо.
    | Мы можем создать обработчик событий, связанный с нарисованным объектом. | В этом случае мы не можем привязать обработчик событий к объектам рисунка, т.к. у нас нет ссылки на них.
    |Не зависит от разрешения. | Зависит от разрешения.
    |

12. **Что такое HTML?**

13. **Отличия Div от Span**
14. **что такое svg-изображения**
15. **Что такое XML, в чем отличия от HTML?**
16. **Как добиться кроссбраузерности и валидности?**
17. **что такое DOM дерво?**
