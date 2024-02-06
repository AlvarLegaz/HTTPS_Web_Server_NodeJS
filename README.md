# HTTPS_Web_Server
HTTPS_Web_Server

Repositorio con información sobre una servidor web HTTPS con Node.js 

## Instalacion de la WEB con Node.JS y Express

**Pasos para instalar servidor**

Info extraida de https://www.jacobsoft.com.mx/es_mx/como-crear-un-servidor-https-con-node-js-y-express/

1. Ejecutar `npm init` para crear el fichero package.json.
1.1 indicar el entry point como index.js

2. Instalar express `npm install --save express`

3. Con esto ya podemos crear un servidor http, 
4. Vamos a instalar de una vez las demás dependencias: 
4.1 https para el manejo del servidor con SSL `npm install --save fs`
4.2 fs para acceso al sistema de archivos. `npm install --save https`

5. Con las dependencias creadas vamos a crear el primer servidor http.
5.1 Creamos el index.js

***Servidor HTTPS***

Necesitamos los archivos de los certificados ssl (crt y key).
podemos crear un certificado de pruebas autofirmado con OpenSSL para desarrollar nuestro servidor.
Luego probado reemplazamos los archivos crt y key por los que correspondan al servidor donde vamos a desplegar el proyecto.

He bajado openssl para windows y en su carpeta he ejecutado el comando
`C:\Program Files\OpenSSL-Win64\bin>openssl req -nodes -x509 -newkey rsa:4096 -keyout server.key -out server.crt -days 365`

Te hará una serie de preguntas y listo...

**Ejecutar el servidor**

1 Ejecutamos el servidor `node index.js`.
2 Accedemos al navegador y tecleamos `https://127.0.0.1` ojo hay que poner el https. 
