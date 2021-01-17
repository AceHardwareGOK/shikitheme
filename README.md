# shikitheme
Установка темы происходит путём добавления всего одной строчки в стилях сайта:
```scss
@import url(https://raw.githubusercontent.com/AceHardwareGOK/shikitheme/main/shiki-pink.css);
```
Для изменени цветов достаточно добавить:
```scss
:root {
  /*цвет верхней панели и т.д*/
  --maincolor: #D94086;
  /*цвет выпадающих меню*/
  --subcolor: linear-gradient(var(--maincolor), #AE4FCE);
  /*цвет рамки выпадающих меню*/
  --subborder: #fff;
  /*цвет текста выпадающих панелей при наведении*/
  --subfonthover: #000;
  /*цвет фона выпадающих панелей при наведении*/
  --subbackhover: #fff;
  /*цвет всех ссылок*/
  --fontcolor: #F672DF;
  /*цвет ссылок при наведении*/
  --hoverfont: #B050CD;
  /*цвет ссылок при нажатии*/
  --activefont: #9BACDE;
  /*цвет рамки в колекциях при наведении, фоны под текстом*/
  --collectionshover: #FFDDF7;
  /*fix*/
  --link-color: var(--fontcolor);
  /*фон жанров и разных текстовых полей*/
  --backgenre: #fff;
  /*цвет текста в поле поиска*/
  --sfontcolor: grey;
  /*цвет кнопок*/
  --buttoncolor: #F0ADF0;
  /*цвет кнопок при наведении*/
  --buttonhover: #F672DF;
  /*основной цвет графиков (вписывать только цифры без скобок), остальные сами подберутся*/
  --graphmain: 217, 64, 134;
  /*цвет самого тёмного графика*/
  --graph0: rgb(var(--graphmain));
  /*цвет графика посветлее*/
  --graph1: rgba(var(--graphmain),0.8);
  /*цвет ещё более светлого графика*/
  --graph2: rgba(var(--graphmain),0.6);
  /*цвет самого светлого графика*/
  --graph3: rgba(var(--graphmain),0.3);
  /*цвет самого тёмного графика при наведении*/
  --graph0hover: var(--graph3);
  /*цвет графика посветлее при наведении*/
  --graph1hover: var(--graph2);
  /*цвет ещё болле светлого графика при наведении*/
  --graph2hover: var(--graph1);
  /*цвет самого светлого графика при наведении*/
  --graph3hover: var(--graph0);
  /*цвет при наведении на кнопки вкладок*/
  --color-overlay-text-hovered: rgba(33, 33, 33, 0.04);
  /* Обложка профиля */
  --user-cover: url(https://64.media.tumblr.com/3211b73c9b32b062261d164039e9fcf5/1c1af52e6a2b68f3-b9/s1280x1920/54dfc22c11b43f12d04168433f3032a5cbe1dbf4.png);
  /* Фон сайта */
  --user-background: url(https://i.imgur.com/bz26Puf.png);
  /*цвет обводки*/
  --bordercolor: var(--fontcolor);
  /*подпись внизу*/
  --text: 'Пусть у каждого прочитавшего родится бабушка';
}
```
Каждая строчка подписана поэтому сложностей возникнуть не должно. 
Фон сайта и шапка профиля меняются там же.
***
### Вкладки:

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
* ```--ripple``` добавляет эффект наведения на вкладку.
*  ```--centered``` располагает горизонтальные вкладки по центру.

Виды ```u-tabs```:
* ```--vertical``` делает вкладки вертикальными при ```@media (min-width: 960px)```.
* ```--right``` перемещает боковые вкладки вправо.
* ```--anorva``` меняет вид вкладок.

P.S. Классы указываются так:
```scss
[div=u-tabs --ripple --centered --vertical to-process data-dynamic=tabs]
```
(после ```u-tabs```, через пробел, без точек)

Добавить иконку к кнопке или вкладке достаточно просто:

Иконка в обычной кнопке:
```scss
[div=b-button data-icon=monetization_on]Текст кнопки[/div]
```

Иконка в кнопке переключения вкладок:
```scss
[div data-tab-switch data-icon=palette]Текст вкладки[/div]
```
Список иконок: [material.io](https://material.io/resources/icons/?style=baseline)
***
### Постеры:
``` 
[div=rate_module cc-6]
[div=c-column][animes ids=2966 cover_notice=studio][b]93/100[/b][/div]
[div=c-column][mangas ids=36131][b]86/100[/b][/div]
[div=c-column][mangas ids=90125][b]91/100[/b][/div]
[div=c-column][mangas ids=9115][b]100/100[/b][/div]
[div=c-column][people ids=79][b]Ками-сама[/b][/div]
[div=c-column][characters ids=7373][b]Богиня ❤[/b][/div]
[/div]
```
Количество колонок указывается в контейнере ```rate_module```. Поддерживаются колонки от 6 (```cc-6```) до 9 (```cc-9```).

Чтобы добавить новый постер, необходимо внутрь контейнера ```rate_module``` добавить новую строчку с кодом:
```[div=c-column][mangas ids=9115][b]100/100[/b][/div]```
где:
* ```[div=c-column][/div]``` – обязательный контейнер, в котором расположены постер и надпись.
* ```[mangas ids=9115]``` – код конкретного постера. Указывать можно только один id!
* ```[b]100/100[/b```] – произвольная надпись.

Также можно добавить блок текста, почти как в коллекциях:

```[div=c-column][mangas ids=9115][div=text]Произвольный текст[/div][b]100/100[/b][/div]```

А класс ```user-defined``` зафиксирует при клике текст в развернутом виде:

```[div=c-column][mangas ids=9115][div=text user-defined]Произвольный текст[/div][b]100/100[/b][/div]```

***
[Очистка кеша на шикимори (если изменения не применяются)](https://shikimori.one/tests/reset_styles_cache?url=)
