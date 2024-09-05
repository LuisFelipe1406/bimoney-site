<script setup lang="ts">
import MyHeader from "../components/MyHeader.vue";
import MyTopButton from "../components/MyTopButton.vue";
</script>

<template>
  <MyHeader />
  <div id="divMain">
    <div id="divTopMain">
      <div id="divTopShape"> </div>
      <div id="divTopInfo">
        <img src="/img/logo.png" alt="logo-top">
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit.
          Sed egestas ante at nisl varius, quis lobortis orci faucibus.
          Duis commodo viverra lectus et euismod. Pellentesque ac
          hendrerit nisl. Nullam non elit nec.
        </p>
        <MyTopButton />
      </div>
      <div id="divTopVideo">
        <h3>Confira nosso <span class="hDestaque">video de apresentação</span></h3>
      </div>
    </div>
    <div id="divProduct">

    </div>
  </div>
</template>

<style scoped>
#divMain {}

#divTopMain {
  width: 100vw;
  height: 95vh;

  background-image: url("/img/main.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;

  display: grid;
  grid-template-columns: repeat(2, 1fr);
  justify-content: center;
  align-items: center;
}

#divTopShape {
  width: 60%;
  height: 95vh;

  position: absolute;

  background-color: var(--our-white);

  clip-path: polygon(0 0, 100% 0, 70% 100%, 0% 100%);
}

#divTopInfo {
  z-index: 1;

  padding: 10% 25% 10% 25%;

  display: grid;
  grid-template-rows: 1fr;
  row-gap: 3vh;
  justify-content: center;
  align-items: center;

  img {
    max-width: 30vh;
  }

  p {
    width: 28vh;

    margin-bottom: 5vh;

    text-align: left;
    font-size: 20px;
  }
}

#divTopVideo {
  display: grid;
  grid-template-rows: repeat(2, max-content);
  row-gap: 3vh;

  h3 {
    color: var(--our-white);

    font-weight: 300;
  }
}

#divProduct {
  width: 100vw;
  height: 95vh;

  background-color: var(--our-dark-blue)
}
</style>
