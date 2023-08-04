<script setup>
import {ref} from 'vue';
import Tabela from './components/Tabela.vue';
import Form from './components/Form.vue';

const tarefas = ref([]);

const adicionarTarefa = (tarefa) => {
  console.log(tarefa);
  tarefas.value.push(tarefa);
}

tarefas.value = ["Fazer Bolo", "Fazer compra", "Dormir muito"];
</script>

<template>
  <h1>Coisas a fazer E não procrastinar!</h1>
  <Form @nova="adicionarTarefa"/>
  <Tabela :tarefas="tarefas" />
</template>

<style scoped>

</style>
