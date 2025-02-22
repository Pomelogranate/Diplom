# «Разработка мобильного приложения для управления бронированием рабочих мест в офисе с поддержкой удалённой работы»

## _**1. Определение плана действий, первичных требований по теме**_

### Описание

Полное наименование программной разработки: «Разработка мобильного приложения для управления бронированием рабочих мест в офисе с поддержкой удалённой работы».
<br>
Приложение служит для упрощения процесса поиска, бронирования и управления рабочими местами, а также для обеспечения удобства пользователей, работающих как в офисе, так и удаленно.
<br>

### Состав выполняемых функций:

1. Авторизация сотрудников
2. Хеширование паролей
3. Разграничение прав доступа
4. Добавление нового бронирования
5. Сохранение нового бронирования
6. Просмотр существующего бронирования
7. Отмена существующего бронирования
8. Изменение существующего бронирования
9. Просмотр рабочих мест в реальном времени с возможностью фильтрации по дате, времени и типу рабочего места
10. Отправка push-уведомлений о приближающихся бронированиях
11. Редактирование настроек уведомлений. 
<br>

## _**2. Создание схемы базы данных**_

<br> 

 ![SchemaBD](https://github.com/Pomelogranate/Diplom/blob/main/Images2/Рисунок1.png)
 
<br>

1.	Роль – в данной таблице хранится информация о уровне доступа к данным и функциям приложения.
1.1.	ID Роли – код роли
1.2.	Роль – название роли

2.	Должности – в данной таблице хранится информация о должностях работников.
2.1.	ID должности – код должности
2.2.	Должность – наименование должности
2.3.	Роль - уровень доступа

3.	Пользователи – в данной таблице хранится информация о пользователях приложения – работниках.
3.1.	ID пользователя – код пользователя
3.2.	Имя
3.3.	Фамилия
3.4.	Отчество
3.5.	Логин
3.6.	Пароль
3.7.	Дата регистрации
3.8.	Номер телефона
3.9.	Должностьм

4.	Отделы – в данной таблице храница информация о офисах компании, их адресах
4.1.	ID отдела – код отдела
4.2.	Название – название отдела
4.3.	Адрес – адрес отдела

5.	Места – в данной таблице хранится информация о местах  на рабочем месте.
5.1.	ID места – код места
5.2.	Отдел – отдел, где находится место
5.3.	Тип места – тип рабочего места
6.	Типы мест – в данной таблице хранится информация о типах рабочих мест, например место с компьютером, зал совещаний и т.д.
6.1.	ID типа места – код типа места
6.2.	Тип – тип места

7.	Резервации - в данной таблице хранится информация о бронированиях рабочих мест.
7.1.	ID резервации – код резервации
7.2.	ID пользователя – кто из работников резервирует
7.3.	ID места – какое место резервируется
7.4.	Дата – день резервации
7.5.	Время начала – время начала резервации
7.6.	Время окончания – время окончания резервации

8.	Комментарии - в данной таблице хранится информация о комментариях к бронированию.
8.1.	ID комментария – код комментария
8.2.	ID резервации – код резервации, к которой пишется комментарий
8.3.	Комментарий – сам комментарий, текст
8.4.	Тип комментария 
8.5.	Дата и время комментария – когда комментарий был оставлен

9.	Типы комментариев - в данной таблице хранится информация о типах комментариев, например сообщения о неполадках оборудования, нарушениях сотрудника или простой комментарий.
9.1.	ID типа комментария – код типа комментария
9.2.	Тип комментария – название типа комментария
