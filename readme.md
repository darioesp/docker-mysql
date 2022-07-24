# **MYSQL Docker**
Este es un contenedor base para correr mysql en tu local de manera sencilla.

Antes de nada deberos contar con docker instalado en nuestra maquina descargalo [aquí](https://www.docker.com/products/docker-desktop/).

## **Recomendaciones**
Se recomienda instalar posteriormente una aplicación para conectarte con mysql desde tu local, recomiendo alternativas como:

| App | Url |
|-|-|
| Workbench | [Descargar](https://dev.mysql.com/downloads/workbench/) |
| Sequel Pro |[Descargar](https://sequelpro.com/download#auto-start) |

## **Iniciemos**
Recuerda seguir estos pasos para que todo se levante de manera correcta:

```bash
# copiar el .env-example a .env
cp .env-example .env

# .env-example
APP_NAME=mysql
APP_PLATAFORM=linux/amd64 #remueve si no estas en linux o con chip m1
# host and port
DB_HOST=127.0.0.1
DB_PORT=33060
# base de datos
DB_MYSQL_ROOT_PASSWORD=Secret@1 # password de root
DB_USERNAME=usuario # usuario personalizado de la base de datos
DB_PASSWORD=Secret@1 # password de usuario
DB_DATABASE= # creara esta base de datos

```

Ahora desde la raíz de nuestro repo ejecuta este comando:

```zsh
docker-compose up -d
```
# **Amante de la terminal**
Te recomiendo instalarte [kool](https://kool.dev/docs/getting-started/installation), posterior a eso mírate 👀 el archivo kool.yml donde encontraras comandos cortos para realizar tareas simples de exportación, migración y creación de base de datos.

|Comando|Descripción|
|-|-|
|`kool run bash`| Conectarnos por bash al contenedor |
|`kool run mysql-create`| Crear db en el contenedor|
|`kool run mysql-imp`| Importar db en el contenedor|
|`kool run mysql-exp`| Exportar db en el contenedor|

Preparemos nuestra variables para los run:

```bash
# Para exportar sql scripts por terminal usando kool run [mysqlimp/mysqlexp]

# name db
db=fixu_soler
# db import
pathimp=/Users/juanito/path/db.sql
# db export
pathexp=/Users/juanito/path/db.sql
```

