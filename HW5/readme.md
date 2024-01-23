# Docker Compose & Docker Swarm 
## Домашней задачи 5
Задание 1:
1) создать сервис, состоящий из 2 различных контейнеров: 1 - веб, 2 - БД
2) далее необходимо создать 3 сервиса в каждом окружении (dev, prod, lab)
3) по итогу на каждой ноде должно быть по 2 работающих контейнера
4) выводы зафиксировать

Установил связи между сервера и клиент при Swarm.
![1](/image/1.1.png "1")

Создал два Dockerfile для веб-контейнера и БД-контейнера.
![2](/image/1.2.png "2")

Создал файл docker-compose.yaml, в котором описвыаеются сервисы для двух контейнеров и сами окружения dev, prod, lab.
В docker-compose.yaml нужно прописать 3 сервиса: web-dev, db-dev, web-prod, db-prod, web-lab, db-lab.
![3](/image/1.3.png "3")

Создал файл dev.html, prod.html, lab.html , в которых описываеются название по каждому файлу.
![4](/image/1.4.png "4")

Запускаем Docker Compose командой docker-compose up -d для создания и запуска контейнеров.
![5](/image/1.5.png "5")

Проверяем, что на каждой ноде есть по 2 работающих контейнера. Для этого используем команду docker ps.
![6](/image/1.6.png "6")

Вышел из docker-compose.Создал файл docker-compose.yaml для SWARM, в котором описвыаеются сервисы для двух контейнеров и сами окружения dev, prod, lab.
В docker-compose-service.yaml нужно прописать 3 сервиса: web-dev, db-dev, web-prod, db-prod, web-lab, db-lab.
![7](/image/1.7.png "7")

Создал сервисе при stack командой docker stack deploy --c docker-compose-service.yaml default
![8](/image/1.8.png "8")

Проверяем, что на каждой ноде есть по 2 работающих контейнера. Для этого используем команду docker ps.
![9](/image/1.9.png "9")
![10](/image/2.0.png "10")
![11](/image/2.1.png "11")
![12](/image/2.2.png "12")
![13](/image/2.3.png "13")
![14](/image/2.4.png "14")