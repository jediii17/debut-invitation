<script>
import LandingPage from './page/LandingPage.vue';

export default {
    components: {
        LandingPage,
    },
    data() {
        return {
            isLoading: true,
            letters: [..."Nicolai @18"],
        };
    },
    mounted() {
        setTimeout(() => {
            this.isLoading = false;
        }, this.letters.length * 200 + 1000);
    },
};
</script>

<template>
    <div id="app">
        <!-- Loading Screen -->
        <transition name="fade">
            <div v-if="isLoading" id="loading-screen">
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
        </transition>

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

.fade-enter-active,
.fade-leave-active {
    transition: opacity 1s ease;
}

.fade-enter,
.fade-leave-to {
    opacity: 0;
}

.page-transition-enter-active,
.page-transition-leave-active {
    transition: opacity 1s ease, transform 1s ease;
}

.page-transition-enter,
.page-transition-leave-to {
    opacity: 0;
    transform: translateY(20px);
}
</style>
