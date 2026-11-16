
# Proyecto Reserva Médica Salud - DevOps

## Descripción

Proyecto de implementación de un servicio web estático
que simula una plataforma de reserva de horas médicas.

El sitio web utiliza HTML5 y CSS3, y se ejecuta
mediante un servidor Nginx dentro de un contenedor Docker.

El proyecto permite demostrar prácticas de control de
versiones, configuración reproducible y ejecución local.

## Objetivo

Implementar un entorno local reproducible para una
aplicación web de reserva de horas médicas, utilizando
Git, GitHub, Docker Desktop y Docker Compose.

## Tecnologías utilizadas

- HTML5
- CSS3
- Git
- GitHub
- Docker Desktop
- Docker Compose
- Nginx Alpine
- Visual Studio Code

## Estructura del proyecto

ProyectoReservaMedicaSalud-devops/
- src/
  - index.html
  - styles.css
- Dockerfile
- docker-compose.yml
- .gitignore
- .env.example
- README.md

## Requisitos técnicos

Para ejecutar el proyecto se necesita:

- Docker Desktop instalado y funcionando.
- Docker Compose disponible.
- Un navegador web.
- Git para el control de versiones.
- Visual Studio Code u otro editor de código.

## Instalación

1. Clonar el repositorio:

   git clone https://github.com/Hecontra/ProyectoReservaMedicaSalud-devops.git

2. Ingresar a la carpeta del proyecto:

   cd ProyectoReservaMedicaSalud-devops

3. Abrir Docker Desktop.

4. Verificar que Docker esté funcionando:

   docker --version
   docker compose version

## Construcción y ejecución

Desde la carpeta principal del proyecto, ejecutar:

    docker compose up -d --build

Docker Compose construirá la imagen basada en
nginx:alpine e iniciará el servicio web.

## Acceso a la aplicación

Abrir un navegador e ingresar a:

http://localhost:8080

La página deberá mostrar:

- Formulario simulado de reserva médica.
- Selección de especialidad, fecha y horario.
- Información general de atención.
- Estado demostrativo del servicio.

La aplicación no registra reservas reales.

## Verificación del contenedor

Consultar el estado del servicio:

    docker compose ps

Consultar los contenedores activos:

    docker ps

Revisar los registros del servicio:

    docker logs reservas-medicas-web

Consultar métricas de consumo de recursos:

    docker stats --no-stream reservas-medicas-web

## Detención del servicio

Para detener y eliminar el contenedor del proyecto:

    docker compose down

## Configuración

El archivo Dockerfile utiliza la imagen nginx:alpine.

Docker Compose publica el puerto 80 del contenedor
mediante el puerto 8080 del computador local.

El archivo .env.example contiene variables ilustrativas
de configuración y no incluye credenciales.

Actualmente, estas variables son documentales y
no son utilizadas directamente por Docker Compose.

## Seguridad

El proyecto utiliza buenas prácticas básicas:

- No publicar contraseñas ni tokens.
- No incorporar credenciales reales.
- Utilizar .gitignore para excluir archivos privados.
- Mantener .env.example sin información sensible.
- No almacenar datos personales de pacientes.
- Revisar los cambios antes de publicarlos en GitHub.

## Limitaciones

La aplicación es una simulación académica.

No utiliza base de datos, API ni servicios externos.

El formulario no procesa ni almacena reservas reales.

El indicador de estado es informativo y no representa
un monitoreo automático del servicio.

## Control de versiones

El proyecto utiliza Git y GitHub para registrar cambios
mediante commits, administrar ramas de desarrollo y
realizar integraciones mediante pull requests.

La rama main representa la versión principal del proyecto.

