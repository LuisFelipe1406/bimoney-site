<script setup lang="ts">
import MyHeader from "../components/MyHeader.vue";
</script>

<template>
  <MyHeader />
  <div id="divMain">
    <h1>Bem Vindo!</h1>
  </div>
</template>

<style scoped>
#divMain {
  position: relative;
  height: 200vh;

  top: 10vh;

  padding: 2vh;
}
</style>
