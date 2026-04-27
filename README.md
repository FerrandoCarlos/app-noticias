# 📰 Portal de Noticias

Aplicación web CRUD desarrollada con Node.js y PostgreSQL.

## 🛠 Tecnologías

- Node.js
- Express
- PostgreSQL
- PUG
- Tailwind CSS
- Zod
- Ajax

## 📋 Requisitos previos

- Node.js instalado
- Laragon con PostgreSQL corriendo
- HeidiSQL o psql para gestionar la base de datos

## 🚀 Instalación

1. Clonar el repositorio

```bash
git clone https://github.com/FerrandoCarlos/app-noticias.git
cd portal-noticias
```

2. Instalar dependencias

```bash
npm install
```

3. Crear el archivo `.env` en la raíz
   - PORT=3000
   - DB_HOST=localhost
   - DB_PORT=5432
   - DB_USER=postgres
   - DB_PASSWORD=
   - DB_NAME=noticias

4. Iniciar el servidor

```bash
npm run dev
```

5. Abrir en el navegador
   - http://localhost:3000

## 📁 Estructura del proyecto

```
📁 portal-noticias/
├── 📁 controllers/
├── 📁 db/
├── 📁 models/
├── 📁 public/
│   ├── 📁 css/
│   └── 📁 js/
├── 📁 router/
├── 📁 schemas/
├── 📁 views/
├── .env
├── .gitignore
├── app.js
└── package.json
```

## 🔗 Rutas

| Método | Ruta               | Descripción              |
| ------ | ------------------ | ------------------------ |
| GET    | /noticias          | Lista todas las noticias |
| GET    | /noticias/insertar | Formulario para agregar  |
| POST   | /noticias/agregar  | Guarda una nueva noticia |
| POST   | /noticias/borrar   | Elimina una noticia      |

## 🗄 Base de datos

### Tabla `categorias`

| Campo  | Tipo        | Descripción            |
| ------ | ----------- | ---------------------- |
| id     | SERIAL      | Clave primaria         |
| nombre | VARCHAR(50) | Nombre de la categoría |

### Tabla `noticias`

| Campo        | Tipo         | Descripción             |
| ------------ | ------------ | ----------------------- |
| id           | SERIAL       | Clave primaria          |
| titulo       | VARCHAR(150) | Título de la noticia    |
| descripcion  | TEXT         | Contenido de la noticia |
| categoria_id | INTEGER      | Referencia a categorias |
| fecha        | DATE         | Fecha de publicación    |
| url_imagen   | TEXT         | URL de la imagen        |
