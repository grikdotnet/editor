<template>
  <div class="container">
    <header>
    <button class="hamburger" id="hamburger" @click="openStorage">&#9776;</button>
    <span>Text Editor</span>
    </header>
    <Storage :isOpen="isStorageOpen" @close-storage="closeStorage"/>
    <Editor/>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Storage from './components/Storage.vue';
import Editor from './components/Editor.vue';

  const isStorageOpen = ref(false);
  function openStorage() {
    isStorageOpen.value = true;
  }
  function closeStorage() {
    isStorageOpen.value = false;
  }
</script>

<style>
  header {
    display: flex;
    background-color: #e9e9e9;
    height: 30px;
    width: 100%;
   }
  .hamburger {
    background: none;
    border: none;
    font-size: 1.2rem;
    cursor: pointer;
    float: left;
  }
  header span {
    margin: 0 auto;
  }
  @media (min-width: 769px) {
    .hamburger {
      display: none;
    }
  }
  @media (max-width: 768px) {
    .hamburger {
      display: flex;
    }
  }
.container {
  display: flex;
  flex-direction: column;
  height: 100vh;
}
</style>