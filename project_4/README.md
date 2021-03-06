# project_4
Прогноз оттока клиентов фитнес центра, Python 3

### Основные моменты: 
•	Исследовательский анализ данных (EDA)
•	Модель бинарной классификации клиентов
•	Кластеризация клиентов

### Описание проекта:
Надо сделать прогноз оттока клиентов, использую модель машинного обучения и данных о клиентах фитнес центра.

### Библиотеки: 
pandas / seaborn/ matplotlib / sklearn / scipy / itertools

### Cтатус проекта: 
завершен

### Вывод:
По всем параметрам "Логистическая регрессия" дает результат немного лучше чем "Случайный лес" При построении моделей прогнозирования оттока клиентов были использованы модели "Логистическая регрессия" и "Случайный лес". Обе модели показали отличные результаты - высокий показатель Accuracy (больше 0,91), а также высокие показатели precision и recall (в диапазоне 0,76 - 0,83).

Кластеризация: В результате анализа было принято решение разбить клиентов на 5 кластеров. Судя по метрике Silhouette_score=0.17, - кластеризация прошла плохо.

Результаты:
Кластер 0 - средний - отток 19% (от всего оттока): Живут рядом, 47% от партнеров, 30% промо-кодов, без телефона, контракт на 3-6 месяца, половина групповые занятия посещает, возраст около 29 лет.
Кластер 1 - самый лучший, доля оттока около 9% (от всего оттока) - Живут рядом, из компаний-партнеров, промо-код используют, контракт больше полугода, половина занимается в группах, возраст около 29 лет.
Кластер 2 - плохой, доля оттока довольно велика 28% (от всего оттока): Это те клиенты, которые живут рядом, 24% от партнеров, без промо-кодов, контракт на 1-3 месяца, групповые занятия не посещают, возраст около 28 лет.
Кластер 3 - средний кластер, здесь отток 15% (от всего оттока): Те клиенты, которые Живут рядом, 25% от партнеров, без промо-кодов, контракт на 3-6 месяца, групповые занятия посещают, возраст около 29 лет.
Кластер 4 - плохой, здесь отток 29% (от всего оттока): Это те клиенты, которые живут далеко, контракт на 3 месяца примерно, возраст около 28 лет, промо-код не использовали.

### Автор: 
Татьяна Щур, @taniashchur

Спасибо за материал Яндекс.Практикум
