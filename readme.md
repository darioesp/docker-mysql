# MYSQL Docker
Este es un contenedor base para correr mysql en tu local de manera sencilla.

Se recomienda instalar posteriormente una aplicación para conectarte con mysql desde tu local, recomiendo alternativas como:

| App | Url |
|-|-|
| Workbench | [Descargar](https://dev.mysql.com/downloads/workbench/) |
| Sequel Pro |[Descargar](https://sequelpro.com/download#auto-start) |

## Instalemos MYSQL
Antes de nada deberos contar con docker instalado en nuestra maquina descargar lo [aquí](https://www.docker.com/products/docker-desktop/).

Ahora desde el path raíz (.) de nuestro repo ejecutaremos este comando:

```zsh
docker-compose -up -d
```

A continuación te dejo la manera de levantar tu conexión con el contenedor, configurando el acceso con estas credenciales:

```text
HOST    : 127.0.0.1:33060
USER    : root
PASSWORD: Secret@1
```

Ahora si eres de los amantes de la terminal te recomiendo instalarte [kool](https://kool.dev/docs/getting-started/installation), posterior a eso mírate 👀 el archivo kool.yml donde encontraras comandos cortos para realizar tareas simples de exportación, migración y creación de base de datos.

Preparemos nuestra variables para los run:
```bash
# usa estas variable para exportar sql scripts por terminal usando kool run [mysqlimp/mysqlexp]
# name db
db=fixu_soler
# db import
pathimp=/Users/juanito/path/db.sql
# db export
pathexp=/Users/juanito/path/db.sql
```

|Comando|Descripción|
|-|-|
|bash| Conectarnos por bash al contenedor |
|mysqlCDB| Crear db en el contenedor|
|mysqlimp| Importar db en el contenedor|
|mysqlexp| Exportar db en el contenedor|
|setup| |
