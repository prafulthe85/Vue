<template>
  <div class="" input-box>
    <input
      v-model="task"
      ref="taskInput"
      type="text"
      placeholder="Enter task"
    />
    <button @click="handleAdd">Add</button>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";

const emit = defineEmits(["add-task"]);
const task = ref("");
const taskInput = ref(null);
onMounted(() => {
  taskInput.value.focus();
});
const handleAdd = () => {
  if (!task.value.trim()) return;
  emit("add-task", task.value);
  task.value = "";
  taskInput.value.focus();
};
</script>
