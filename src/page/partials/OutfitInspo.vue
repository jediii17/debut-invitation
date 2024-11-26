<template>
    <section id="outfit-inspiration" class="scroll-page outfit-inspiration">
        <div class="container-wrapper">
            <div class="container">
                <h2>Outfit Inspiration</h2>
                <p>Men Outfit:</p>
                <div class="images">
                    <img :src="outfitmen1" alt="Inspiration 1">
                    <img :src="outfitmen2" alt="Inspiration 2">
                    <img :src="outfitmen3" alt="Inspiration 3">
                </div>

                <p>Women Outfit:</p>
                <div class="images">
                    <img :src="outfitwomen5" alt="Inspiration 1">
                    <img :src="outfitwomen1" alt="Inspiration 2">
                    <img :src="outfitwomen4" alt="Inspiration 3">
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import outfitmen1 from '@/assets/img/outfitmen1.jpg';
import outfitmen2 from '@/assets/img/outfitmen2.jpg';
import outfitmen3 from '@/assets/img/outfitmen3.jpg';
import outfitwomen1 from '@/assets/img/outfitwomen1.jpg';
import outfitwomen2 from '@/assets/img/outfitwomen2.jpg';
import outfitwomen4 from '@/assets/img/outfitwomen4.jpg';
import outfitwomen5 from '@/assets/img/outfitwomen5.jpg';

export default {
    name: 'OutfitInspiration',
    data() {
        return {
            outfitmen1,
            outfitmen2,
            outfitmen3,
            outfitwomen1,
            outfitwomen2,
            outfitwomen4,
            outfitwomen5
        };
    },
};
</script>

<style lang="scss" scoped>
.outfit-inspiration {
    background: linear-gradient(135deg, #003366, #b30000, #000000);
    background-attachment: fixed;
    background-position: center;
    background-size: 100% 200%;
    padding: 60px 0;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #f2f1e1;
}

.container-wrapper {
    padding: 0;
}

.container {
    max-width: 999px;
    margin: 0 auto;
    background-color: rgba(0, 0, 0, 0.6);
    padding: 30px;
    border: 2px solid #d4a76f;
    border-radius: 15px;
    position: relative;
    z-index: 1;
    width: 100%;
    animation: glowing 1.5s infinite alternate;

    @media screen and (max-width: 768px) {
        max-width: 90%;
    }

    @media screen and (max-width: 480px) {
        max-width: 95%;
    }
}

@media screen and (max-width: 768px) {
    .container-wrapper {
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
        padding: 10px;
    }
}

h2 {
    font-family: 'Merriweather', serif;
    font-size: 2.4rem;
    color: #d4a76f;
    text-align: center;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
    margin-bottom: 20px;
}

p {
    font-family: 'Merriweather', serif;
    font-size: 1.8rem;
    color: #d4a76f;
}

.images {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 10px;
    margin-top: 20px;
    flex-wrap: wrap;
}

img {
    width: 300px;
    height: 500px;
    object-fit: cover;
    border: 2px solid #d4a76f;
    border-radius: 10px;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
    transition: transform 0.2s ease, box-shadow 0.3s ease;

    @media screen and (max-width: 768px) {
        width: 250px;
        height: 250px;
    }

    @media screen and (max-width: 680px) {
        width: 200px;
        height: 300px;
    }

    @media screen and (max-width: 480px) {
        width: 300px;
        height: 500px;
    }
}

img:hover {
    transform: scale(1.05);
    box-shadow: 0 0 15px 5px rgba(212, 167, 111, 0.8);
}
</style>
