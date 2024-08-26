1) Запустить контейнер nginx:
- создать и прокинуть внутрь контейнера папку app (монтировать в /usr/share/nginx/html)
- в папке app создать файл index.html с таким содержимым
```
<Html>    
<Head>  
<title>  
Example of make a text B,I,U  
</title>  
</Head>  
<Body>   
<b> [This text is Bold......] </b>  
<I> [This text is Italic......] </I>  
<U> [This text is Underline......] </U>   
</Body>  
</Html> 
```
- вывесить порт 80 из контейнера на порт хоста 8090 
- при выполнении curl на ip:port должна отдаваться страница из п2
2) Запустить контейнер с mongodb:
- задать переменную ME_CONFIG_MONGODB_ADMINUSERNAME со значением admin
- задать переменную ME_CONFIG_MONGODB_ADMINPASSWORD со значением adminpassword
- создать директорию mongo_data и смонитировать ее внутрь контейнера в /data/db
- вывесить дефолтный порт монги на хост
3) Запустить контейнер с postgres 9:
- задать переменную POSTGRES_PASSWORD со значением passwd
- создать директорию pg_data и прокинуть ее в контейнер по пути /var/lib/postgresql/data
4) Для всех контейнеров, запущенных в п1-3 выяснить с помощью [docker inspect](https://docs.docker.com/reference/cli/docker/inspect/):
- ip-адрес
- volumes
- image
