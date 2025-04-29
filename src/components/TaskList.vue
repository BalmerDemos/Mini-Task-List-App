<template>
  <div>
    <h2>Task List</h2>
    <ul>
      <li v-for="task in tasks" :key="task.id">
        <div class="task-main">
          <input
            type="checkbox"
            :checked="task.completed"
            @change="() => emit('toggle-complete', task.id)"
          />
          <span :style="{ textDecoration: task.completed ? 'line-through' : 'none' }">
            {{ task.text }}
          </span>
          <button @click="() => emit('delete-task', task.id)">❌ Delete</button>
        </div>
        <div class="task-meta">
          <small>🕓 Para: {{ task.dueDate || 'Not assigned' }}</small>
        </div>
      </li>
    </ul>
  </div>
</template>

<script setup>
const props = defineProps({
  tasks: Array
});

const emit = defineEmits(['delete-task', 'toggle-complete']);
</script>

<style scoped>
li {
  display: flex;
  flex-direction: column;
  padding: 0.5rem 0;
  border-bottom: 1px solid #ccc;
}
.task-main {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.task-meta {
  margin-left: 1.5rem;
  color: #666;
  font-size: 0.85rem;
}
button {
  margin-left: 1rem;
}
</style>
