# shikitheme
Все цвета можно изменить в :root, каждая строчка подписана поэтому сложностей возникнуть не должно. 
Фон сайта и шапка профиля меняются там же.
Чтобы добавить вкладки в поле "Обо мне", нужно вставить этот код:

```scss
[div=u-tabs to-process data-dynamic=tabs]
  [div]
    [div=active data-tab-switch]Кнопка вкладки №1[/div]
    [div data-tab-switch]Кнопка вкладки №2[/div]
    [div data-tab-switch]Кнопка вкладки №3[/div]
  [/div]
  [div data-tab]Содержимое вкладки №1[/div]
  [div=hidden data-tab]Содержимое вкладки №2[/div]
  [div=hidden data-tab]Содержимое вкладки №3[/div]
[/div]
```
Дополнительные классы для u-tabs:
Класс --ripple добавляет эффект наведения на вкладку.
Класс --centered располагает горизонтальные вкладки по центру.

Виды u-tabs:
Класс --vertical делает вкладки вертикальными при @media (min-width: 960px).
(класс --right перемещает боковые вкладки вправо)
Класс --anorva делает вкладки как у @anorva. :advise:

P.S. Классы указываются так:
[div=u-tabs --ripple --centered --vertical to-process data-dynamic=tabs]
(после u-tabs, через пробел, без точек)

Добавить иконку к кнопке или вкладке достаточно просто:

Иконка в обычной кнопке
[div=b-button data-icon=monetization_on]Текст кнопки[/div]

Иконка в кнопке переключения вкладок
[div data-tab-switch data-icon=palette]Текст вкладки[/div]
