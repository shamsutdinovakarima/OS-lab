# Лабораторная работа №4

## Задание
Были даны 3 сервера rrobin, web1, web2,на которые установила nginx.На серверах web1, web2 Nginx должен работать по порту 8080 и отдавать кастомную страницу, зайдя на которую можно понять на каком сервере вы находитесь.На сервере rrobin Nginx должен обеспечить балансировку нагрузки серверов web1 и web2 в режиме round-robin. Вес каждого сервера одинаковый.


## Необходимые команды 
***Команда для поднятия виртуальных машин***

---
>vagrant up
---


***Команда для запуска playbook***

---
>ansible-playbook nginx.yml
---


## Кастомные страницы 

Кастомная страница web1

<a href="https://ibb.co/JBWbDbt"><img src="https://i.ibb.co/vwCr0rq/1-web.jpg" alt="1-web" border="0"></a>

Кастомная страница web2

<a href="https://ibb.co/p0hL9PJ"><img src="https://i.ibb.co/X2YCv4S/2-web.png" alt="2-web" border="0"></a>

192.168.11.113

<a href="https://ibb.co/Sxjg6Vq"><img src="https://i.ibb.co/4fqLF4B/2022-04-05-13-03-42.png" alt="2022-04-05-13-03-42" border="0"></a>
