<script setup>
import { RouterView } from 'vue-router'

</script>

<template>
  <!-- <header>
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink :to="{name : 'todo'}">TodoList</RouterLink>
      </nav>
  </header> -->
    
  <!-- <main> -->
      <RouterView />
  <!-- </main> -->
</template>

<style scoped>

*{
  margin: 0;
  padding: 0;
}



</style>
