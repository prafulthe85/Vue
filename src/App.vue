<script setup>
import { ref } from "vue";
// const count = ref(0);
// const name = ref("");
const toShow = ref(true);

// const users = [
//   { id: 1, name: "Praful" },
//   { id: 2, name: "Rahul" },
//   { id: 3, name: "Charlie" },
// ];
</script>
<template>
  <!-- <input v-model="name" />
  <button @click="count++">Count: {{ count }}</button>
  <h1>Hello {{ name }}</h1> -->
  <!-- <div v-for="user in users" :key="user.id">
    <h2>{{ user.name }}</h2>
  </div> -->
  <button @click="toShow = !toShow">Toggle</button>

  <h1 v-if="toShow">Visible</h1>
  <h1 v-else>Not Visible</h1>
</template>

<style>
h1 {
  color: blue;
}
</style>
