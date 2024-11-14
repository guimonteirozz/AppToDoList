<script setup>
const props = defineProps(['modelValue'])
const emit = defineEmits(['update:modelValue'])

const name = computed({
  get: () => props.modelValue,
  set: (value) => emit('update:modelValue', value)
})
</script>

<template>
    <section class="greeting">
      <h2 class="title">
        Essa lista pertence a: <input type="text" id="name" placeholder="Nome aqui" v-model="name" />
      </h2>
    </section>
</template>

  