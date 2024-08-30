1) Запустить с помощью docker compose mongodb и mongo-express (https://hub.docker.com/_/mongo-express)
- mongo - нереляционная БД
- mongo-express - админка к ней
2) Запустить с помощью docker compose gitea (https://hub.docker.com/r/gitea/gitea) и postgres
- gitea - аналог gitlab. Потребуются переменные
```
DB_TYPE=postgres
DB_HOST=db:5432
DB_NAME=gitea
DB_USER=gitea
DB_PASSWD=gitea
``` 
3) Запустить с помощью docker compose portainer (https://hub.docker.com/r/portainer/portainer)
