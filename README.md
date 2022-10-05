# CusoDeNPM-JS
Desarrollo del curso de gestión de paquetes y dependencias con JS

## React with npm(npx)

Primero tienes que tener instalado el paquete create-react-app

- `npm install -g create-react-app`

Ahora si podemos crear la preconfiguración de la app

- `npx create-react-app nameDir`

Una vez construido, podemos habilitar un entorno de desarrollo local con

- `npm start`

## Actualización de dependencias

Para este ejemplo vamos a clonar un proyecto del profesor Oscar Barajas
donde, tendremos que actualizar las dependencias, primero clonamos

- `git clone https://github.com/gndx/react-base.git`

Ahora instalmos las dependencias necesarias que aparecen en el `package.json`

- `npm install`

Verificamos que todas esten en orden con

- `npm list`
- `npm outdate`

Actualizamos react y react-dom a su ultima versión

`npm install react@latest`

Tener en cuenta que react-dom tiene que actualizarse a la
misma versión, en mi caso la 17.0.2

`npm install react-dom@latest`

## Seguridad y solución de problemas

Para ver cuales son las vulnerabilidades actuales podemos
correr el comando `npm install`, a pesar de que ya esten 
instaladas las dependencias, esto con el fin de ver las
vulnerabilidades.

Ahora podemos usar

- `npm audit`

Que nos va mostrar que esta pasando y la información necesaria
para saber como solucionar las vulnerabilidades.

Una muy buena forma de saber si es buena idea usar un paquete
es con el siguiente comando, que muestra las vulnerabilidades
y otra información para cada paquete que estemos usando.

- `npm audit --json`

## Eliminación de dependencias y Package lock

Esto es un proceso sencillo, para esto podemos usar el siguiente
comando:

- `npm uninstall namePackage`

Otra forma de hacerlo es ir dentro del `package.json` y
eleminar las dependencias que ya no necesitamos, eso si
hay que volver a instalar el proyecto, podemos hacerlo con:

- `rm -rf node_modules/`
- `npm install`

Tambien hay que tener en cuenta que tenemos a nuestra disposición
el script para la instalación, el cual podemos usar con

- `npm run build`

O añadiendole la flag `--dd`

Que activa el modo verbose que muestra una información
más robusta sobre lo que va a ejecutar el comando.

Otro comando muy utilizado es:

`npm ci`

Que nos muestra las dependencias que ya no tienen soporte, 
que estan depreciadas.

### Package lock

Es un documento como package.json pero que muestra la historia 
de todas las dependencias, y las dependencias de las dependencias.
