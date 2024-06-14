<script setup>
import { ref } from 'vue'

</script>
<template>
<main class="content">

</main>
</template>

<style scoped>
.content {
  flex-grow: 1;
  padding: 1rem;
  overflow-y: auto;
}

.input-box {
  display: flex;
  padding: 1rem;
  background-color: #f1f1f1;
}

.input-box input {
  flex-grow: 1;
  padding: 0.5rem;
  border: 1px solid #ccc;
  border-radius: 20px;
  margin-right: 0.5rem;
}

.input-box button {
  padding: 0.5rem 1rem;
  border: none;
  background-color: #333;
  color: white;
  border-radius: 20px;
  cursor: pointer;
}

</style>