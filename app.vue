<template>
    <div class="wrapper">
        <h1>{{ message }}</h1>
        <input type="text" v-model="text" placeholder="Enter lastname">
        <CharacterName firstName="Hermione" v-bind:lastName="text"  />
    </div>
</template>

<script>
import CharacterName from './character-name';

export default {
    components: {
        CharacterName
    },
    data: () => {
        return {
            message: "Stop, stop stop! You're going to take someone's eye out. Besides, you're saying it wrong." +
        " It's Levi-o-sa, not Levio-sar.",
            text: '' 
        }
    }
}
</script>

<style>
    body {
        width: 100vw;
        height: 100vh;
        background: #FAF5EB;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .wrapper {
        max-width: 1000px;
        display: flex;
        flex-direction: column;
    }

    h1 {
        color: #692D55;
    }
</style>