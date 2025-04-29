<template>
  <form @submit.prevent="handleSubmit">
    <input
      type="text"
      v-model="taskText"
      placeholder="New task"
    />
    <input
      type="date"
      v-model="dueDate"
      :min="today"
      title="Due date"
    />
    <button type="submit">Add Task</button>
  </form>
</template>

<script setup>
import { ref } from 'vue';

const emit = defineEmits(['add-task']);
const taskText = ref('');
const dueDate = ref('');

const handleSubmit = () => {
  if (taskText.value.trim()) {
    const task = {
      text: taskText.value,
      dueDate: dueDate.value,
      completed: false,
      id: Date.now(),
    };
    emit('add-task', task);
    taskText.value = '';
  }
};
</script>

<style scoped>
form {
  display: flex;
  gap: 0.5rem;
  margin-bottom: 1rem;
}
input {
  flex: 1;
  padding: 0.5rem;
}
button {
  padding: 0.5rem 1rem;
}
</style>