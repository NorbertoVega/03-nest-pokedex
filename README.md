<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

# Ejecutar en desarrollo

1. Clonar el repositorio

2. Ejecutar:
```
npm install
```

3. Tener Nest CLI instalado
```
npm install -g @nestjs/cli
```

4. Levantar la base de datos
```
docker-compose up -d
```

5. Clonar el archivo ```.env.template``` y renombrar la copia a ```.env```

6. Llenar las variables de entorno en el ```.env```

7. Ejecutar la aplicación en dev: 
```
npm run start:dev
```

8. Reconstruir la base de datos con seed
```
http://localhost:3000/api/v2/seed
```

## Production build
1. Crear el archivo ```.env.prod```
2. Llenar las variables de entorno para producción
3. Crear la nueva imágen
```
docker-compose -f docker-compose.prod.yaml --env-file .env.prod up --build
```

## Stack usado

* MongoDB
* Nest