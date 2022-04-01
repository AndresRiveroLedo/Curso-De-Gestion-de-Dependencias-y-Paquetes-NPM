# 📒 v1 - Acerca de NPM, paquetes y módulos

## ¿Qué es NPM (node package manager) ? 

De sus siglas NPM (Node Package Manager) es un gestor de paquetes desarrollado en su totalidad bajo el lenguaje JavaScript por Isaac Schlueter, a través del cual podemos obtener cualquier librería con tan solo una sencilla línea de código, lo cual nos permitirá agregar dependencias de forma simple, distribuir paquetes y administrar eficazmente tanto los módulos como el proyecto a desarrollar en general.


Es un gestor de paquetes, el más popular que tiene JavaScript, donde encontrarás una gran cantidad de recursos para poder implementar en tus proyectos. También vas a poder crear tus propios paquetes y compartirlos con toda la comunidad.

Enlace oficial: https://www.npmjs.com/

## ¿Que diferencia hay entre NPM y YARN?

Ambos tienen el mismo propósito, manejar paquetes para aplicaciones Javascript. NPM es más grande, tiene más cantidad de dependencias. Pero Yarn tengo entendido que utiliza APIs de NPM para descargar dependencias de ahí.
Una ventaja que ofrece Yarn es la posibilidad de cachear las dependencias para descargarlas rápidamente y sin internet. Pero desde luego que es más utilizado NPM.

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

Listar paquetes instalados de forma global.
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

PD: Instalar siempre los paquetes dentro de la carpera raíz del proyecto. 

## ¿Cómo puedo saber si una librería es de desarrollo o de producción?

Para saberlo tienes que preguntarte siempre ¿Esta librería la necesita mi proyecto para correr o nada más la estoy usando yo para que el desarrollo se me haga más sencillo?

Sé que en un principio puede no ser tan fácil de responder, pero uno le va agarrando el truco.

Te dejo un par de ejemplos:

Eslint: ¿Esta librería la necesita mi proyecto para correr? No, esta librería lo que hace es marcarme los errores mientras estoy escribiendo el código.

Babel: ¿Mi proyecto necesita esto para correr? No, la estoy usando para que todo el código de JavaScript que estoy usando se compile en un archivo que entiendan todos los navegadores.

React: ¿Mi proyecto necesita esto para correr? Si, sin esta librería mi proyecto deja de funcionar.

## ¿Que quiere decir instalar de forma “opcional” un paquete?

En tu proyectos puedes tener dependencias que son opcionales, es decir, que el proyecto puede correr hasta cierto punto. una ventaja para este tipo de dependencias es que puedes acelerar el proceso de instalación de los proyectos.

Imagina que tiene un proyecto donde aplicas integración continua y un conjunto de pruebas. Y tienes estos 4 trabajos: construcción, linting, pruebas unitarias y pruebas de extremo a extremo. En cada una de ellas se instalan las dependencia en primer lugar, pero puede ocurrir que una dependencia la necesites solo en el ultimo paso, ahí es donde la dependencia opcional es una buena opción y evitas que se instale y tarde más.

para instalar una dependencia opcional usa el siguiente comando

```
 npm install paquete --save-optional
```

Esto agregara tu dependencia al optionalDependencies de tu package.json

Y puedes usar el flag –no-optional para no instalar los paquetes.

En este enlace puedes conseguir información acerca del tipo de dependecias

https://docs.npmjs.com/cli/v6/configuring-npm/package-json

## Carpeta node_modules

La carpeta node_modules se crea al instalar el primer modulo, paquete o dependencia. En esta carpeta se instalará los modulos que iremo creando o instalando. Esta carpeta debemos de ignorarla como buena práctica en el archivo .gitignore

## ¿Cuál es la diferencia entre librería, módulo, paquete, dependencia?

+ Módulo. La pieza más pequeña de software. Puede ser un conjunto de métodos o funciones para usarlo.

+ Paquete. Colección de módulos.

+ Librería. Colección de paquetes.

+ Framework. Conjunto de librerías. No solo ofrecen funcionalidades, sino que también arquitectura. Uno no incluye un framework, uno incluye código dentro de un framework.

+ Dependencia. Se refiere a cuán interconectados están los módulos. O sea, que tu software depende de módulos para funcionar.

## ¿Porqué se ignora los modulos y no se envian a nuestro repositorio?

Porque normalmente al descargar o clonar el proyecto y ejecutar npm install la carpeta node modules se reconstruye, esto es gracias al manejador de paquetes, ya sea npm o yarn.

## ¿Qué significa que un paquete se instale de forma opcional?

Hacen referencia a dependencias que no necesariamente impiden el funcionamiento de tu app.

## ¿Y como se cuales dependecias debo instalar con el comando --save?

+ –save
    + Dependencias
        + Paquetes necesarios para el funcionamiento de tu aplicación.
    + Ejemplo:
        + React
        + Next
        + React-Dom
+ –save-dev
    + Dependencias de desarrollo
        + Paquetes que se usan en el ambiente de desarrollo
    + Ejemplo:
        + Grunt
        + Sass
        + Typescript


## ¿cuando se instala una dependencia sin especificar si es --save o --save-dev . Que flag toma por default?

Anteriormente tenias que especificar algun flag, pero en npm hicieron unos cambios y ahora el flag por defecto es –save, este flag permite que se actualice tu archivo package.json

Hay otras opciones como –save-dev que actualiza el devDependencies en tu package. Con esto puedes usar la dependencia solo en desarrollo local y para hacer pruebas.

Tambien tienes la el flag –no-save* que instala la dependencia pero no actualiza tu package.

Aquí puedes conseguir información con mas detalle

https://docs.npmjs.com/cli/v6/commands/npm-install

# 📒 v6 - Instalación de dependencias con force

## Instalación de Dependencias
+ En nuestro proyecto jsnpm creamos una carpeta con `mkdir src` que es donde va a vivir todos los archivos que van a consumir todos los recursos que hemos instalado, 
+ Despues creamos un archivo con `touch index.js`
+ Ahora hay que hacer `pwd` que nos indica la ruta donde estamos ya que las dependencias se deben instalar en nuestra carpeta raíz de nuestro proyecto y entonces nos movemos a esta raiz
+ Después para instalar un paquete, es aquí donde tomamos la decisión de como lo vamos a ejecutar,
    + En el momento que instalamos el primer paquete se nos creara una carpeta `node_modules` aqui se instalaran lo modulos que estamos agregando a nuestro proyecto y sera necesaria para que este funcione, pero no debe ser enviada a ningun repositorio ni a nuestro proyecto a producción y por eso debemos ignorarla al nos mas se cree y para ello creamos un archivo `.gitignore` en la carpeta raiz y dentro de este escribimos `node_modules/`
    + `npm install <package>` este por defecto se instala como una dependencia requerida para el proyecto es decir que el paquete que instalas es necesario para vivir en produccion esto tiene otras variantes como `npm install <package> --save` aqui la palabra save se tomara por defecto y no es necesario escribirla o `npm install <package> --S` como ejemplo instalaremos npm install moment para manejar fecha en javascript o con el shortcut npm install moment --S

```
    "moment": {
        "version": "2.29.1",
        "resolved": "https://registry.npmjs.org/moment/-/moment-2.29.1.tgz",
        "integrity": "sha512-kHmoybcPV8Sqy59DwNDY3Jefr64lK/by/da0ViFcuA4DH0vQg5Q6Ze5VimxkfQNSC+Mls/Kx53s7TjP1RhFEDQ=="
        }
```
+ `npm i <package> -D` (este es con shortcut) o `npm install <package> -save-dev` este flag nos va a permitir establecer que el paquete a instalar solo es necesario en nuestro entorno local o el entorno de desarrollo ejem: vamos a instalar una dependencia que maneja fecha y datos npm install date-fns save-dev
```
    "dependencies": {
        "date-fns": {
        "version": "2.16.1",
        "resolved": "https://registry.npmjs.org/date-fns/-/date-fns-2.16.1.tgz",
        "integrity": "sha512-sAJVKx/FqrLYHAQeN7VpJrPhagZc9R4ImZIWYRFZaaohR3KzmuK88touwsSwSVT8Qcbd4zoDsnGfX4GFB4imyQ==",
        "dev": true
        }
```

+ `npm install <package> -g` instalar un paquete de forma global, esto nos permite que podamos utilizar este paquete en diferentes proyectos por lo general se deben instalar estos paquetes con permisos de administrador. Ejem. sudo npm install -g nodemon nos permite generar un demonio que va a estar siempre escuchando algun cambio o algun valor y nos va dejar mantener en nuestro proceso algun comando que estemos ejecutando de node

Guia para no esta colocando permisos de administrador a cada rato https://docs.npmjs.com/resolving-eacces-permissions-errors-when-installing-packages-globally

+ `npm list -g—depth 0` (depth es la profundidad que va a buscar dentro de los paquetes) ver los paquetes que están instalados de forma global.

/usr/lib
├── nodemon@2.0.6
└── npm@6.14.8

+ `npm list`: es para listar los paquetes que tienen un proyecto en especifico
+ `npm install <package> -O` podemos instalar de forma opcional un paquete con este comando ejemplo instalaremos eslint para correcciones de codigo en JS npm install eslint -O y cuando finalizamos siempre nos un output de mensajes y tiempos de ejecucion en este ejemplo
```
    //nos disce que podemos donar y que ejecutamos npm fund para apollar
    //a los desarrolladores
    10 packages are looking for funding
    run `npm fund` for details
```
+ npm install <package> --dry-run (simula la instalación) este flag indica que el paquete no va a ser instalado dentro del proyecto simplemente es una simulación nada mas nos muestra el output como si fuere instalado, despues de esto nosotros decidimos si la instalamos o no ejem: npm install react --dry-run
npm install <package> -f o npm install <package> --force instalar algún paquete de forma forzada y nos va a permitir instalar este paquete forzándola a que sea desde el ultimo recurso o version y desde el servidor de NPM ejemplo npm install webpack -f si nos vamos al archivo package.json y vemos que el paquete se instalo en las dependencies pero estas deberieron estar en devdependencies podemos tomar el nombre de ese paquete cortarlo y pegarlo en el grupo que corresponda
```
//asi se instalo en dependecies
"dependencies": {
    "date-fns": "^2.16.1",
    "eslint": "^7.12.1",
    "moment": "^2.29.1",
		"webpack": "^5.3.2"
  },
  "devDependencies": {
    
  },

//nosotros lo cortamos y lo pegamos en devDependecies
"dependencies": {
    "date-fns": "^2.16.1",
    "eslint": "^7.12.1",
    "moment": "^2.29.1"
    
  },
  "devDependencies": {
    "webpack": "^5.3.2"
  },
```
+ `npm install` si nosotros queremos volver a instalar todas las dependencias que están en el package.json
+ `npm install <package>@<version>` para instalar algun paquete con una versión específica, esto puede ser necesario cuando tenemos que darle mantenimiento a una app con una version anterior de algun paquete o quizas las version actual es beta, etc. ejem: npm install json-server@0.15.0

## json-server:

El paquete json-server es fantástico, se pueden hacer peticiones HTTP a un archivo json, yo lo uso con Ngrok y hago peticiones externas.

```
    Un error que cometemos al clonar un proyecto de un repositorio remoto, es querer iniciar la aplicación de forma local inmediatamente después de descargar el código. Seguramente, nada funcionará, debido a que no existe la carpeta node_modules que contiene las dependencias requeridas.
    Como regla, siempre ejecuten `npm install` después de clonar el proyecto.
```

## ¿No entendi como funciona –dry -run?

Básicamente lo que hace es simular la instalación para que veas que te devolverá, te dejo la documentación donde lo explica mejor.
Exacto, solo simula la instalacion y te entrega un output de que sucederia si lo instalaras.

## ¿Si hipotéticamente llegase a borrar el archivo package-lock que debería hacer para que vuelva a aparecer?

Simplemente escribe npm install y volverá a aparecer solito, recuerda que ese archivo se genera con base en tu package.json 😄

## “dependencies”, “devDependencies”, “optionalDependencies”. ¿Cual es su diferencia?
+ dependencies: Sirven para dependencias de producción, es decir, las que ajuro necesita nuestro codigo para funcionar correctamente.
+ devDependenciers: Sirven para ayudarnos a desarrollar pero no son esenciales para el funcionamiento del proyecto. Por ejemplo los paquetes de testing por lo general son dependencias de desarrollo, ya que una vez probado nuestro codigo ya no sera necesario estas dependencias en producción.
+ optionalDependencies: Estas tal vez nos podrian ayudar a desarrollar y no son esenciales para el funcionamiento del codigo. Por ejemplo cowsay es un paquete que te permite dibujar en la terminal una vaca que habla, no sirve para desarrollar tampoco para el funcionamiento de la aplicación pero es divertida jejejeje


Cuando instalas un paquete con npm de forma global por ejemplo
```
    npm i -g my-package
```
tu puedes llamarlo directamente en tu terminal (como si fuera un programa normal) por ejemplo:
```
    my-package my-file.js
```

pero como llamas un programa que instalaste de forma local?
```
    npm i -D my-package
```
debes hacerlo de la siguiente forma (mas o menos):
```
    /node_modules/path/to/my/package my-file.js
```

pero no es practico verdad? entonces podemos hacer que npx resuleva la ruta para ejecutar nuestro paquete (instalado de forma local, ya sea dev dependency o no):
``` 
    npx my-package my-file.js
```

npx es un comando adicional a npm que ejecuta los programas instalados mediante npm

# 📒 v7 - Actualizar y eliminar paquetes

## Actualizar paquetes

+ Revisar que paquetes disponen de nuevas versiones
```
    npm outdate
```
+ Para ver un output más detallado
```
    npm outdate --dd
```
+ Actualizar los paquetes que no están en la ultima versión
```
    npm update
```

+ Actualizar un paquete especifico
```
    npm install json-server@latest
```
![update](./img/v7.webp)

## Actualizar y eliminar
+ `npm outdate` es para ver si se algún paquete se encuentran desactualizados y además nos indica la últimas versiones de estos paquetes, dándonos la version actual (current) , recomendada(wanted) y la mas actualizada (Latest)
+ `npm outdate --dd` con el `flag --d` podemos ver todo el output mas detallado viendo lo que esta pasando por detrás de npm osea como hace cada operación hasta llegar a el output final
+ `npm update` podemos actualizar todos los paquetes que se encuentran desactualizados
+ `npm install <package>@latest` podemos actualizar un paquete en especifico a su ultima versión con este comando ejem: npm install json-server@latest
+ `npm uninstall <package>` para desinstalar o eliminar un paquete en especifico esto lo elimina del package.json y node_modules , Ojo muchas veces lo borramos del archivo package.json pero esto no lo elimina de la carpeta node_modules por lo tanto es una buena práctica ejem: 
+ `npm uninstall json-server`
+ `npm uninstall <package> --no-save` nos permite desinstalar o eliminar un paquete pero sin eliminarlo del package.json pero si del node__modules, 
    + ejem: `npm uninstall webpack --no-save` podemos instalar un plugin `npm egamma` en VSCode que nos revisa nuestro package.json vrs la carpeta de node_modules para comparar si hay dependencias que están agregadas en package.json pero no en la carpeta de node_modules (Ojo hay que revisar si efecto se elimino de node_modules ay que parece cuando esta en devDependencies no se elimina)

##  Eliminar paquetes
+ Eliminar un paquete de node_modules y del archivo package.json
```
    npm uninstall json-server
```
+ Desinstalar un paquete de todo node_modules pero no del archivo package.json
```
    npm uninstall webpack --no-save
```

## ¿Por qué motivo elimino un paquete de node_modules pero lo dejo en el package.json?

A veces se corrompen los paquetes o algún conflicto extraño pasa. Yo he borrado paquetes del node_modules y los he dejado en el package.json para después hacer un npm install y obtener una versión nueva y funcional del paquete. Cuidado aquí con las versiones, mirar semver.

Si tiene conflictos de dependencias pueden usar el coamando:
```
    npm ci
```
que significa clean install y lo que hace es borrar todo y instalar de nuevo en un solo paso


## Cuando usamos npm install json-server@latest, por ejemplo. ¿Se elimina la versión anterior que tengamos instalada?

Si, pero se puede mantener si instalas otra versión especifica dentro del paquete, también puedes usar alias para tener varias instalaciones.

## ¿npm update o npm outdate corrobora las actualizaciones dependiendo la configuración que tiene package.json?

asi es  por su puesto, el comando `npm update` respeta tu version constrain (ese es el nombre origianl) solo que el comando `npm outdate` te la seguira marcando como desactualizada.
si usas el comando npm i <package>@latest ese no te respera el constrain

¿ Se podría llegar a afectar otros paquetes al momento de actualizarlos?

Es muy raro que llegue a pasar eso.

## ¿Podrian ayudarme a entender cual es la diferencia de npm Update a npm install name_package@latest ?

Lo que pasa es que npm Update actualiza todos de manera general a la versión mas estable en el server npm, en cambio el otro al poner @latest se dice de manera explicita que se requiere es la ultima de todas.

# 📒 v8 Package lock y el uso los símbolos ^ y ~

## Versionado Semántico

+ En el versionado tenemos 3 dígitos que significa:
    + Primer dígito: son cambios mayores
    + Segundo dígito: añaden ciertas funcionalidades pero no representan un gran paso para decir que esta es una versión nueva
    + Tercer dígito: estos son patch, bug fixes o cambios menores
+ Cuando tenemos el símbolo (^) catet dentro de la configuración del package.json estamos garantizando que cuando nosotros hagamos una actualización o tengamos un cambio que podamos realizar, vamos a hacer actualizacion solo de los cambios menores y de los parches o bug fix de este paquete.

+ También podemos establecer una tilde (~) esto quiere decir que vamos a recibir actualización o cambios que son parch o bug fixes.

+ Lo recomendo si queremos tener el control sobre estas actualizacion garantizando que nos queremos quedar en cierta versión lo mejor es elimina el caret (^)

+ `Package-lock.json` a partir de la versión 5 npm encontramos este archivo que nos permite tener ciertas configuraciones la cual nos permite saber que esta sucediendo a lo largo de nuestro proyecto sabiendo que versiones, que paquetes y que dependencias se encuentran en este, permitiendonos tener un versionado uno poco mas establecido, podremos compartir este documento con los demás desarrolladores y garantizar que las versiones que se están instalando sean las correctas, al igual nos sirve para cuando los proyectos estén en la nube y nuestro servidor instale de manera automática todas estas dependencias

![v8](./img/v8.jpg)

+ Además de esos símbolos, también tenemos:
    + < : Versión menor a la indicada.
    + <= : Versión menor o igual a la indicada.
    + > : Versión mayor a la indicada.
    + >= : Versión mayor o igual a la indicada.

Hasta donde sabía, el package-lock era como un mapa más detallado de nuestro proyecto, el cual ya tenía todas las versiones y todo escrito para que npm unicamente las instalara sin tener que volver a hacer una búsqueda, etc.

Y como resumen, en teoría cuando usas “^” permites el update de cambios menores y cuando usas “~” permites el update de bugfixes unicamente, y esto es útil para aquellos servicios que hacen los updates de nuestros paquetes automáticamente ^^

## No me quedó claro exactamente para que sirve el package-lock

Anteriormente cuando sólo teníamos el package.json, pasaba que al clonar un paquete y hacer npm install se instalaban actualizaciones menores que rompían el paquete, todo por lo permisivo de semver.

Ahora el archivo package.json.lock se encarga de presentar una captura estática del árbol de dependencias que estamos incluyendo en un proyecto. Ahora se respeta la versión exacta de la dependencia indicada, así cualquier persona del equipo, cuando ejecute npm install, será capaz de reproducir el mismo árbol que el de su compañero sin problemas dando estabilidad dentro de los proyectos.

## No me queda claro cuales son esas “ciertas configuraciones” que tiene el archivo package-lock.

¡Hola!, no te preocupes, el archivo package-lock.json rara vez lo vas a tocar.

Este archivo contiene información mucho más detallada de los paquetes que están instalados, es decir, el package.json contiene únicamente nombre y versión, pero el package-lock.json contiene más información que solo eso, digamos que es un mapa más detallado de las dependencias de nuestro proyecto, este se genera automáticamente partiendo del package.json, por eso te digo que rara vez lo vas a tocar, porque mayormente vas a modificar el package.json, no el package-lock.json

## es decir que si hay una actualización en el major ( un cambio mayor) no se actualizará mi paquete automáticamente? Solamente se podrán realizar cambios automáticos minor y patch?

De acuerdo a lo que vi en la clase, cuando se hacen los cambios en major es porque cambió toda la estructura, por ende cambiario minor y patch, ya que son solamente para cambios menores y parches. Esta es mi opinión que te comparto de lo que vi en esta clase. Ojalá más gente de la comunidad se sume a este comentario muy bueno que acabas de hacer. 

## Que es lo que vino a resolver el archivo package-lock.json?

Básicamente se asegura de que las versiones de las dependencias sean las mismas a las que nuestro software soporta al momento de que alguien más comienza a trabajar en el proyecto. Esto en base al Package.json.

# 📒 v9  Ejecutar tareas

Ejecutar tareas o script los cuales son comando que podemos establecer y ejecutar desde la consola, y podemos crear los que necesitemos además van a correr de forma nativa dentro de nuestra terminal, para nombrarlo debe ser un shortcut de lo que vamos a ejecutar con npm run <script-name>
```
    "scripts": {
        "build": "webpack --mode production",
        "start": "webpack-dev-server --open --mode development",
        "format": "prettier --write '{**.js,src/**/*.{js,jsx}}'"
        "lint": "eslint src/ --fix",
        //aqui podemos concatenar dos comandos
        "deploy": "npm run format && npm run build"
    }
```

Puedes también especificar scripts con el prefijo “pre” que se ejecutarán automáticamente antes del comando que ejecutaste. Por ejemplo, si defines el comando build y prebuild, cuando corras npm run build el comando prebuild se ejecutará primero. Esto sirve para poder ejecutar tareas que hagan algún tipo de preparación necesaria para correr el comando principal. Sin embargo, hay que hacer notar que si el comando pre falla (retorna un valor que no es 0) el comando principal no se ejecutará. Esto es algo bueno ya que si nuestro proceso de preparación no se realiza de forma exitosa, puede que tengamos problemas al querer ejecutar la tarea principal.

```
    "presass-build": "(rm css/*.css; rm css/*.css.map) || exit 0"
```

Ese es un ejemplo de un comando que hice hace un tiempo. rm puede fallar si el directorio css está vacio, y en ese caso no hay problema, la tarea principal puede funcionar sin ningún problema ya que presass-build tiene el propósito de vaciar ese directorio.

En algunas ocaciones, sin embargo, la tarea previa puede fallar sin que eso afecte la ejecución de la tarea principal. En esos casos puedes usar || exit 0 para retornar 0:


Algo que también faltó mencionar es que `npm run` agrega el directorio ./node_modules/bin/ al PATH de modo que para ejecutar un comando no es necesario agregar la ruta completa. Esto es algo que hace tiempo me confundió, cuando vi que Laravel ejecuta un comando setenv y yo quice buscarlo en mi computadora con which setenv y resultó que el comando no existía. Esto es porque en realidad el binario está ubicado en node_modules/bin/

Añadir comandos a npm suele ser buena idea pues nos ayudan a tener shortcuts de comandos más largos, lo genial es que frameworks como Vue ya traen pre escritos estos comandos para que solo nos preocupemos en desarrollar.

## ¿que es lo que hace exactamente lo que quiso decir el profesor del comando npm run test y npm start?

npm start y npm test son alias para los comandos npm run start y npm run test, eso significa que al ser muy utilizados se provee una solución para ejecutar los comandos de una manera más corta (sin la palabra run).

## ¿Que significa llevar un proyecto a produccion?

Hola Juan!
En la vida real, es decir, en los trabajos 😛
El código se trabaja en una area para llama pre-producción para hacer ahí todo el testing y ver si realmente el el código y el programa está funcionando como se desea.
Cuando pasa las pruebas de los testers, se sube, copia, duplica (depende de la arquitectura del software) se pasa a producción, es decir, a otro server.

## ¿Que significa hacer un deploy?

En términos generales, la palabra deploy es utilizada para describir que algo fue colocado en su posición. También se utiliza cuando un sistema es habilitado para su uso, ya sea un ambiente de desarrollo, para realizar pruebas o producción.

Básicamente es desplegar/publicar tu aplicación o tu web haciendo uso de algún servicio de infraestructura (servidores, dominios, redes, etc). Un ejemplo es cuando usas los servicios que tiene Github para publicar algo que tengas en tu repositorio, en el momento en que tu sitio o aplicación esta disponible para que se pueda visitar significa que fue desplegada.

## Puedo ejecutar dos librerias en una sola tarea?

Si en tu paquete en la seccion de script especificars que tarea correr y una tarea puede corrar 2 o mas.

# 📒 v10 - Solución de problemas

Cuando estés trabajando con proyectos que están usando NPM te vas a topar con una gran cantidad de posibles errores que vas a tener. Estos errores pueden ser desde la configuración, pueden ser desde el sistema operativo, espacios, no haber configurado correctamente tu GitHub, no haber establecido bien los datos del package, haber dejado un typo u algún elemento extraño dentro de esta configuración así como una serie de errores que pueden generarse, que no están ligados directamente a NPM.

+ Uno de los problemas que podemos toparnos en la construcción de nuestro proyectos trabajando con un equipo es que nuestros archivos de node__moduls no estén correctamente instalados o tengamos una versión anterior, una forma de solucionarlo es eliminar la carpeta de ‘node_modules’ o ejecutar un comando que a nosotros nos va a dar seguridad de limpiar ese ‘cache’ que pueda llegar a existir.
    + `npm run build --d` lo primero es poder ver todo el detalle de la ejecución de nuestro comando y lo hacemos con el flag --d para esto tenemos que leer detenidamente y así poder determinar la causa de nuestro error, de la misma forma al final no deja un archivo .log que podemos abrir con el comando code <ruta> este archivo nos dará una bitácora de toda la ejecución
    + `npm cache clean -f` o npm cache clean --force eliminar la caché
    + `npm cache verify` con este vamos a poder ver si ya la cache ha sido eliminada y que todas las instalaciones de nuestros recursos van a ir hacia los servidores de NPM
    + `rm -rf <Carpeta/>` Eliminar una carpeta y después corremos npm install para que se vuelvan a instalar todas las dependencias.
    + `sudo npm install -g rimraf` este ayuda al borrado de la carpeta de carpetas de forma segura y los instalaremos de forma global, ahora para ejecutarlo lo haremos con el comando rimraf <carpeta>

## ¿Entonces, si me traigo un proyecto y no tengo las dependencias que necesita para correr, tengo que ejecturar npm install antes de poder correrlo?

Si así es, siempre que descargues un proyecto de Github este viene acompañado de un archivo package.json el cual contiene las dependencias necesarias para funcionar ejecutas npm install y va a instalar las dependencias luego ya puedes correrlo con su respectivo comando.

## ¿Cual es diferencia de rm -rf y rimraf?

+ rimraf es un paquete adicional para que puedas eliminar de forma segura la carpeta de node_modules.

+ rm -rf es el comando de los sistemas basados en Unix (Linux y Mac) para eliminar de forma recursiva y forzada.

## ¿Cual es la diferencia ente -f y --force?

 ninguna, sólo se escribe de manera diferente. Generalmente con un guion y una letra seria la abreviacion del comando con dos guiones y la palabra entera.

 # 📒 v11 - Seguridad

## Seguridad
+ `npm audit` para ver las vulnerabilidades que tenemos en nuestro proyecto
+ `npm audit --json` nos genera un json con información un poco mas detallada de lo que esta pasando con estos paquetes que instalamos
+ Una ves sepamos cual es la vulnerabilidad podemos proceder a actualizar cualquiera de los paquetes ejem: `npm update eslint-utils --depth 2` esto para instalar todas sus dependencias
+ `nom audit fix` es para solucionar las vulnerabilidades que tengamos en nuestro proyecto básicamente, actualiza a la ultima version nuestros paquetes con las dependencias que requieren, después de esto volvemos a correr npm audit para ver que ya no tenemos vulnerabilidades.
+ También hay una herramienta que garantiza que estemos siempre actualizados con nuestras dependencias del proyecto y es snyk.io

Genial, algo curioso es que si tienes un proyecto en GitHub, hay una cosa llamada DependaBot que igual busca estas vulnerabilidades en tus paquetes y te hace un pull request solucionándolas, aunque no se qué tan parecido sea a npm audit 🤔


 ## ¿Sería recomendable primero intentar solucionar con npm audit fix y lo que no se solucione lo actualizamos de a uno?

 Sí, ese seria el camino idóneo para auditar nuestros proyectos.

 ## Porque 2 y no 1 o 3 cuando ejecuto el comando npm update eslint-utils --depth 2

No siempre es 2 el depth tienes que ejecutar primero el comando npm audit y en el reporte te da detalles del error y e comando que necesitas correr, en el caso de oscar le aparecio

# 📒 v15 

![resumen completo](./img/v4.png)
