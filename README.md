<head>

</head>
 
<body>
 
В качестве репрезентации опыта работы с SQL-запросами рассмотрим сайт Alikson.ru. В частности работа с профилем (добавление, удаление, обновление информации о пользователе)

Цель: продемонстрировать работу с INSERT, DELETE, UPDATE, SELECT

Пояснение: Все операции провожу над таблицей Profile, которая имеет следующие поля last_login, username, first_name, last_name, email, is_active, phone, date_of_birth.

Добавляю пользователя:
<pre>INSERT INTO</span> Profile (last_login, username, first_name, last_name, email, 
is_active, phone, date_of_birth)
values( 'volfgun_666@gmail.com', 'Семен', 'Коржов' 
'</span>volfgun_666@gmail.com', TRUE, '+7-906-563-45-91'.'1966-10-27')</pre>

<p ><em>Обнавляю информацию о пользователе:</em></p>



<pre>
UPDATE Profile 
SET date_of_birth = '1999-09-26'
WHERE id = 10</pre>

<p>Удаление несокльких пользователей:</em></p>

<pre>
  
DELETE FROM Profile
WHERE ID > 5 AND ID < 8
</pre>

<p><em>Вывод пользователей с почтовым ящиком @gmail.com:</em></p>
<pre>SELECT *
FROM Profile
WHERE email LIKE '%@gmail.com'</pre>

