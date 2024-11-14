<script setup>
import { ref, computed, onMounted, watch } from 'vue'
import Greeting from './components/Greeting.vue'
import CreateTodo from './components/CreateTodo.vue'
import TodoList from './components/TodoList.vue'

const todos = ref([])
const name = ref('')

const todos_asc = computed(() => todos.value.sort((a, b) => a.createdAt - b.createdAt))

watch(name, (newVal) => {
  localStorage.setItem('name', newVal)
})

watch(todos, (newVal) => {
  localStorage.setItem('todos', JSON.stringify(newVal))
}, { deep: true })

const addTodo = (newTodo) => {
  todos.value.push(newTodo)
}

const removeTodo = (todo) => {
  todos.value = todos.value.filter((t) => t !== todo)
}

onMounted(() => {
  name.value = localStorage.getItem('name') || ''
  todos.value = JSON.parse(localStorage.getItem('todos')) || []
})
</script>

<template>
  <main class="app">
    <Greeting v-model:name="name" />
    <CreateTodo @add-todo="addTodo" />
    <TodoList :todos="todos_asc" @remove-todo="removeTodo" />
  </main>
</template>
