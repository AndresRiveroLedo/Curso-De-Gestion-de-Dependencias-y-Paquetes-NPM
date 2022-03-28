# 📒 v1 - Acerca de NPM, paquetes y módulos

## ¿Qué es NPM (node package manager) ? 

De sus siglas NPM (Node Package Manager) es un gestor de paquetes desarrollado en su totalidad bajo el lenguaje JavaScript por Isaac Schlueter, a través del cual podemos obtener cualquier librería con tan solo una sencilla línea de código, lo cual nos permitirá agregar dependencias de forma simple, distribuir paquetes y administrar eficazmente tanto los módulos como el proyecto a desarrollar en general.


Es un gestor de paquetes, el más popular que tiene JavaScript, donde encontrarás una gran cantidad de recursos para poder implementar en tus proyectos. También vas a poder crear tus propios paquetes y compartirlos con toda la comunidad.

Enlace oficial: https://www.npmjs.com/

## ¿Que diferencia hay entre NPM y YARN?

Ambos tienen el mismo propósito, manejar paquetes para aplicaciones Javascript. NPM es más grande, tiene más cantidad de dependencias. Pero Yarn tengo entendido que utiliza APIs de NPM para descargar dependencias de ahí.
Una ventaje que ofrece Yarn es la posibilidad de cachear las dependencias para descargarlas rápidamente y sin internet. Pero desde luego que es más utilizado NPM.

Yarn es un gestor de paquetes JavaScript construido por Facebook, Google, Exponent y Tilde. Como se puede leer en el anuncio oficial, su propósito es resolver algunos problemas que los equipos de estas empresas enfrentaron al usar NPM, como que la Instalación de paquetes no fue rápida o lo suficientemente consistente, o los problemas de seguridad surgidos a raíz de la manera en que NPM permite ejecutar paquetes de código en la instalación.

Sin embargo, esto no es un intento de sustituir por completo a NPM. Yarn es solamente un nuevo cliente CLI que obtiene módulos del registro de NPM. Nada va a cambiar sobre los propios registros; es decir, todavía serás capaz de invocar y publicar paquetes de forma normal.

## ¿Qué es Node.js?

Node.js es un entorno de tiempo de ejecución de JavaScript (de ahí su terminación en .js haciendo alusión al lenguaje JavaScript). Este entorno de tiempo de ejecución en tiempo real incluye todo lo que se necesita para ejecutar un programa escrito en JavaScript. También aporta muchos beneficios y soluciona muchísimos problemas, por lo que sería más que interesante realizar nuestro curso de Node.js para obtener las bases, conceptos y habilidades necesarias que nos motiven a profundizar en sus opciones e iniciar la programación. 

Node.js fue creado por los desarrolladores originales de JavaScript. Lo transformaron de algo que solo podía ejecutarse en el navegador en algo que se podría ejecutar en los ordenadores como si de aplicaciones independientes se tratara. Gracias a Node.js se puede ir un paso más allá en la programación con JavaScript no solo creando sitios web interactivos, sino teniendo la capacidad de hacer cosas que otros lenguajes de secuencia de comandos como Python pueden crear. 

Tanto JavaScript como Node.js se ejecutan en el motor de tiempo de ejecución JavaScript V8 (V8 es el nombre del motor de JavaScript que alimenta Google Chrome. Es lo que toma nuestro JavaScript y lo ejecuta mientras navega con Chrome). Este motor coge el código JavaScript y lo convierte en un código de máquina más rápido. El código de máquina es un código de nivel más bajo que la computadora puede ejecutar sin necesidad de interpretarlo primero, ignorando la compilación y por lo tanto aumentando su velocidad. 

## ¿Para qué sirve Node.js?

Node.js utiliza un modelo de entrada y salida sin bloqueo controlado por eventos que lo hace ligero y eficiente (con entrada nos referimos a solicitudes y con salida a respuestas). Puede referirse a cualquier operación, desde leer o escribir archivos de cualquier tipo hasta hacer una solicitud HTTP. 

La idea principal de Node.js es usar el modelo de entrada y salida sin bloqueo y controlado por eventos para seguir siendo liviano y eficiente frente a las aplicaciones en tiempo real de uso de datos que se ejecutan en los dispositivos. Es una plataforma que no dominará el mundo del desarrollo web pero si que satisface las necesidades de una gran mayoría de programadores. 

La finalidad de Node.js no tiene su objetivo en operaciones intensivas del procesador, de hecho, usarlo para programación de más peso eliminará casi todas sus ventajas. Donde Node.js realmente brilla es en la creación de aplicaciones de red rápidas, ya que es capaz de manejar una gran cantidad de conexiones simultáneas con un alto nivel de rendimiento, lo que equivale a una alta escalabilidad.

## Cómo funciona Node.js

El funcionamiento interno del entorno de ejecución para JavaScript, Node.js, es bastante interesante. En comparación con las técnicas tradicionales de servicio web donde cada conexión (que crea una solicitud) genera un nuevo subproceso, ocupando la RAM del sistema y regularmente maximizando la cantidad de RAM disponible, Node.js opera en un solo subproceso, utilizando el modelo entrada y entrada sin bloqueo de la salida, lo que le permite soportar decenas de miles de conexiones al mismo tiempo mantenidas en el bucle de eventos.

El nodo está completamente controlado por eventos. Resumiendo podemos decir que el servidor consta de un subproceso que procesa un evento tras otro. 

# 📒 v2 - Windows

## Comprobar version de Node y NPM

Una vez descargado y instalado nodejs, comprueba si se ha instalado correctamente ejecutando en una terminal (en Windows pulsa Control + R y escribe cmd ) el comando:

```
    node -v
```

Si la salida del comando es la versión de nodejs es que se ha instalado correctamente, comprueba también que tienes npm ejecutando:

```
    npm -v
``` 
### Cómo actualizar NPM

Si quieres actualizar NPM a la última versión simplemente tienes que lanzar este comando:

```
    npm install -g npm@latest
```

O si quieres actualizar NPM en MAC:

```
    sudo npm install -g npm
```
También puedes actualizar NPM usando tu gestor de paquetes de la distribución de Linux si lo has instalado así.

Si están trabajando en Windows es muy recomendable probar Cmder, un emulador de la consola de los sistemas *nix, con el que van a poder ejecutar más fácilmente los comandos que se vean a lo largo del curso 😉

Enlace oficial: https://nodejs.org/es/

## ¿Que significa la -g del comando?

Significa que se aplicará globalmente.

-g o --global para instalar dependencias globales
-S o --save para instalar dependencias globales
-D o --save-dev para instalar dependencias globales

## ¿Que relación tienen los archivos : package.json, package-lock.json y yarn.lock

Los archivos yarn.lock y package-lock.json son archivos que Yarn y NPM generan con toda la información de las dependencias de nuestro proyecto para que todo el equipo utilice las mismas versiones de las herramientas y no haya ningún problema en esa parte.

Por lo tanto, si nos encontramos con algún error es posible que podamos resolverlo pidiéndole a Yarn o NPM que vuelvan a instalar nuestras dependencias desde cero.

Package.json es donde vamos a definir la información y las dependencias del proyecto.

La diferencia entre package-lock y yarn.lock es que package-lock es utilizado por NPM, mientras que yarn-lock es por utilizado por Yarn.

Yarn es un instalador dependencias de JavaScript alternativo a NPM.

La clave es que se sugiere que un proyecto solo utilice ya sea NPM o Yarn, no ambos, ya que puede generar un conflicto por la manera en el que funciona cada uno al ser diferente.

## ¿Cómo desinstalo npm?

En el caso de windows lo que tienes que hacer simplemente desinstalar nodejs del panel de control, como cualquier aplicacion de windows.

En linux:
En esta guía te explican: https://docs.npmjs.com/misc/removing-npm.html. 😉

## ¿Cómo actualizo node y npm en wls?

De igual forma que si estuvieras en Linux nativo. Puedes usar NVM. O con el comando `npm install -g npm@latest`. O como prefieras.

# 📒 v3 - Mac

## En Mac

1. Debes de ir a nodejs.org.
2. Descargar la última versión de Node.

Para comprobar que está instalado:

1. Abre la terminal y escribe:

```
    npm -v 
```
Esto nos da la versión que tenemos.

Para instalar la última versión:

```
    sudo npm install npm@latest -g
```

## ¿Qué significa el comando sudo?

Es una utilidad de los sistemas operativos tipo Unix, como Linux, BSD, o Mac OS X, que permite a los usuarios ejecutar programas con los privilegios de seguridad de otro usuario (normalmente el usuario root) de manera segura, convirtiéndose así temporalmente en súper usuario.

Si un usuario normal desea ejecutar un comando de root (o de cualquier otro usuario), Sudo verifica en su lista de permisos y si está permitido la ejecución de ese comando para ese usuario, entonces Sudo se encarga de ejecutarlo.

## En linux:
1. Ultima versión LTS : `sudo apt-get install nodejs npm`
2. Instalar NVM: curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
    + `nvm ls-remote` para ver la lista de versiones que hay de node
    + Luego escogen la versión que deseen instalar
    + Example: para instalar Nodejs v9.3.0, ejecuta: -nvm install v9.3.0

## ¿Como puedo actualisar npm si lo tengo instalado con nvm?

NPM se actualiza cada vez que actualizas node a través de nvm, sin embargo puedes usar el comando nvm install-latest-npm para actualizar npm a la última versión soportado por la versión de node que usas. Si actualizas node puedes agregar el flag --lastest-npm para asegurarte de instalar la última versión de npm que soporta.

# 📒 v4 - Iniciar un proyecto

## iniciar un proyecto en NPM
+ Primero abrimos nuestra terminal y nos posicionamos donde guardamos nuestros archivos.
+ Podemos crear una carpeta para nuestro proyecto con el comando desde la consola:
    + `mkdir project_name` nos movemos dentro de la carpeta con `cd project_name` ya dentro de la carpeta podemos iniciar:

## Primeros pasos:

+ `git init:` Para tener el control de cambios y versiones en nuestro proyecto
+ `npm init:` con este comando vamos a crear nuestro archivo de configuración del proyecto, el `package.json`

Luego nos saldrá lo siguiente:
+ `package name`: el nombre de nuestro proyecto, generalmente es el nombre de la carpeta
+ `version`: version con la que iniciaremos el proyecto, generalmente aparece 1.0.0
+ `description`: descripcion breve del proyecto
+ `entry point`: punto de acceso a nuestro proyecto
+ `test command`: comando para gestionar los test
+ `git repository`: repositorio de github u otro servicio
+ `keywords`: palabras claves del proyecto
+ `author**`: nombre del autor y < correo > 
+ `**license`: licencia que tendrá el proyecto

```
    <h3>2da opción (para hacer package rápido)</h3>
```
Escribimos `npm init -y` y esto generará un package.json vacio para que lo configuremos más adelante.

``` 
    <h3>3ra opción (configuramos algunos elementos)</h3>
```

Escribimos en nuestra terminal:
```
    npm set init.author.email "your@email" (enter)
    npm set init.author.name "your name" (enter)
    npm set init.license "license name" (enter)
    npm init -y (enter)
```
Y se creará un package.json con los datos que seleccionamos.

Recomiendo mucho leer la documentación de package.json en el sitio de npm: https://docs.npmjs.com/files/package.json.html

![v4](./img/v4.jpg)



# 📒 v5 - Instalación de dependencias

Son las dependencias que aportan algo extra al proyecto pero que no son necesarias para que el proyecto funcione. Por lo que si su instalación falla por cualquier motivo el proyecto es totalmente funcional.

Un ejemplo de esto es si quieres decorar los logs en la consola, puedes agregar un paquete como chalk que te ayudará a lograrlo. El proyecto va a funcionar igual asi los logs no estén decorados, por lo que este sería un paquete opcional.

Listar paquetes instalados de forma global
```
    npm list -g --depth 0
```

🟢 npm install moment --save : Paquete que se encarga de manejar las fechas en JavaScript
🟢 --save : El documento que vamos a instalar dentro del proyecto es necesario para vivir en produccion.
🟢 -dev : El documento que vamos a instalar solo es necesario en nuestro entorno local o en el entorno de desarrollo
🟢 npm install date-fns : Al igual que moment se encarga de manejar fechas y datos
🟢 npm i : abreviacion de nmp install

🟢 -D : abreviacion para --save-dev

Evita tener que hacer sudo cuando hagas un `npm i -g` Con estos tips del equipo de NPM 👉 https://docs.npmjs.com/resolving-eacces-permissions-errors-when-installing-packages-globally

**Demonio:** Servicio que corre en segundo plano en el sistema:
```
    npm install -g nodemon
```
nodemon: demonio que nos permite escuchar algun cambio o valor para activar un proceso o comando que este a la espera. 

Para ver los paquetes o dependencia instalados de forma global
```
    npm list -g --depth 0
```

# 📒 v15 

![resumen completo](./img/v4.png)
