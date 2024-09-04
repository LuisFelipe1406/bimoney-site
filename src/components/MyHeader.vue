<script setup lang="ts">
import { onMounted } from "vue";

onMounted(() => {
    // Muda o header ao scrollar
    var header = document.getElementById("divHeader");

    window.onscroll = function () {
        if (document.body.scrollTop > 75 || document.documentElement.scrollTop > 75) {
            header.classList.add("scrolled");
        } else {
            header.classList.remove("scrolled");
        }
    };
});

// Joga o usuário para o topo da tela
function scrollTop() {
    window.scrollTo({ top: 0, behavior: 'smooth' });
}

</script>

<template>
    <div id="divHeader">
        <img src="/img/logo-horizontal.png" alt="logo-horizontal" id="imgLogo" @click="scrollTop">
    </div>
</template>

<style scoped>
#divHeader {
    position: fixed;
    width: 100%;
    height: 8vh;

    padding: 0vh 14vh 0vh 14vh;

    z-index: 2;

    display: grid;
    justify-content: center;
    align-items: center;

    transition: background-color 0.3s ease;
}

/* Header Aparece no scroll */
#divHeader.scrolled {
    background-color: var(--our-white);
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);

    #imgLogo {
        display: grid;
    }
}

#imgLogo {
    max-height: 6vh;

    display: none;

    cursor: pointer;

    transition: transform 0.3s ease;
}

#imgLogo:hover {
    transform: scale(1.1);
}
</style>