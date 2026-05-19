<script setup>
import { ref, computed } from "vue";
// import TaskInput from "./components/TaskInput.vue";
// import TaskList from "./components/TaskList.vue";
// import Navbar from "./components/Navbar.vue";
import UserCard from "./components/UserCard.vue";
// const count = ref(0);
// const increment = () => {
//   count.value++;
// };
// const name = ref("");
// const toShow = ref(true);

// const users = [
//   { id: 1, name: "Praful" },
//   { id: 2, name: "Rahul" },
//   { id: 3, name: "Charlie" },
// ];

// const tasks = ref([]);
// const addTask = (task) => {
//   tasks.value.push(task);
// };

// const removeTask = (index) => {
//   tasks.value.splice(index, 1);
// };
const firstname = ref("Praful");
const lastname = ref("Shinde");

const fullname = computed(() => {
  return `${firstname.value} ${lastname.value}`;
});
</script>
<template>
  <!-- <input v-model="name" />
  <button @click="count++">Count: {{ count }}</button>
  <h1>Hello {{ name }}</h1> -->
  <!-- <div v-for="user in users" :key="user.id">
    <h2>{{ user.name }}</h2>
  </div> -->
  <!-- <button @click="toShow = !toShow">Toggle</button>
  <button @click="increment">Count : {{ count }}</button>

  <h1 v-if="toShow">Visible</h1>
  <h1 v-else>Not Visible</h1> -->
  <!-- <Navbar /> -->

  <!-- <div class="app">
    <h1>Todo App</h1>
    <TaskInput @add-task="addTask" />
    <p>Total tasks: {{ tasks.length }}</p>

    <TaskList :tasks="tasks" @remove-task="removeTask" />
  </div> -->
  <!-- <UserCard name="Praful" age="24" /> -->
  <UserCard :name="fullname" age="24" />
</template>

<style>
h1 {
  color: blue;
}
</style>
