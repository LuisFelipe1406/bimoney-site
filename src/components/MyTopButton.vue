<script setup lang="ts">
import { Icon } from '@iconify/vue';
import { ref } from 'vue';

const props = defineProps({
    buttonText: {
        type: String,
        required: true
    },
    buttonTextHover: {
        type: String,
        required: false
    },
    buttonIcon: {
        type: String,
        required: false
    }
});

const hover = ref(false);                // Controla classes ao dar hover no botão
const textButton = ref("Teste Agora");   // Texto do botão

// Altera o texto ao dar hover no botão
function hoverOn() {
    textButton.value = "É Grátis!";
    hover.value = true;
}

function hoverOff() {
    textButton.value = "Teste Agora";
    hover.value = false;
}

</script>

<template>
    <button @mouseenter="hoverOn" @mouseleave="hoverOff">
        <span :class="{ 'hovered': hover }" id="btnText">{{ textButton }}</span>
        <Icon icon="streamline:button-power-1-solid" :class="{ 'hovered': hover }" id="btnIcon" />
    </button>
</template>

<style scope>
button {
    width: 30vh;

    padding: 2vh;

    color: var(--our-white);
    background-color: var(--our-green);

    font-size: 20px;
    font-weight: 300;

    display: inline-flex;
    justify-content: center;
    align-items: center;

    border: 0px;
    border-radius: 5px;

    transition: background-color 0.5s ease;
}

button:hover {
    background-color: var(--our-dark-blue);
}

span {
    color: var(--our-white);

    cursor: pointer;

    display: inline-block;
    transition: transform 0.3s ease;
}

#btnText.hovered {
    transform: translateX(30px);
}

#btnIcon {
    margin-left: 2vh;

    transition: transform 0.3s ease;
}

#btnIcon.hovered {
    transform: translate(-100px);
}
</style>