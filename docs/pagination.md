Пагинация
===

Инфо о пагинации отправляется в виде GET-параметров `page`, `per-page`, `offset`.

## GET-параметры

### Текущая страница (Page number)

Пример:

```json
{
	"page": {
        "number": 3
    }
}
```

### Размер страницы (Page size)

Пример:

```json
{
    "page": {
        "size": 15
    }
}
```

### Смещение выборки (Offset)

Смещение может поддерживаться не везде.

Пример:

```json
{
    "page": {
        "offset": 7
    }
}
```

Начнет выборку 15-той сущности. Это может быть полезно для *Lazy load*.

## Получаемые заголовки

* X-Pagination-Total-Count - Количество всех сущностей
* X-Pagination-Page-Count - Количество страниц
* X-Pagination-Per-Page - Количество сущностей на страницу
* X-Pagination-Current-Page - Текущая страница
* X-Pagination-Offset - Смещение
