<script>
import Navbar from './partials/NavBar.vue';
import EventDetails from './partials/EventDetails.vue';
import DressCode from './partials/DressCode.vue';
import OutfitInspiration from './partials/outfitInspiration.vue';
import Roses from './partials/18Roses.vue';
import BlueBills from './partials/18BlueBills.vue';
import Treasures from './partials/18Treasurers.vue';
import Candles from './partials/18Candles.vue';
import DebutantInfo from './partials/DebutantInfo.vue';
import RSVP from './partials/RSVP.vue';

export default {
    name: 'LandingPage',
    components: {
        Navbar,
        EventDetails,
        DressCode,
        OutfitInspiration,
        Roses,
        BlueBills,
        Candles,
        Treasures,
        DebutantInfo,
        RSVP,
    },
};
</script>

<template>
    <div id="app">
        <Navbar />
        <EventDetails />
        <DressCode />
        <OutfitInspiration />
        <Roses />
        <BlueBills />
        <Candles />
        <Treasures />
        <DebutantInfo />
        <RSVP />
    </div>
</template>

<style scoped>
@import '../assets/style.scss';


#app {
    padding-top: 60px;
}
</style>
