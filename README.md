<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

# Ejecutar en Desarrollo

1.- clonar el repositorio 2. Ejecutar

```
yarn install
```

3. Tener Nest CLI instalado

```
npm -i g @nestjs/cli
```

4. Levantar la base de datos

```
docker-compose up -d
```

5. Clonar el archivo **_.env.template_** y renombrarlo la copia a **_.env_**

6. Llenar las variables de entorno definidas en el `.env`

7. Ejecutar la aplicación en dev:

```
yarn start:dev
```

. Reconstruir la base de datos con el seed

```
http://localhost:3000/api/v2/seed
```

## Stack usado

- MongoDB
- NestJS
- Docker

# Production Build

1. Crear el archivo `.env.prod`
2. Llenar las variables de entorno definidas en el `.env.prod`
3. Crear la nueva imagen

```
docker-compose -f docker-compose.prod.yaml --env-file .env.prod up --build
```
