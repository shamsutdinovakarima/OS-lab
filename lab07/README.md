# Лабораторная работа №7

## Задание 
:ballot_box_with_check: 1. Настроила консул.

:ballot_box_with_check: 2. Проинициализировала  базу данных на выделенных дисках. 

:ballot_box_with_check: 3. На серверах pg1 и pg2 настроила оркестратор репликации Patroni (пакет в архиве).

:ballot_box_with_check: 4. С помощью утилиты vip-manager обеспечила настройку VIP адреса на мастер сервере. 

## Используемые команды 
***Команда для поднятия виртуальных машин***  :computer:

---
>vagrant up
---

***Команда для запуска playbook*** :book:
---
>ansible-playbook consul.play
---
***Остальные команды***
---
>ansible consul -m shell -a 'sudo systemctl restart consul'
---

---
>ansible-playbook playbook.yml
---

---
>зайти на pg1, pg2 под рутом

>patronictl -c /opt/app/patroni/etc/postgresql.yml list

>patronictl -c /opt/app/patroni/etc/postgresql.yml switchover
---
***Проверка оркестратора репликации Patroni на pg1***

<a href="https://ibb.co/9s6H8Fx"><img src="https://i.ibb.co/PwKGm72/2022-04-12-22-21-56.png" alt="2022-04-12-22-21-56" border="0"></a>

***Проверка оркестратора репликации Patroni на pg2***

<a href="https://ibb.co/sKcrwyc"><img src="https://i.ibb.co/tqn5s8n/2022-04-12-22-22-15.png" alt="2022-04-12-22-22-15" border="0"></a>
