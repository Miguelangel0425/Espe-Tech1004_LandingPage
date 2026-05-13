# Landing Page — ESPE TECH 1004

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)

Despliegue de una Landing Page estática para el evento institucional utilizando **Docker** y **Nginx**, desarrollado como parte de las actividades de Ingeniería de Software de la ESPE.

---

## Descripción del Proyecto

Este proyecto presenta la página web oficial para el evento **ESPE TECH 1004**. El sitio está construido con HTML estático y empaquetado en un contenedor Docker utilizando **Nginx** como servidor web de alto rendimiento. Esta arquitectura permite que el sitio sea portable, escalable y fácil de desplegar en cualquier servidor local o en la nube.

---

## Estructura de Carpetas

```text
Espe-Tech1004_LandingPage/
├── assets/             # Recursos visuales (imágenes, logos del evento)
├── css/                # Estilos y diseño responsivo
├── index.html          # Estructura principal de la Landing Page
├── Dockerfile          # Instrucciones para la construcción de la imagen
├── .dockerignore       # Archivos excluidos del contenedor
└── README.md           # Documentación técnica
```

---

## Instrucciones de Uso con Docker

### 1. Construir la imagen

Clona el repositorio y construye la imagen localmente:

```bash
git clone https://github.com/Miguelangel0425/Espe-Tech1004_LandingPage.git
cd Espe-Tech1004_LandingPage
docker build -t gamanosalvas/espe-tech-1004:latest .
```

### 2. Ejecutar el contenedor

Inicia el contenedor mapeando el puerto 80 del servidor interno al puerto 8080 de tu máquina host:

```bash
docker run -d -p 8080:80 --name landing-espe-1004 gamanosalvas/espe-tech-1004:latest
```

### 3. Acceder al sitio

Abre tu navegador y visualiza el proyecto en:

```
http://localhost:8080
```

---

## Imagen en Docker Hub

La imagen está disponible para su descarga directa desde Docker Hub:

🔗 **URL:** `https://hub.docker.com/r/gamanosalvas/espe-tech-1004`

### Descargar la imagen

```bash
docker pull gamanosalvas/espe-tech-1004:latest
```

### Ejecutar directamente desde Docker Hub

Sin necesidad de clonar el repositorio, puedes ejecutar el contenedor directamente:

```bash
docker run -d -p 8080:80 --name landing-espe-1004 gamanosalvas/espe-tech-1004:latest
```

Luego accede en tu navegador a: **http://localhost:8080**

---

## Tecnologías Utilizadas

| Tecnología | Uso |
|---|---|
| ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white) HTML5 | Maquetación y contenido del evento |
| ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) Docker | Contenerización para despliegue consistente |
| ![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white) Nginx Alpine | Servidor web ligero y optimizado |
