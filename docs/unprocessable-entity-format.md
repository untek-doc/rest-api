# Формат ошибки валидации данных

Ошибки ввода пользовательских данных отдается в виде массива объектов
с указанием поля и сообщения об ошибке.

Например:

```json
{
    "title": "Unprocessable entity",
    "message": "User input error",
    "errors": [
        {
            "field": "amount",
            "message": "Поле должно быть целым числом"
        },
        {
            "field": "description",
            "message": "Поле не может быть пустым"
        }
    ]
}
```

Если у одного поля несколько ошибок, то выглядеть это будет так:

```json
{
    "title": "Unprocessable entity",
    "message": "User input error",
    "errors": [
        {
            "field": "amount",
            "message": "Поле должно быть целым числом"
        },
        {
            "field": "amount",
            "message": "Сумма не должна быть меньше, чем 20 у.е."
        }
    ]
}
```

Можно указывать поля, которые находятся глубже, чем первый уровень:

```json
{
    "title": "Unprocessable entity",
    "message": "User input error",
    "errors": [
        {
            "field": "page.number",
            "message": "Поле должно быть целым числом"
        },
        {
            "field": "page.size",
            "message": "Поле должно быть целым числом"
        }
    ]
}
```
