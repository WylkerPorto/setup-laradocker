# Setup Docker Para Projetos Laravel (9.19)

### Passo a passo
Clone Repositório
```
git clone https://github.com/WylkerPorto/setup-laradocker.git
```

Crie o Arquivo .env
```
cp .env.example .env
```


Atualize as variáveis de ambiente do arquivo .env
```
APP_NAME=setup
APP_URL=http://localhost

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=db_name
DB_USERNAME=usuario
DB_PASSWORD=senha

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
```


Suba os containers do projeto
```
docker-compose up -d
```


Acessar o container
```
docker-compose exec app bash
```


Instalar as dependências do projeto
```
composer install
```


Gerar a key do projeto Laravel
```
php artisan key:generate
```


Acessar o projeto
[http://localhost](http://localhost)
