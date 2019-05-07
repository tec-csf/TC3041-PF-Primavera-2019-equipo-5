# TC3041 Proyecto  Final Primavera 2019

#*ADMINISTRACIÓN DE COLEGIOS*
---

##### Integrantes:
1. [Joan Andoni González Rioz](https://github.com/JoanAndoni)
2. [Alejandra Tubilla Castellanos](https://github.com/alejandratub)


---
## 1. Aspectos generales

### 1.1 Requerimientos técnicos

- MongoDB 3.6.9

- node.js 11.9.0
- npm 6.5.0

- Angular CLI: 7.0.4
- rxjs 6.3.3

- Docker 18.09.2

- Minikube 1.0.0

-Google SDK de cloud

### 1.2 Estructura del repositorio

```
- / 			        # Raíz de todo el proyecto
    - README.md			# Archivo con los datos del proyecto (este archivo)
    - frontend			# Carpeta con la solución del frontend hecha en Angular 6 (Web app)
    - backend			# Carpeta con la solución del backend hecho con node.js (CMS)
    - dbs			# Carpeta con los modelos, catálogos y scripts necesarios para generar las bases de datos
    - backend/models			# Carpeta donde se almacenan los modelos de datos que utilizamos para este proyecto
    <!-- - docs			# Carpeta con la documentación del proyecto
        - stage_f               # Documentos de la entrega final
        - manuals               # Manuales y guías -->
```

### 1.3 Documentación  del proyecto

Como parte de la entrega final del proyecto, se debe incluir la siguiente información:

* Descripción del proyecto.

* Descripción del o los *datasets* y las fuentes de información utilizadas.

* Guía de configuración, instalación y despliegue de la solución en la plataforma en la nube  seleccionada.

* Documentación de la API. Puede ver un ejemplo en [Swagger](https://swagger.io/).

* El código debe estar documentado siguiendo los estándares definidos para el lenguaje de programación seleccionado.

## 2. Descripción del proyecto

EL proyecto consiste en una administración de colegios, en la que se dan de alta profesores y alumnos. 

Existen tres roles diferentes dentro del sistema:

  1. Profesor
  2. Alumno
  3. Administrador

Cada profesor tiene asignadas materias por grado y grupo, y cada alumno tiene asignadas diferentes materias. 

El profesor puede asignarle a cada alumno la calificación correspondiente a cada trimestre de la materia, así como comentarios relevantes respecto a las clase.

El alumno puede consultar sus calificaciones y los comentarios recibidos por parte de los profesores.

El administrador puede agregar nuevos profesores, alumnos y clases. Puede aceptar, rechazar o modificar los comentarios creados por los profesores. Crear un nuevo perfil de administrador o eliminar su perfil de administrador.

## 3. Solución

A continuación aparecen descritos los diferentes elementos que forman parte de la solución del proyecto.

### 3.1 Modelos de *bases de datos* utilizados

Utilizamos dos modelos diferentes de bases de datos, base de datos orientadas a documentos (MongoDB) y base de datos llave-valor (Redis). Ambas bases de datos fueron implementadas en sus servicios de nube que tienen clusters para almacenar la información necesaria RedisLabs y Mongo Atlas respectivamente.

Nuestro sistema nos demanda una base de datos orientada a documentos ya que tiene muchos datos que se van adicionando a los diferentes tipos de usuarios dependiendo de su rol asignado, al usar este tipo de base de datos es más sencillo de adicionar nuevos módulos conforme se vaya necesitando.

Usamos base de datos llave-valor para poder hacer un mejor manejo de los usuarios y las sesiones.

### 3.2 Arquitectura de la solución

*[Incluya aquí un diagrama donde se aprecie la arquitectura de la solución propuesta, así como la interacción entre los diferentes componentes de la misma.]*

### 3.3 Frontend

*[Incluya aquí una explicación de la solución utilizada para el frontend del proyecto. No olvide incluir las ligas o referencias donde se puede encontrar información de los lenguajes de programación, frameworks y librerías utilizadas.]*

#### 3.3.1 Lenguaje de programación

Los lenguajes de programación utilizados para el desarrollo del frontend fueron: HTML y TypeScript.

#### 3.3.2 Framework

El framework utilizado para el desarrollo del frontend fue: [Angular](https://angular.io/). Es un framework de código abierto, para el desarrollo de aplicaciones web de una sola página.

#### 3.3.3 Librerías de funciones o dependencias

Para el diseño de las vistas de la aplicación se utilizó [Bootstrap](https://getbootstrap.com/) una librería multiplataforma para el diseño de sitios y aplicaciones web.

Todas las dependencias se encuentran en el archivo "package.json" 

*[Rxjs](https://angular.io/guide/rx-library)

### 3.4 Backend

*[Incluya aquí una explicación de la solución utilizada para el backend del proyecto. No olvide incluir las ligas o referencias donde se puede encontrar información de los lenguajes de programación, frameworks y librerías utilizadas.]*

#### 3.4.1 Lenguaje de programación

El lenguaje de programación utilizado para el desarrollo del backend fue: [JavaScript](https://www.javascript.com/).

#### 3.4.2 Framework

El frameworks utilizado para el desarrollo del backend fueron: [Express](https://expressjs.com/es/) y  [NodeJs](https://nodejs.org/es/). NodeJs es un entrono de código abierto para la capa del servidor, mientras que Express es una infraestructura de aplicaciones web de NodeJs.

#### 3.4.3 Librerías de funciones o dependencias

Todas las dependencuas se encuentran en el archivo "package.json"

*[Braces](https://www.npmjs.com/package/braces)

*[Mail Service for the Sendgrid v3 Web API](https://www.npmjs.com/package/@sendgrid/mail)

*[Express Handlebars](https://www.npmjs.com/package/express-handlebars)

*[Method Overrides](https://www.npmjs.com/package/method-override)

*[Nodemon](https://www.npmjs.com/package/nodemon)

*[Bcryptjs](https://www.npmjs.com/package/bcryptjs)

*[Body Parser](https://www.npmjs.com/package/body-parser)

*[Cors](https://www.npmjs.com/package/cors)

*[Jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken)

*[Mongoose](https://www.npmjs.com/package/mongoose)

*[Passport](https://www.npmjs.com/package/passport)

*[Passport-jwt](http://www.passportjs.org/packages/passport-jwt/)

*[Redis](https://redis.io/)


## 3.5 Pasos a seguir para utilizar el proyecto


### Para ejecutarlo local

1. Clonar el repositorio de GitHub

`git clone https://github.com/tec-csf/TC3041-PF-Primavera-2019-equipo-5.git`

2. Cambiarse a la carpeta del proyecto

`cd TC3041-PF-Primavera-2019-equipo-5`

3. Cambiarse a la carpeta del backend

`cd backend`

4. Iniciar el backend de la aplicación, asumiendo que ya tiene NodeJs y todas las dependendias instaladas. En caso contrario, instalar primero NodeJs y sus dependiencias.

`npm start`

5. Abrir una nueca terminal y cambiarse a la carpeta del frontend del proyecto

`cd TC3041-PF-Primavera-2019-equipo-5/frontend`

6. Iniciar el frontend de la aplicación, asumiendo que ya tiene AngularCli y todas las dependendias instaladas. En caso contrario, instalar primero AngularCli y sus dependiencias.

`ng serve`

7. Abrir el navegador en el puerto 4200 para ver la aplicación funcionando

`http://localhost:4200`

**Nota: ya que la aplicación está usando Redislabs, puede ser que esté bloqueado el puerto de conexión. Si la aplicación no le permite hacer login es el caso, y es necesario conectarse a una red diferente.

### Para ejecutarlo local con Minikube

1. Clonar el repositorio de GitHub

`git clone https://github.com/tec-csf/TC3041-PF-Primavera-2019-equipo-5.git`

2. Iniciar el clúster de Minikube, asumiendo que ya lo tiene instalado. En caso contrario, instalar primero Minikube.

`minikube start`

3. Habilitar el contexto de Docker

`eval $(minikube docker-env)`

4. Carmbiarse a la carpeta del proyecto

`cd TC3041-PF-Primavera-2019-equipo-5`

5. Compilar las imágenes de Docker

`docker build -t frontend-image frontend/.`

`docker build -t backend-image backend/.`

6. Desplegar la solución en el clúster de Kubernetes.

`kubectl apply -f equipo5.yaml`

7. Obtener la IP del clúster de Minikube

`minikube ip`

8. Obtener el puerto donde se encuentra escuchando el servicio

`kubectl get svc`

9. Acceder a la aplicación en un browser

`http://<IP-Minikube>:<Puerto-Servicio>`

### Para ejecutarlo en la nube (Google Cloud)

1. Entra a la consola de Google Cloud Platform (GCP)

`https://console.cloud.google.com`

2. Dentro de la plataforma entra a Compute/Kubernetes Engine y crea un nuevo cluster

3. Una vez creado el cluster correctamente accede a el por medio de "Cloud Shell". Da click en "conectar"

4. Una vez conectado al cluster clonar el repositorio de Gitub

`git clone https://github.com/tec-csf/TC3041-PF-Primavera-2019-equipo-5.git`

5. Cambiarse a la carpeta del proyeto

`cd TC3041-PF-Primavera-2019-equipo-5`

6. En la terminal de tu equipo clonar el repositorio de Github

`git clone https://github.com/tec-csf/TC3041-PF-Primavera-2019-equipo-5.git`

7. Cambiarse a la carpeta del frontend del proyecto

`cd TC3041-PF-Primavera-2019-equipo-5/frontend`

8. Crear la imagen del forntend usando el comando

`docker build -t gcr.io/[id del proyecto de GCP]/frontend-image`

9. Dar push a la imagen del frontend usando el comando 

`docker push gcr.io/[id del proyecto de GCP]/frontend-image`

10. Cambiarse a la carpeta del backend del proyecto

`cd TC3041-PF-Primavera-2019-equipo-5/backend`


11. Crear la imagen del forntend usando el comando

`docker build -t gcr.io/[id del proyecto de GCP]/backend-image`

12. Dar push a la imagen del frontend usando el comando 

`docker push gcr.io/[id del proyecto de GCP]/frontend-image`

13. Dentro de la consola de GCP modifica el archivo "equipo5.yaml" y cambia el nombre de la imagen del frontend en la línea "37" y el nombre de la imagen del backend en la línea "42"

`imagen del frontend: gcr.io/[id del proyecto de GCP]/frontend-image`

`imagen del backend: gcr.io/[id del proyecto de GCP]/backend-image`
 
 14. Desplegar la aplicación en el cluster
 
 `kubectl apply -f equipo5.yaml`
 
 15. Comprobar que el pod está funcionando correctamente (el Status debe ser Running)
 
 `kubectl get pods`
 
 16. Obtener la dirección ip externa y el puerto
 
 `kubectl get service`
 
 17. Exponer la apliación a internet
 
 `kubectl expose deployment frontend-app --type=LoadBalancer --port 80 --target-port [puerto asignado]`
 
 18. Acceder a la aplicación en un browser
 
 `http://[ip externa]`
 
 
 ### Para usar la aplicación
 
 Teniendo la apliación corriendo (con cualquiera de los métodos previamente explicados), hacer login.
 
 **Como administrador:**
 
    `matricula: alejandra` 
    
    `contraseña: 12345`
    
 **Como profesor:**
 
   `matricula: P01`
   
   `contraseña: 12345`
   
   (Como administrador puedes agregar un nuevo profesor e ingresar después con esas credenciales)
   
   **Como alumno:**
   
   `matricula: K208`
   
   `contraseña: 12345`
   
   (Como administrador puedes agregar un nuevo alumno e ingresar después con esas credenciales)
   
 
 

## 4. Referencias

1. [Conexión con Redislabs](https://docs.redislabs.com/latest/)
2. [Conexión con Mongoose](https://mongoosejs.com/docs/guide.html)
3. [Crear un contenedor de docker con Angular](https://scotch.io/tutorials/create-a-mean-app-with-angular-2-and-docker-compose)
4. [Crear un contenedor de docker con Node.js](https://nodejs.org/en/docs/guides/nodejs-docker-webapp/)
5. [Implementar una aplicación web en contenedor](https://cloud.google.com/kubernetes-engine/docs/tutorials/hello-app)
6. [Pushing and pulling images](https://cloud.google.com/container-registry/docs/pushing-and-pulling)
