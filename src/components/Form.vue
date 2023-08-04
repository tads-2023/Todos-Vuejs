<script setup>
import {ref} from 'vue';

const tarefa = ref('');
const emit = defineEmits(["nova"])
const clickHandler = () => {
  emit('nova', tarefa.value);
}
</script>

<template>
  <form>
    <input v-model="tarefa" type="text" name="Todo">
    <button @click.prevent="clickHandler">Salvar</button>
  </form>

</template>