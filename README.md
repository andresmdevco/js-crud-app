# CRUD App 🗂️

Aplicación CRUD de usuarios construida con **Vite + Vanilla JS**. Permite listar, crear, editar y eliminar usuarios consumiendo una API REST local con `json-server`. 

## 🛠 Tecnologías

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)

## Funcionalidades

- Listar usuarios con paginación 
- Crear un nuevo usuario desde un modal
- Editar un usuario existente
- Eliminar un usuario

## ⚙️ Instalación y uso

### 1. Clonar el repositorio

```bash
git clone https://github.com/andresmdevco/js-crud-app.git
cd js-crud-app
```

### 2. Configurar variables de entorno

- Hacer una copia de `.env.template` y renombarala como `.env`

- Editar el `.env` y agrega la URL base del servidor. Por defecto json-server corre en:

````dotenv
VITE_BASE_URL=http://localhost:3001
````


### 3. Levantar el servidor (json-server)

```bash
npm run server
```

### 4. Iniciar la app

```bash
npm install
npm run dev
```

## Arquitectura

El proyecto está organizado en capas dentro de `src/users/`:

- **models** — clase `User` que define el modelo de datos
- **mappers** — transforman los datos entre el formato de la API y el modelo interno
- **use-cases** — lógica de negocio: cargar, guardar y eliminar usuarios
- **store** — estado global de la app (página actual, lista de usuarios)
- **presentation** — componentes de UI que renderizan la tabla, el modal y los botones

## 🧠 Conceptos practicados

- Arquitectura por capas (models, mappers, use-cases, store, presentation)
- Patrón mapper para desacoplar la API del modelo interno
- Estado global con módulo singleton
- CRUD completo con `fetch` (GET, POST, PATCH, DELETE)
- Manipulación dinámica del DOM
- Formularios con `FormData`
- Variables de entorno con Vite (`import.meta.env`)
