<script setup>
import Tarefa from './Tarefa.vue';

defineProps({
  tarefas: {
    type: Array,
    required: true
  }
})
</script>

<template>
  <table>
    <tbody>
      <Tarefa v-for="tarefa in tarefas" :tarefa="tarefa"/>
    </tbody>
  </table>

</template>