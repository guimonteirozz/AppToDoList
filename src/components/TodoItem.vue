<script setup>
  import { defineProps, defineEmits } from 'vue'
  
  const props = defineProps(['todo'])
  const emit = defineEmits(['remove-todo'])
</script>
  
<template>
    <div :class="`todo-item ${todo.done && 'done'}`">
      <label>
        <input type="checkbox" v-model="todo.done" />
        <span :class="`bubble ${todo.category === 'business' ? 'business' : 'personal'}`"></span>
      </label>
  
      <div class="todo-content">
        <input type="text" v-model="todo.content" />
      </div>
  
      <div class="actions">
        <button class="delete" @click="$emit('remove-todo', todo)">
          <span class="material-symbols-outlined">delete</span>
        </button>
      </div>
    </div>
</template>
