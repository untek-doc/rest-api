URI
===

## Соглашения о наименовании URI

* URI является существительным, глаголом является HTTP-method (`GET`, `PSOT`, `PUT`, `DELETE`)
* URI называем аналогично имени сущности, с которой работаем
* Названия всегда давайте в **единственном числе**.
* Названия всегда пишите **строчными буквами**.
* Названия ссылок делайте как можно **проще**.
* **Используйте** в именах только буквы, цифры и тире.
* **Используйте** kebab-case стиль именования.
* **Убедитесь** в том, что имя уникально.
* в случае **совпадений** URI, составляем их так:
  * предметная область + тире + сущность
  * сущность + тире + вложенная сущность
* **Начинайте** имена с буквы и **не заканчивайте** их символом тире.
* **Избегайте** сокращений. Если их всё же нужно использовать, убедитесь в том, что они общепонятны.
* **Избегайте** нескольких подряд идущих символов тире.
* **Избегайте** глаголов в URI.

## Примеры

Разберем пример именования URI ресурса.
Пусть ресурсом будут статьи новостей.

Ссылки будут такие:

* `article` - статьи
* `comment` - комментарии к статьям

Если ресурс комментариев уже существует, то его следует именовать как `article-comment`.

Представим, что у нас есть еще фотографии и комментарии к ним.

Тогда ссылки будут такими:

* article
* article-comment
* photo
* photo-comment

Можно так же, делать глубину в некоторых случаях.
Например, восстановление пароля:

* `restore-password/request-activation-code`
* `restore-password/set-password`
* `restore-password/verify-activation-code`

Здесь немного ломается соглашение об использовании глаголов в ссылках, т.к. сделать шаги восстановления пароля без использования глаголов не представляется возможным.

> Note: Используйте глубину только там, где это действительно необходимо. Не стоит злоупотреблять уровнем глубины.