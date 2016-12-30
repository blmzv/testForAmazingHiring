# Тестовое задание в AmazingHiring

## Задача
Написать приложение для работы с вакансиями, используя Реакт+Редакс и любую библиотеку для роутинга.
В приложении две страницы:
 * список вакансий;
 * описание вакансии.

### Список вакансий
Открывается по пути `/vacancies/`. Роутер должен перенаправлять на эту страницу, когда открываешь корень сайта.

Здесь выводятся все вакансии. Над списком вакансий фильтр по рекрутерам, на которых назначены вакансии. Пользователю показываются только имена рекрутеров, без идентификаторов. Если выбрать фильтр, то на странице останутся только назначенные на рекрутера вакансии, и это состояние сохранится в урл страницы ГЕТ-параметром, например, `/vacancies/?assignee=5`.

Одна вакансия может быть назначена на нескольких исполнителей. У каждого рекрутера может быть больше одной вакансии.

На этой странице находится кнопка _**Добавить вакансию**_. По нажатию на кнопку открывается страница создания вакансии.

### Вакансия
Открывается по `/vacancies/<vacandy_id>/`.

Это страница создания/просмотра/редактирования вакансии. Если открыть страницу по адресу `/vacancies/create/`, то это создание вакансии. Если айди вакансии есть — `/vacancies/3/`, —  то это просмотр. По пути `/vacancies/3/edit/` — редактирование.

У вакансии три поля:
 * название;
 * ответственный;
 * описание.

#### Название
Простое текстовое поле.

#### Ответственный
Выпадающий список имён рекрутеров. По умолчанию, пусто.

Если в режим создания в параметрах страницы передать идентификатор пользователя, например, `/vacancies/create/?assignee=2`, то должно подставиться имя пользователя с этим идентификатором.

#### Описание
Большое текстовое поле (textarea).
