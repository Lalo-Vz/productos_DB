# productos_BD

Base de datos PostgreSQL para la administración de productos. Este proyecto levanta un contenedor de PostgreSQL usando Docker Compose.

## Requisitos

- Docker
- Docker Compose

## Configuración

Crea un archivo `.env` y ajusta los valores según necesites:

```
POSTGRES_PASSWORD=root
POSTGRES_USER=root
POSTGRES_DB=administrador_productos
PORT=5432:5432
```

## Poner en marcha

Levantar el contenedor de la base de datos:

```bash
docker compose up -d
```

Ver los contenedores activos:

```bash
docker compose ps
```

## Detener

```bash
docker compose down
```

> Nota: `docker compose down` no borra los datos. Para eliminar también el volumen (y los datos), usa:
> `docker compose down -v`

## Conectar a la base de datos

Desde tu equipo, la base de datos está disponible en `localhost:5432` con el usuario y contraseña definidos en `.env`.

Conectarse por línea de comandos (PostgreSQL client):

```bash
psql -h localhost -p 5432 -U root -d administrador_productos
```