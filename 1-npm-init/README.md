[[_TOC_]]

# NPM init

## Instalción de NPM en WSL

Revisamos la versión de npm

- `npm --version`

Instalamos la ultima versión de npm

- `sudo npm install -g npm@latest`

Comprobamos la nueva versión

- `npm --version`

limpiamos la caché

- `sudo npm cache clean -f`

Actualizamos Node

- `sudo npm install -g n`
- `sudo n stable`

## Instalación de Dependencias

Dependencias

- `npm install name`

Dependencia que solo va a ser utilizada en el entorno de desarollo

- `npm install name --save-dev`

Dependencia para ser llevada a produccion.

- `npm install name --save`

Paquetes Globales

- `npm install -g name`

Ver lista de los paquetes

- `npm list`

Ver lista de paquetes globales

- `npm list -g`

## Instalación de dependencias de versiones específicas

1. Instalar una dependencia opcional

	- `npm install package-name -o`

2. Se pueden generar conflictos cuando se tienen paquetes que usan la misma dependencia pero en versiones diferentes. Para evitar esto se puede simular una instalación con

	- `npm install package-name —dry-run`
Con esto se simula la instalación pero sin agregar ningún paquete, si no hay ningún conflicto se procede a instalar de la manera convencional.

3. Instalar la versión especifica de un paquete.

	- `npm install package-name@version`
Si luego se quiere instalar la versión más reciente se usa

	- `npm install package-name@latest`

4. Instala las dependencias que estén dentro de un package.json.

	- `npm install`

## Comandos en NPM (Scripts)

En el archivo `package.json` encontraremos un apartado de `scripts`

    "scripts": {
        "start": "node src/index.js",
        "node": "node src/index.js && node src/index.js"
      },

Podemos añadir n cantidad scripts segun necesitemos. Podemos unir
comandos con una misma palabra calve con el operador `&&`.

> Si el primero no se ejecuta el segundo tampoco lo hara.
