1) Запустить с помощью docker compose приложение на go (https://github.com/AnastasiyaGapochkina01/apps/tree/main/nginx-golang):

код приложения лежит в папке backend; в папке proxy лежит конфиг nginx. Nginx используется как прокси, то есть перенаправляет запросы на контейнер с бэкендом. Нужно:
- написать Dockerfile для backend`a
- написать docker-compose.yml, который поднимет два контейнера: первый  - само приложение (backend), второй прокси
- для прокси: смонтировать файл proxy/nginx.conf в /etc/nginx/conf.d/default.conf и вывесить порт контейнера 80 на хостовый порт 8080

должно подняться 2 контейнера и по команде ```curl 127.0.0.1:8090``` должно отвечать приложение

2) Запустить с помощью docker compose nextloud:
потребуется два контейнера
- сам nextcloud (https://hub.docker.com/_/nextcloud)
- база данных postgres

по итогу на ip виртуалки дожно открываться что-то такое
![image](https://github.com/user-attachments/assets/51b50b45-cd85-47c7-a9cf-d212453f439a)

3) С помощью docker compose запустить приложение vuejs (https://github.com/AnastasiyaGapochkina01/apps/tree/main/vuejs)

как собрать
- сделать workdir
- скопировать файлы приложения
- выполнить команды
```
yarn global add @vue/cli
yarn install
```
- определить переменную HOST=0.0.0.0
- запускается командой ```yarn run serve```

по итогу на ip машины должно открываться
![image](https://github.com/user-attachments/assets/bee1b053-e8b0-489e-8659-7d5803de74ea)
