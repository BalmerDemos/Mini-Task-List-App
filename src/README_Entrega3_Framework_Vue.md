# Entrega 3 - Framework Vue.js

## 📚 Descripción
Este proyecto corresponde a la Entrega 3 del curso de **Estructuras y Algoritmos Web**.
Se desarrolla una mini aplicación en **Vue.js 3** utilizando el framework moderno para construir una lista de tareas.

## 🛠 Tecnologías utilizadas
- Vue.js 3 (Composition API)
- Vite (framework de construcción rápido)
- Node.js y npm
- Visual Studio Code

## 📁 Estructura del proyecto
```
entrega3-framework-vue/
├── public/
│   └── index.html - we moved to the correct location...
├── src/
│   ├── components/
│   │   ├── TaskForm.vue
│   │   └── TaskList.vue
│   ├── App.vue
│   └── main.js
├── package.json
├── vite.config.js
└── README.md
```

## 🚀 Instalación y ejecución

### 1. Requisitos previos
- Tener instalado **Node.js** (versión 18 o superior).
- Tener instalado **npm**.

### 2. Instalación del proyecto
Desde la terminal, ubicado en la carpeta raíz del proyecto:
```bash
npm install
```

### 3. Ejecución del proyecto
Para iniciar el servidor de desarrollo:
```bash
npm run dev
```

Esto abrirá la aplicación en:
[http://localhost:5173](http://localhost:5173)

## 📄 Funcionalidades
- **Agregar Tareas:** Permite ingresar nuevas tareas a la lista.
- **Listar Tareas:** Muestra todas las tareas ingresadas.
- **Completar Tareas:** Permite marcar tareas como completadas.
- **Eliminar Tareas:** Permite borrar tareas de la lista.

## 🧩 Componentes Vue utilizados
- **TaskForm.vue:** Formulario para agregar tareas nuevas.
- **TaskList.vue:** Lista de tareas con opciones de completar o eliminar.

## 📷 Vista previa esperada
- Formulario de entrada de tareas.
- Lista dinámica de tareas actualizada en tiempo real.

## 📌 Notas
- Los datos se almacenan temporalmente en memoria durante la sesión.
- La aplicación puede ser extendida para persistencia utilizando bases de datos o almacenamiento local.

---

Desarrollado para fines académicos.
