# Proyecto (angularStreaming)

Este es una clásica plataforma de streaming, elaborado en Angular versión 13.3.4
Bootstrap como CSS, posee un sistema de autentificación con auth0, protección de rutas sensibles con canLoad, canActivate, lazy loading, y todo en módulos.

Guard para hacer funcionar la protección canLoad, ya que el de auth0 no manda a identificar el usuario en canLoad con el Guard que él trae, este que posee el proyecto si lo hace y se implantó para evitar que se carguen componentes si el usuario no está debidamente identificado lo redirige al login

## Como hacerlo funcionar

Instale las dependencias del proyecto:

```bash
npm install
```

Agregue las siguientes configuraciones en **constant.js** archivo ubicado en el directorio del proyecto:

```bash
// Datos de auth0
const AUTH0_AUDIENCE = '';
const AUTH0_DOMAIN = '';
const AUTH0_CLIENTID = '';
const AUTH0_REDIRECT_URL = 'https://ddddd.com/auth'

// Server url
const SERVER_URL = '';
```

Los datos de Auth0 los puedes obtener en el Dashboard.

https://manage.auth0.com/dashboard/

**AUTH0_AUDIENCE** =

**AUTH0_DOMAIN** =

**AUTH0_CLIENTID** =

**AUTH0_REDIRECT_URL**= La URL que coloques aquí la tienes que agregar como callback permitidos en la configuración de auth0 y muy importante el callback debe de ser la URL donde está el proyecto sumándole  **/auth** al final 

**Ejemplo:** `https://ddddd.com/auth`

**SERVER_URL** = Esta es la URL del servidor donde se va a consumir la data
<br/><br/><br/>
**Ya con las configuraciones listas:**

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
