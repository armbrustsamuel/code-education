# Desafios

## Desafio 2

https://hub.docker.com/r/armbrustsamuel/codeeducation

## Excellent reference
https://blog.filippo.io/shrink-your-go-binaries-with-this-one-weird-trick/

## Commands

```
# docker build -t armbrustsamuel/laravel .

# docker run -d --name laravel -v $(pwd):/var/www -p 8000:8000 armbrustsamuel/laravel

# docker ps

# browser: http://localhost:8000/

#  instalar BASH
#  docker exec -it laravel apk add bash

#  acessar o container
#  docker exec -it laravel bash

# php artisan serve -> habilitar a porta

# deletar todos os containers
# docker rm $(docker ps -aq) -f 

# php artisan serve --host=0.0.0.0

# migration
# php artisan migrate
```

## importante
https://github.com/jwilder/dockerize

## importante para liberar acesso ao arquivo
```
chmod +x ./.docker/entrypoint.sh
```


## optimized
```
docker build -t armbrustsamuel/laravel-optimized -f Dockerfile.prod .
docker run --name laravel -d armbrustsamuel/laravel-optimized 

docker exec -it laravel bash -> não pode deixar pois não tem BASH em prod

entao

docker exec -it laravel apk add bash
```
