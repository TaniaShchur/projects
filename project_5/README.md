# project_5
## Анализ поведения пользователей в мобильном приложении, Python 3

### Основные моменты: 
•	Предобработка данных – пропуски, корректировка типов, дубликаты, выбросы.
•	Анализ данных – зависимости, корреляции
•	Анализ воронки/коверсии событий
• Расчет метрики удержания пользователей
•	Проверка гипотез с помощью статистического теста


### Описание проекта:
Доска объявлений для вещей. Надо изучить поведение пользователи мобильного приложения.

### Библиотеки: 
pandas / numpy / plotly / matplotlib / seaborn / math / scipy / datetime

### Cтатус проекта: 
завершен

### Вывод:
Есть данные о действиях 4293 пользователей в мобильном приложении и источники их перехода. Заменили названия столбцов для удобства работы. Пропусков, дубликатов нет. Тип данных заменили только в столбце с временем, также соратили дату до секунд. Проверили на пересекающихся пользователей по источникам, все хорошо, пересечений нет. Также проверили, что пользователи в двух файлах одинаковые. Тут тоже все хорошо. Уифицировали название целевого события и поисков.
Пользователи имеют как самостоятельные события, так и пары связанных событий, например просмотр фотографий и открытие контактов. У них есть множество путей и комбинаций событий в приложении. Поэтому мы можем рассмотреть влияние одного события на последующее. Например, событий просмотра фотографий приводят к целевому событию и другим событиям. Мы также видим, что пользователь иметь несколько сессий, но они состоят только из пары действий.
Фотографии - в сессиях мы видим одно - два события. Возможно, здесь есть что улучшить. Больше фотографий и, возможно более детальных, может заинтересовать пользователя в продукте.
Favorites_add - при достаточно больших периодах поиска было бы удобнее добавлять объявления в отдельный список, чтобы было легче вернуться к ним. Но это событие почти не используется. Возможно, его можно улучшить, сделать более заметным и удобным.
В таблицах выше мы можем видеть какая доля пользователей переходит к следующему действию:
В advert_open переходят часто из advert_open, map, favourites add.
В map из map, search, advert_open
В search из search, contact_show, photos. Переход от звонка снова в поиск может быть, если не договорились с продавцом или не дозвонились.
tips_click из tips_click. Здесь надо учитывать еще tips_show, которое мы убрали из выборки.
В photos из photos, call, favourites, search.
В favourites add из favourites, photos и contacts_show.
В contacts_call из contacts_call, contacts_show
Очень низкая конверсия у событий favorites_add, map, tips_click. Возможно, эти события можно сделать более удобными для пользователя.
Графики удержания показывают ,что в приложении лучше остаются пользователи, которые нашли то, что искали. Поэтому имеет смысл улучшать работу приложения и помогать пользователю находить, то, что он ищет. Возможно стоит изучить запрос сессий, которые не были успешными. Может быть есть продукты, которых в приложении еще нет.
Мы рассмотрели две гипотезы и пришли к выводам:
Конверсия в просмотры контактов различается у этих двух групп.
Конверсия в просмотры фотографий равна у этих двух групп

### Рекомендации:

В данных было 7 видов события search. Если между ними есть разница, то ее лучше уточнить для дальнейшей корректной работы.
Пользователи наиболее активны в период примерно с 9 утра до 24 часов. Размещение новых объявлений, возможно, стоит проводить в это время.
В данных было достаточно много событий между которыми разница по времени составляла 0 секунд. Лучше уточнить причину таких событий.
Фотографии хорошо конвертируются в фотографии. У пользователя одно - два фото события в сессии. Возможно, было бы полезно добавить больше фотографий, детальных, чтобы заинтересовать пользователя.
событие favorites_add, возможно, надо улучшить, сделать более заметным и удобным.
Надо проверить событие contacts_call. Были ли случаи недозвона? Возможно это событие можно улучшить.
Посмотреть поисковые запросы в неуспешных сессиях на предмет новых товаров, слов/фраз. Возможно, получится улучшить результаты поиска. Удержание успешных пользователей лучше.

### Автор: 
Татьяна Щур, @taniashchur

Спасибо за материал Яндекс.Практикум
