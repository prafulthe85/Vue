<template>
  <ul>
    <li v-for="(task, index) in tasks" :key="index">
      {{ task }}
      <button @click="$emit('remove-task', index)">Remove</button>
    </li>
  </ul>
</template>

<script setup>
defineProps({
  tasks: {
    type: Array,
  },
});
defineEmits(["remove-task"]);
</script>
