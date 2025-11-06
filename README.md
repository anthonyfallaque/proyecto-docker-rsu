# Sistema RSU 2025 - Dockerizado

## Instrucciones de Despliegue

### Requisitos

- Docker Desktop instalado

### Pasos

1. Clonar este repositorio:

```bash
   git clone https://github.com/tuusuario/proyecto-docker.git
   cd proyecto-docker
```

2. Levantar los contenedores:

```bash
   docker-compose up -d
```

3. Configurar la aplicación (primera vez):

```bash
   docker exec -it laravel-app bash
   cp .env.docker .env
   php artisan key:generate
   php artisan migrate:fresh --seed
   exit
```

4. Acceder a la aplicación:

```
   http://localhost:8080
```

## Detener los contenedores

```bash
docker-compose down
```
