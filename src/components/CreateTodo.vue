<script setup>
  import { ref } from 'vue'
  import { defineEmits } from 'vue'
  
  const emit = defineEmits(['add-todo'])
  const inputContent = ref('')
  const inputCategory = ref(null)
  
  const submitTodo = () => {
    if (inputContent.value.trim() === '' || !inputCategory.value) {
      alert('Digite o nome da tarefa')
      return
    }
  
    const newTodo = {
      content: inputContent.value,
      category: inputCategory.value,
      done: false,
      editable: false,
      createdAt: new Date().getTime()
    }
  
    emit('add-todo', newTodo)
  
    inputContent.value = ''
    inputCategory.value = null
  }
</script>
  

<template>
    <section class="create-todo">
      <h3>CRIAR TAREFA</h3>
      <form @submit.prevent="submitTodo">
        <h4>Qual o nome da tarefa?</h4>
        <input type="text" placeholder="Nome da tarefa" v-model="inputContent" />
  
        <h4>Escolha a Categoria</h4>
        <div class="options">
          <label>
            <input type="radio" value="business" v-model="inputCategory" />
            <span class="bubble business"></span>
            <div>Negócios</div>
          </label>
  
          <label>
            <input type="radio" value="personal" v-model="inputCategory" />
            <span class="bubble personal"></span>
            <div>Pessoal</div>
          </label>
        </div>
  
        <input type="submit" value="Adicionar tarefa" />
      </form>
    </section>
</template>
