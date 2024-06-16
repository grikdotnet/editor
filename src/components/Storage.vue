<template>
  <nav :class="{ storage: true, open: isOpen }">
    <div class="storage-header">
      <h2>Storage</h2>
      <button class="close-btn" @click="closeStorage">&times;</button>
    </div>
    <ul>
      <li><a href="#">File 1</a></li>
    </ul>
  </nav>
</template>

<script setup>
  const props = defineProps({isOpen: Boolean})
  const emit = defineEmits(['close-storage'])
  function closeStorage() {
    emit('close-storage');
  }
</script>

<style scoped>
.storage {
  height: 100%;
  background-color: #333;
  color: white;
  width: 300px;
  transition: transform 0.3s ease;
}
.storage-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
}
.storage ul {
  list-style-type: none;
  padding: 0;
}
.storage ul li {
  padding: 1rem;
}
.storage ul li a {
  color: white;
  text-decoration: none;
}
@media (max-width: 768px) {
  .storage {
    display: none;
  }
  .storage.open {
    display: block;
  }
  .close-btn {
    display: block;
    background: none;
    border: none;
    font-size: 1.5rem;
    color: white;
    cursor: pointer;
  }
}
@media (min-width: 769px) {
  .close-btn {
    display: none;
  }
}

</style>