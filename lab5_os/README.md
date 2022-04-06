# Лабораторная работа №5

## Задание  
:ballot_box_with_check: 1. На серверах web1, web2 установить Nginx.

:ballot_box_with_check: 2. На серверах haproxy1, haproxy2 установить и настроить  отказоустойчивую связку HAProxy+Keepalived. Настроить VIP с помощью Keepalived в соответствии со схемой

:ballot_box_with_check: 3. На серверах web1, web2 Nginx должен работать по порту 8080 и отдавать кастомную страницу, зайдя на которую можно понять на каком сервере вы находитесь.

:ballot_box_with_check: 4. На серверах с HAProxy ПО должно обеспечить балансировку нагрузки серверов web1 и web2 в режиме round-robin. Сделать таймауты ожидания ответа web1 и web2 как можно меньше. Скажем, 1-2 секунды

:ballot_box_with_check: 5. Установка и настройка всего ПО должна быть обеспечена Ansible-сценарием.

:ballot_box_with_check: 6. Все файлы по этому заданию выложить в Github и написать ReadMe со скринами работоспособности и инструкцию по запуску вашего Ansible-сценария.


## Необходимые команды 
***Команда для поднятия виртуальных машин***  :computer:

---
>vagrant up

---


***Команда для запуска playbook*** :book:

---
>ansible-playbook nginx.yml
---

## Проверяем работу балансировки:

<a href="https://ibb.co/Sy5rbVr"><img src="https://i.ibb.co/QQpdLYd/photo-2022-04-06-21-55-07.jpg" alt="photo-2022-04-06-21-55-07" border="0"></a>

## Проверка отказоустойчивости:

***Сначала всё включено***

![68747470733a2f2f692e6962622e636f2f515170644c59642f70686f746f2d323032322d30342d30362d32312d35352d30372e6a7067](https://user-images.githubusercontent.com/89980487/162050969-9f89e2a2-b552-41ef-bbbd-cd12332b4e09.jpg)

<a href="https://ibb.co/hHs6M1k"><img src="https://i.ibb.co/82MCB4J/2022-04-06-14-12-17.png" alt="2022-04-06-14-12-17" border="0"></a>

***Отключим haproxy 1***

<a href="https://ibb.co/v3hBVZK"><img src="https://i.ibb.co/LxrPYn2/2.png" alt="2" border="0"></a>

 :tada: ***Страница продолжает работать***  :tada:

<a href="https://ibb.co/Sy5rbVr"><img src="https://i.ibb.co/QQpdLYd/photo-2022-04-06-21-55-07.jpg" alt="photo-2022-04-06-21-55-07" border="0"></a>

***Отключим haproxy 2***

<a href="https://ibb.co/TY0zTZ4"><img src="https://i.ibb.co/NtNw3X9/2022-04-06-14-17-00.png" alt="2022-04-06-14-17-00" border="0"></a>

 :tada: ***Страница продолжает работать*** :tada:

<a href="https://ibb.co/Sy5rbVr"><img src="https://i.ibb.co/QQpdLYd/photo-2022-04-06-21-55-07.jpg" alt="photo-2022-04-06-21-55-07" border="0"></a>




