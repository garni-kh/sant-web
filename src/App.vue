<script setup>
import { RouterView } from 'vue-router'
import MenuHeder from './components/MenuHeder.vue'
import MenuFooter from './components/MenuFooter.vue'
</script>

<template>
  <header>
    <MenuHeder />
  </header>

  <RouterView />

  <footer class="bg-primary-500">
    <MenuFooter />
  </footer>
</template>
