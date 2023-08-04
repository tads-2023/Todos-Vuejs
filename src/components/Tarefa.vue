<script setup>
defineProps({
  tarefa: {
    type: String,
    required: true
  }
})
</script>

<template>
  <tr>
    <td>{{ tarefa }}</td>
    <td><button>Feito!</button></td>
    <td><button>Remover</button></td>
  </tr>
</template>