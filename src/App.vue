<template>
  <div style="padding: 20px;">
    <header class="banner">
      <img src="/BalmerDemosV2.png" alt="Banner de Lista de Tareas" />
    </header>
    <h1>Mini Task List App</h1>
    <TaskForm @add-task="addTask" />
    <TaskList :tasks="tasks" @delete-task="deleteTask" @toggle-complete="toggleComplete" />

    <!-- Footer -->
    <footer class="footer">
      <div class="footer-content">
        <p>Desarrollado por <strong>Balmer Valencia</strong></p>
        <div class="social-links">
          <a href="https://github.com/BalmerDemos" target="_blank" rel="noopener noreferrer">GitHub</a>
          <a href="https://www.linkedin.com/in/balmer-valencia-988a42273" target="_blank" rel="noopener noreferrer">LinkedIn</a>
          <a href="https://balmerdemos.pythonanywhere.com" target="_blank" rel="noopener noreferrer">Sitio Web</a>
        </div>
        <p>&copy; 2023 Balmer Valencia. Todos los derechos reservados.</p>
        <p>Este proyecto es un ejemplo de una aplicación de lista de tareas simple utilizando Vue 3.</p>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import TaskForm from './components/TaskForm.vue';
import TaskList from './components/TaskList.vue';

const tasks = ref([]);

const addTask = (newTask) => {
  tasks.value.push({
    id: Date.now(),
    text: newTask.text,
    createdAt: newTask.createdAt,
    dueDate: newTask.dueDate,
    completed: newTask.completed,
  });
};


const deleteTask = (id) => {
  tasks.value = tasks.value.filter(task => task.id !== id);
};

const toggleComplete = (id) => {
  const task = tasks.value.find(task => task.id === id);
  if (task) task.completed = !task.completed;
};
</script>

<style scoped>
.app-container {
  max-width: 90%;
  margin: auto;
  padding: 2rem;
  font-family: Arial, sans-serif;
}

.banner {
  display: flex;
  justify-content: center;
  margin-bottom: 1rem;
}

.banner img {
  max-width: 200px;
  width: 100%;
  height: auto;
  border-radius: 8px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

body {
  background: linear-gradient(to bottom, #f0f4ff, #ffffff);
  color: #333;
  padding: 1rem;
}

footer {
  margin-top: 2rem;
  padding: 1rem 0;
  text-align: center;
  background-color: #2a5298; /* Same color as your logo for consistency */
  color: white;
}

footer a {
  color: white;
  text-decoration: none;
  margin: 0 10px;
}

footer a:hover {
  text-decoration: underline;
}

footer .social-links {
  margin-top: 0.5rem;
}

footer .social-links a {
  margin: 0 15px;
}

@media (max-width: 600px) {
  .banner img {
    max-width: 150px;
  }
}
</style>
