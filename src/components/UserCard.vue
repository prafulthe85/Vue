<script setup>
defineProps({
  name: String,
  age: Number,
});
</script>

<template>
  <h1>{{ name }} - {{ age }}</h1>
</template>
