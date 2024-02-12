# INTRODUCCION AL BACKEND 🗒

Creación de un servidor usando NODEJS y Express.

## Tabla de contenidos

- [Introducción](#introducción)
- [Descripción general de Node.js y Express](#descripción-general-de-nodejs-y-express)
- [Configuración del entorno de desarrollo](#configuración-del-entorno-de-desarrollo)
- [Manejo de rutas y vistas en Express](#manejo-de-rutas-y-vistas-en-express)
- [Conexión a la base de datos MySQL con Node.js](#conexión-a-la-base-de-datos-mysql-con-nodejs)
- [Creación de un formulario HTML para ingreso de datos](#creación-de-un-formulario-html-para-ingreso-de-datos)
- [Consulta y visualización de datos desde la base de datos](#consulta-y-visualización-de-datos-desde-la-base-de-datos)
- [Actualización y eliminación de datos en la base de datos](#actualización-y-eliminación-de-datos-en-la-base-de-datos)
- [Consumo de APIs](#consumo-de-apis)
- [Manejo de errores y mensajes flash en Express](#manejo-de-errores-y-mensajes-flash-en-express)
- [Optimización del código y buenas prácticas](#optimización-del-código-y-buenas-prácticas)
- [Despliegue de la aplicación en un servidor](#despliegue-de-la-aplicación-en-un-servidor)

## Introducción

Explicacion de los fundamentos de Node.js y Express, así como en la configuración inicial de nuestro entorno de desarrollo.

## Tech Stack  

**Client:** Javascript, EJS, Boostrap

**Server:** Node, Express

## Descripción general de Node.js y Express

¿Qué es NodeJs?

Node.js es un entorno de ejecución de JavaScript en el lado del servidor. A diferencia del entorno de ejecución del navegador, Node.js nos permite ejecutar código JavaScript en el servidor, lo que lo convierte en una herramienta poderosa para construir aplicaciones backend eficientes.

¿Qué es Express?

Express es un framework web minimalista para Node.js. Simplifica la creación de aplicaciones web y proporciona herramientas esenciales para el desarrollo del lado del servidor, como manejo de rutas, middleware, y otras utilidades.

## Configuración del entorno de desarrollo

- Verificación de la instalación de NodeJs y Npm en nuestro dispositivo.

```bash
node -v  # Verificar la instalación de Node.js
npm -v   # Verificar la instalación de NPM
```

## Inicialización de nuestro proyecto

- Comandos usados

```bash
npm init -y  # Creación del package.json
npm install express # Instalación del Framework Express
npm install -g nodemon # Instalación global de Nodemon (opcional)
npm install nodemon --save # Instalación local de Nodemon como dependencia
```

- Estructura de Carpetas y Archivos

Organizaremos nuestro proyecto creando carpetas para manejar diferentes aspectos de la aplicación, como rutas, vistas y archivos estáticos.

```cmd
/src
     /routes
     /views
     /public
```

## Creación de un Servidor Express Básico

Implementaremos un servidor Express básico para asegurarnos de que nuestra configuración inicial funcione correctamente.

```js
const express = require('express');
const app = express();
const port = 3000;

app.get('/', (req, res) => {
  res.send('¡Hola, mundo!');
});

app.listen(port, () => {
  console.log(`Servidor escuchando en http://localhost:${port}`);
});

```
