HELLO WORLD DOCKER

Para bajar la imagen se ejecuta el siguiente comando:

    docker pull hello-world

Para correrlo se ejecuta:

    docker run hello-world


----------------------------------------------------------
Comandos Git

primero incializamos

    git init

Agregamos los archivos necesarios

    git add .

Hacemos commit de lo que incluye

    git commit -m "{MENSAJE}"

definimos la branch

    git branch -M master

agregamos el origen remoto

    git remote add origin {ENLACE AL REPO}

Hacemos push

    git push -u origin master

------------------------------------------
Para bajar la imagen de sql server ejecutamos el siguiente comando:

    docker pull mcr.microsoft.com/mssql/server:2019-latest

Para ejecutarlo cuidando parametros como
    persitencia
    conexion
Ejecutamos el siguiente comando

    docker run -e 'ACCEPT_EULA=Y' -e 'MSSQL_SA_PASSWORD=Password' -p 1433:1433 -v ${pwd}/data:/var/opt/mssql/data -v ${pwd}/log:/var/opt/mssql/log -v ${pwd}/secrets:/var/opt/mssql/secrets -d mcr.microsoft.com/mssql/server:2019-latest

-e son los parametros de configuracion

-p son los puertos a utilizar externo:internoImagen

-v define las rutas de memoria  local:rutaImagen para guardar datos de forma persistente

-d hace que no requiera el uso en primer plano de la terminal para funcionar y mandarlo a background.

