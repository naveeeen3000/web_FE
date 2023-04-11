<script setup>
import NavBar from './components/NavBar.vue';
import { RouterView } from 'vue-router';
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <NavBar />
      </nav>
      
    </div>
  </header>
  <div>
    <RouterView />
  </div>

</template>
