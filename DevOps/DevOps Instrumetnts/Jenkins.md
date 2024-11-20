Курс по Jenkins - https://www.youtube.com/watch?v=cyb10iplv7U&list=PLg5SS_4L6LYvQbMrSuOjTL1HOiDhUE_5a

Jenkins book - ![[1727244862668.pdf]]


## CI/CD

==CI== - Continuous Integration
- Это DevOps модель, в которой разроботчики делают Commit кода в Repository и автоматически запускаются Build или Компиляция этого кода, после этого запускаются автоматические тесты кода: Unit Test, Integration Test, Functionally Test.
==CD== - Continuous Delivery and Deployment
- Это DevOps модель, в которой разроботчики делают Commit кода в Repository и автоматически запускаются Build или Компиляция этого кода, после этого запускаются автоматические тесты кода и готовый Artifact ( скомпелированный код ) делает Deploy в Staging, Production.
![[Screenshot 2024-08-08 090213.png]]

А теперь раскроем все структуру:
==1. CI==
- **Частое коммитирование:** Разработчики часто интегрируют свои изменения в общий репозиторий, что позволяет быстро выявлять и исправлять ошибки.
- **Автоматическое тестирование:** При каждом коммите или пуше изменений запускаются автоматические тесты, чтобы проверить корректность кода и его совместимость с остальной системой.
- **Автоматическая сборка:** Создание новых билдов автоматически после успешного прохождения тестов.
==2. CD==
- **Автоматическое развертывание:** Код автоматически разворачивается на подготовительную среду после прохождения всех тестов.
- **Человеческий контроль:** Финальное развертывание в продуктивную среду выполняется вручную, что позволяет проводить дополнительные проверки и тестирования.


## Альтернативы Jenkins 
- Circleci
- Bamboo
- TeamCity
- Codeship
- CI/CD Git
![[Screenshot 2024-08-08 090458.png]]

## Поднимаем Jenkins
Сам Jenkins я поднял на контейнере, вот сама команда:
```javascript
docker run jenkins/jenkins:lts-alpine
```

Если не откроется его web интерфенйс то нужно сделать проброс портов, и вот как это сделать:
```javascript
docker run -p 8080:8080 jenkins/jenkins:lts-alpine
```
Так же не забываем про открытие портов и firewall.
Сама команда у нас есть на Zabbix 

После всех работ мы если выйдем то настройки не сохронятся, для этого мы вот что сделаем:
```javascript
mkdir -p /home/user/jenkins
sudo chown -R 1000:1000 /home/user/jenkins 
sudo chmod -R 775 /home/user/jenkins
docker run -p 8080:8080 -v /home/user/jenkins:/var/jenkins_home --user 1000:1000 jenkins/jenkins:lts-alpine
```
Это пример, для нашего примера мы должны поменять дирикторию которая у нас используется 

## Администрирование Jenkins

- Обзор UI
- Основные настройки Jenkins 
- Обновление Jenkins 
- Возврат на предыдущую версию Jenkins
- Создание пользователей

## Команды для обновления Jenkins

Для начала мы копируем нашу ссылку на которой новый Jenkins. Далее просто захом в диррикторию /usr/share/jenkins/
И тут мы меняем файл jenkins.war на новый файл 

## Управление Plugins

- Установка Plugins
- Установка Plugins любой предыдущей версии
- Обновление Plugins
- Удаление Plugins 

## Простейшие Jobs

- Создание простейших Jenkins Jobs
- Директории Jobs и Build на Jenkins Server
- АвтоУдаление Buiдd-ов
- Простейший пример доставки Artifact на удаленный сервер

Простейшие Deployment Jobs:
![[Screenshot 2024-08-14 091646.png]]

## Добавление Slave / Nodes

- Снизить нагрузку с Jenkins Master 
- Больше одновременных Build'ов 
- Build разных Платформ на разных серверах 
Node1 для .NET
Node2 JAVA
Node3 Ansible
Node4 Chef
- Windows или Linux
![[Screenshot 2024-08-19 145245.png]]
