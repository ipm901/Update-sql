

 
В качестве репрезентации опыта работы с SQL-запросами рассмотрим сайт Alikson.ru. В частности работа с профилем (добавление, удаление, обновление информации о пользователе)

Цель: продемонстрировать работу с INSERT, DELETE, UPDATE, SELECT

Пояснение: Все операции провожу над таблицей Profile, которая имеет следующие поля last_login, username, first_name, last_name, email, is_active, phone, date_of_birth.

Добавляю пользователя:
</span></span><pre><span class="pl-k">INSERT INTO</span> Profile (last_login, username, first_name, last_name, email, 
is_active, phone, date_of_birth)
<span class="pl-k">values</span> (<span class="pl-k">NULL</span>, <span class="pl-s"><span class="pl-pds">'</span>volfgun_666@gmail.com<span class="pl-pds">'</span></span>, <span class="pl-s"><span class="pl-pds">'</span>Семен<span class="pl-pds">'</span></span>, <span class="pl-s"><span class="pl-pds">'</span>Коржов<span class="pl-pds">'</span></span>, 
<span class="pl-s"><span class="pl-pds">'</span>volfgun_666@gmail.com<span class="pl-pds">'</span></span>, TRUE, <span class="pl-s"><span class="pl-pds">'</span>+7-906-563-45-91<span class="pl-pds">'</span></span>, <span class="pl-s"><span class="pl-pds">'</span>1966-10-27<span class="pl-pds">'</span></span>)</pre>

<p dir="auto"><em>Обнавляю информацию о пользователе:</em></p>



<pre>UPDATE Profile 
SET date_of_birth = '1999-09-26'
WHERE id = 10</pre>

<p dir="auto">Удаление несокльких пользователей:</em></p>

<pre>
  
 DELETE FROM Profile
WHERE ID > 5 AND ID < 8
</pre>

<p dir="auto">Вывод пользователей с почтовым ящиком @gmail.com:</em></p>
<pre>SELECT *
FROM Profile
WHERE email LIKE '%@gmail.com'</pre>

<span class="pl-k">INSERT INTO</span>
