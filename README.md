# Домашнее задание к занятию «Ansible.Часть 2» -Твердяков Михаил

### Задание 1

**Выполните действия, приложите файлы с плейбуками и вывод выполнения.**

Напишите три плейбука. При написании рекомендуем использовать текстовый редактор с подсветкой синтаксиса YAML.

Плейбуки должны: 

1. Скачать какой-либо архив, создать папку для распаковки и распаковать скаченный архив. Например, можете использовать [официальный сайт](https://kafka.apache.org/downloads) и зеркало Apache Kafka. При этом можно скачать как исходный код, так и бинарные файлы, запакованные в архив — в нашем задании не принципиально.

[Playbook-7-2-1.1.yml](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/Playbooks-7-02/playbook-7-2-1.1.yml)
-
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%201-1.1.png)
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%201-1.2.png)
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%201-1.3.png)
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%201-1.4.png)

2. Установить пакет tuned из стандартного репозитория вашей ОС. Запустить его, как демон — конфигурационный файл systemd появится автоматически при установке. Добавить tuned в автозагрузку.

[Playbook-7-2-1.2.yml](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/Playbooks-7-02/playbook-7-2-1.2.yml)
-
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%201-2.1.png)
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%201-2.2.png)
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%201-2.3.png)
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%201-2.4.png)

3. Изменить приветствие системы (motd) при входе на любое другое. Пожалуйста, в этом задании используйте переменную для задания приветствия. Переменную можно задавать любым удобным способом.

[Playbook-7-2-1.3.yml](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/Playbooks-7-02/playbook-7-2-1.3.yml)
-
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%201-3.1.png)
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%201-3.2.png)
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%201-3.3.png)
---

### Задание 2

**Выполните действия, приложите файлы с модифицированным плейбуком и вывод выполнения.** 

Модифицируйте плейбук из пункта 3, задания 1. В качестве приветствия он должен установить IP-адрес и hostname управляемого хоста, пожелание хорошего дня системному администратору. 

[Playbook-7-2-2.yml](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/Playbooks-7-02/playbook-7-2-2.yml)
-
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%202-1.png)
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%202-2.png)
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%202-3.png)
---

### Задание 3

**Выполните действия, приложите архив с ролью и вывод выполнения.**

Ознакомьтесь со статьёй [«Ansible - это вам не bash»](https://habr.com/ru/post/494738/), сделайте соответствующие выводы и не используйте модули **shell** или **command** при выполнении задания.

Создайте плейбук, который будет включать в себя одну, созданную вами роль. Роль должна:

1. Установить веб-сервер Apache на управляемые хосты.
2. Сконфигурировать файл index.html c выводом характеристик каждого компьютера как веб-страницу по умолчанию для Apache. Необходимо включить CPU, RAM, величину первого HDD, IP-адрес. Используйте [Ansible facts](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_vars_facts.html) и [jinja2-template](https://linuxways.net/centos/how-to-use-the-jinja2-template-in-ansible/)
3. Открыть порт 80, если необходимо, запустить сервер и добавить его в автозагрузку.
4. Сделать проверку доступности веб-сайта (ответ 200, модуль uri).

В качестве решения:
- предоставьте плейбук, использующий роль;
- разместите архив созданной роли у себя на Google диске и приложите ссылку на роль в своём решении;
- предоставьте скриншоты выполнения плейбука;
- предоставьте скриншот браузера, отображающего сконфигурированный index.html в качестве сайта.

[Playbook-7-2-3.yml](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/Playbooks-7-02/playbook-7-2-3.yml)
-
[roles-7-2-3](https://drive.google.com/drive/folders/1iJQN9qb9GGjsT90eLSYO9eLlgFUHaPSS?usp=sharing)
-
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%203-1.png)
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%203-2.png)
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%203-3.png)
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%203-4.png)
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%203-5.png)
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%203-6.png)
![png](https://github.com/tverdyakov/7-02-Ansible-part-2/blob/main/screenshots/Задание%203-7.png)
---
