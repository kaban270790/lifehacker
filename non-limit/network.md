# Без всяких ограничений кладка `Network`

Открыл сайт через инкогнито в яндекс.браузере с отключеным кэшем.

Файл с профилем загрузки ресурсов [HAR](./lifehacker.ru.har)

Вижу много дублирующих запросов связаных с рекламными сервисами Google и Yandex:

 ![src-1](screenshots-network/Screenshot%20at%20Sep%2027%2020-50-45.png)

 ![src-2](screenshots-network/Screenshot%20at%20Sep%2027%2020-51-44.png)

 ![src-3](screenshots-network/Screenshot%20at%20Sep%2027%2020-52-27.png)
 
 ![src-4](screenshots-network/Screenshot%20at%20Sep%2027%2020-54-51.png)
 

Так же замечено что грузятся много стилей и js файлов, которые возможно
имело место объединить в один или меньшее кол-во файлов:

 ![src-5](screenshots-network/Screenshot%20at%20Sep%2027%2021-13-10.png)
 
Вот к примеру несколько файлов:
 ![src-6](screenshots-network/Screenshot%20at%20Sep%2027%2021-17-24.png)
 
 ![src-7](screenshots-network/Screenshot%20at%20Sep%2027%2021-17-45.png)

Один из документов не был загружен, код ошибки 522:

 ![src-8](screenshots-network/Screenshot%20at%20Sep%2027%2021-35-58.png)
 
Более детально посмотреть на диаграмму заргузки ресурсов относительно времени,
видно что большую часть времени занимает ответ от сервера (зеленая часть полосы ресурса).
Видно что последние из скрина ресурса ожидают загрузку, что бы начать грузиться, тут скорее всего
достигли лимита TCP

 ![src-9](screenshots-network/Screenshot%20at%20Sep%2027%2021-54-45.png)
