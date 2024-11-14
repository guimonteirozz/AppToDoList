<script setup>
import TodoItem from './TodoItem.vue'
import { defineProps, defineEmits } from 'vue'

const props = defineProps(['todos'])
const emit = defineEmits(['remove-todo'])
</script>

<template>
    <section class="todo-list">
      <h3>LISTA DE TAREFAS</h3>
      <div class="list">
        <TodoItem v-for="todo in todos" :key="todo.createdAt" :todo="todo" @remove-todo="$emit('remove-todo', todo)" />
      </div>
    </section>
</template>
  