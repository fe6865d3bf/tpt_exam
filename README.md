# EXAM

# 1.ansible -----
Установить с помощью ansible SonarQube -> https://www.howtoforge.com/tutorial/how-to-install-sonarqube-on-ubuntu-1604/
Модули `shell` `command` использовать нельзя

# 2.terraform -----
Ссылка на приложение - exam_python
Развернуть приложение в облаке используя Serverless (google/azure functions; aws lambda) 
Вам понадобиться Storage; Serverless; API
API должно быть сконфигурировано на GET
В отпут записать url, который сгенерирует terraform зайти по url, увидеть волшебную фразу

# 3.k8s -----
Настройка RBAC
Создать 2 Namespace в minikube
Создать 2 ServiceAccount и сгенерировать для них конфиги. Каждый аккаунт должен мочь обращаться только в ской NameSpace; в остальные нет

# 4.docker ---- 
Собрать и запустить Docker образ для приложения на java
использование multi-stage build является обязательным
Ссылка на приложение exam_java

# 5.code ----
Написать приложение на любом языке у которого будет возможность использования web-server (python(flask, django), php (laravel), ruby(ror) или другие), у которого будет пустая web страница. Создать route "/blacklist" при обращении на которую ваш IP будет вноситься в черный список и будет выдоваться HTTP ERROR 403 

ip можно записать в базу или массив (лучше в базу данных)

# 6.jenkins ----
Ссылка на приложение - https://github.com/gruntwork-io/sample-app-docker
Создать jenkins pipeline, который будет - брать код, устанавливать зависимости, запускать тесты, собирать docker образ, положить образ в приватный dockerhub, спулить образ, а запустить (docker run)

sh использовать только для зависимостей и тестов

# 7.ansible ---
Установить LAMP (Apache/Nginx MySQL/PostgreSQL PHP7.1) на LINUX и с помощью Ansible развернуть приложение exam_php

# 8.k8s -----
Развернуть приложение - https://github.com/kosmas58/pia-docker 

Там должно быть 2 пода, один из которых приложение, второй база данных. поды должны видеть друг друга kubernetes DNS

Параметры запуска можно посмотреть в docker-compose.yml (То есть все имена хостов вы должны указать правильно, по тому как работает kubernetes)

# 9.docker
Собрать 2 контейнера, один из который будет открывать GOOGLE_CHROME, а второй MOZILA FIREFOX. при запуске контейнера браузер должен открыться на вашей хост машине. Совет используйте Linux


# 10.helm -----
Приложение - exam_go
Собрать docker образ (Dockerfile присутствует). Отправить его в ваш приватный репозиторий на dockerhub и развернуть приложение в kubernetes с помощью helm

# 11.terraform ----
Создать 2 NoSQL базы данных (MongoDB, Neo4j, DynamoDB, CosmosDB) в любом облаке и связать их и настроить репликацию между ними и geo redundancy.

Внутри одной из них создать коллекцию и документ (через какое-то время это все должно появиться в во второй базе)

# 12.docker ----
Приложение exam_php
Собрать docker образ для приложения.

Вы должны поднять Nginx контейнер и в нем настроить php-cgi и запустить второй контейнер (они должны видеть друг друга). Открыть в браузере nginx и увидеть ваш сайт

# 13.ansible ----
Установить 2 postgresql базы данных и настроить между ними репликацию

https://www.howtoforge.com/tutorial/how-to-set-up-master-slave-replication-for-postgresql-96-on-ubuntu-1604/

# 14.k8s
Свалидировать Kubernetes кластер (1 master, 1 node)

# 15.terraform ---- 
Установить 2 машины в облаке и 1 реляционную базу данных. Создать базу данных в RDBMS
	С помощью Remote Exec на машинах установить на 1 Nginx/Apache на второй Python3.6 и pip3; С помощью pip поставить pandas и tensorflow (или как-то так)
	И открыть 80 порт для 1 машины на уровне облака (Network Security Group)

# 16. terraform + ansible ---	
Спровизионить виртуальную машину в облаке и установить на неe Redis https://redis.io/topics/quickstart и Set local redis instance to be slave of melee.island on port 6377 (ansible_doc). Все должно делаться одной коммандой - через Local-exec и terraform inventory (https://github.com/adammck/terraform-inventory)
Использовать методы shell и command нельзя

# 17. jenkins ----
Ссылка на приложение - exam_go
Положить содержимое в новый github repo
Сделай пайплай, который будет брать сурс код, билдить контейнер и класть образ в гитхаб с разными тегами образа. Тегирование должно быть не от балды, а соблюдать какую-то логику. Тегирование должно быть построено на основе git

# 18.helm -----
Нужно задеплоить магазин соков с помощью helm в куберенетес и задеплоить его еще раз с другим тегом (обновить) и после этоог откатиться на предыдущую. Так же не обоходимо настроить Ingress и привязать его к магаизну соков
Магазин соков https://hub.docker.com/r/bkimminich/juice-shop
