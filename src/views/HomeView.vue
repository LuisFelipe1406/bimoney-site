<script setup lang="ts">
import MyHeader from "../components/MyHeader.vue";
</script>

<template>
  <MyHeader />
  <div id="divMain">
    <div id="divTopMain">
      <!-- <img src="/img/main.jpg" alt="image-top"> -->
    </div>
    <h1>Bem Vindo!</h1>
  </div>
</template>

<style scoped>
#divMain {
  position: relative;

  padding: 2vh;
}

#divTopMain {
  width: 100vw;
  height: 95vh;

  position: absolute;
  top: 0vh;
  left: 0vh;

  background-image: url("/img/main.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
</style>
