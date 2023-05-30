Домашнее задание к занятию «Очереди RabbitMQ»   SKOPKIN ILYA


Задание 1. Установка RabbitMQ
Используя Vagrant или VirtualBox, создайте виртуальную машину и установите RabbitMQ. Добавьте management plug-in и зайдите в веб-интерфейс.

Итогом выполнения домашнего задания будет приложенный скриншот веб-интерфейса RabbitMQ.

![alt text](https://github.com/matiz86/git_hw-11-4/blob/main/Screenshot_1.jpg)

Задание 2. Отправка и получение сообщений
Используя приложенные скрипты, проведите тестовую отправку и получение сообщения. Для отправки сообщений необходимо запустить скрипт producer.py.

Для работы скриптов вам необходимо установить Python версии 3 и библиотеку Pika. Также в скриптах нужно указать IP-адрес машины, на которой запущен RabbitMQ, заменив localhost на нужный IP.

$ pip install pika
Зайдите в веб-интерфейс, найдите очередь под названием hello и сделайте скриншот. После чего запустите второй скрипт consumer.py и сделайте скриншот результата выполнения скрипта

В качестве решения домашнего задания приложите оба скриншота, сделанных на этапе выполнения.

![alt text](https://github.com/matiz86/git_hw-11-4/blob/main/Screenshot_2.jpg)

![alt text](https://github.com/matiz86/git_hw-11-4/blob/main/Screenshot_3.jpg)

Задание 3. Подготовка HA кластера
Используя Vagrant или VirtualBox, создайте вторую виртуальную машину и установите RabbitMQ. Добавьте в файл hosts название и IP-адрес каждой машины, чтобы машины могли видеть друг друга по имени.

Пример содержимого hosts файла:

$ cat /etc/hosts
192.168.0.10 rmq01
192.168.0.11 rmq02
После этого ваши машины могут пинговаться по имени.

Затем объедините две машины в кластер и создайте политику ha-all на все очереди.

В качестве решения домашнего задания приложите скриншоты из веб-интерфейса с информацией о доступных нодах в кластере и включённой политикой.

![alt text](https://github.com/matiz86/git_hw-11-4/blob/main/Screenshot_6.jpg)


![alt text](https://github.com/matiz86/git_hw-11-4/blob/main/Screenshot_9.jpg)


Также приложите вывод команды с двух нод: 

![alt text](https://github.com/matiz86/git_hw-11-4/blob/main/Screenshot_4.jpg)

![alt text](https://github.com/matiz86/git_hw-11-4/blob/main/Screenshot_5.jpg)

![alt text](https://github.com/matiz86/git_hw-11-4/blob/main/Screenshot_7.jpg)

![alt text](https://github.com/matiz86/git_hw-11-4/blob/main/Screenshot_8.jpg)
