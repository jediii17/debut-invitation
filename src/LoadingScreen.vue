<script>
import LandingPage from './page/LandingPage.vue';

export default {
    components: {
        LandingPage,
    },
    data() {
        return {
            isLoading: true,
            letters: [..."Nicolai @18"], // Split string into an array of letters
        };
    },
    mounted() {
        // Simulate a loading process or replace with actual logic
        setTimeout(() => {
            this.isLoading = false;
        }, this.letters.length * 200 + 1000); // Adjust to fade all letters plus a slight delay
    },
};
</script>


<template>
    <div id="loading-screen" v-if="isLoading">
        <div class="text-container">
            <span v-for="(letter, index) in letters" :key="index" class="letter"
                :style="{ animationDelay: `${index * 0.2}s` }">
                {{ letter }}
            </span>
        </div>
    </div>
    <div v-else>
        <LandingPage />
    </div>
</template>


<style scoped>
#loading-screen {
    background-color: #000000;
    height: 100vh;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    position: fixed;
    top: 0;
    left: 0;
    z-index: 9999;
    overflow: hidden;
    transition: opacity 1s ease-in-out;
}

.text-container {
    display: flex;
    gap: 5px;
}

.letter {
    font-family: "Pinyon Script", serif;
    font-size: 2.4rem;
    font-weight: bold;
    color: #b30000;
    opacity: 0;
    animation: flash 1s ease forwards;
}

@keyframes flash {
    0% {
        opacity: 0;
        transform: translateY(20px);
    }

    100% {
        opacity: 1;
        transform: translateY(0);
    }
}
</style>
