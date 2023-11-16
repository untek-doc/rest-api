Пагинация
===

Инфо о пагинации отправляется в виде GET-параметров в ассоциативном массиве `page`.

## GET-параметры

### Текущая страница (Page number)

Например URI:

    /v1/post?page[number]=2

### Размер страницы (Page size)

Например URI:

    /v1/post?page[size]=2

### Смещение выборки (Offset)

Смещение может поддерживаться не везде.

Например URI:

    /v1/post?page[offset]=2

Начнет выборку 15-той сущности. Это может быть полезно для *Lazy load*.

## Получаемые заголовки

* X-Pagination-Total-Count - Количество всех сущностей
* X-Pagination-Page-Count - Количество страниц
* X-Pagination-Per-Page - Количество сущностей на страницу
* X-Pagination-Current-Page - Текущая страница
* X-Pagination-Offset - Смещение
