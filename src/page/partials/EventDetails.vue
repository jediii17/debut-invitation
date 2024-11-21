<template>
    <section id="event-details" class="scroll-page event-details">
        <div class="content-container">
            <div class="text-content">
                <span>Nicolai @18</span>
                <div class="event-info">
                    <p class="date">FRI | 13 | DEC</p>
                    <p class="msg">6 o'clock in the evening at Sunlane Resort</p>
                    <p class="address" @click="openMap">
                        Brgy. Pansol, Calamba City, Laguna
                    </p>
                    <p><strong>Theme:</strong> Old Money</p>
                    <div class="btn-group">
                        <a @click.prevent="scrollToSection('rsvp')" class="btn">RSVP</a>
                        <a @click="openMap" class="btn right-btn"> Location</a>
                    </div>

                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'EventDetails',
    methods: {
        openMap() {
            window.open(
                'https://www.google.com.ph/maps/place/SunLane+Resort/@14.1810796,121.1838738,18z/data=!4m14!1m7!3m6!1s0x33bd618ebf32c30f:0x74dd7b3fb0448037!2sSunLane+Resort!8m2!3d14.1810796!4d121.1851613!16s%2Fg%2F11y5p2t5st!3m5!1s0x33bd618ebf32c30f:0x74dd7b3fb0448037!8m2!3d14.1810796!4d121.1851613!16s%2Fg%2F11y5p2t5st?entry=ttu&g_ep=EgoyMDI0MTExNy4wIKXMDSoASAFQAw%3D%3D',
                '_blank'
            );
        },
        scrollToSection(sectionId) {
            const section = document.getElementById(sectionId);
            if (section) {
                section.scrollIntoView({ behavior: 'smooth' });
            }
        },
    },
};
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Great+Vibes&family=Pinyon+Script&display=swap');

#event-details {
    margin: 0;
    padding: 0;
    background-image: url('@/assets/img/banner.png');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-position: center;

    .content-container {
        max-width: 1200px;
        width: 100%;
        margin-top: 25px;
        display: flex;
        justify-content: flex-end;
        align-items: center;
        color: #f2f1e1;

        .text-content {
            background: rgba(0, 0, 0, 0.65);
            padding: 60px 40px;
            width: 50%;
            margin-left: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.15);
            border: 1px solid #d4a76f;

            .date {
                font-family: 'Georgia', serif;
                font-size: 1.5rem;
                text-align: center;
                font-weight: bold;

                @media screen and (max-width: 768px) {
                    font-size: 6vw;
                }

                @media screen and (max-width: 480px) {
                    font-size: 5vw;
                }
            }

            span {
                font-family: "Pinyon Script", serif;
                font-size: 8rem;
                margin-bottom: 1px;
                text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.4);
                background: linear-gradient(90deg, #ff0000, #e8d0c8, #c6b5b2, #dcd4d1, #d65f34, #ff0000);
                background-size: 400%;
                -webkit-background-clip: text;
                -moz-background-clip: text;
                background-clip: text;
                -webkit-text-fill-color: transparent;
                -moz-text-fill-color: transparent;
                animation: shiny 20s linear infinite;
                padding: 0 12px;
                display: inline-block;
                text-align: center;

                @keyframes shiny {
                    0% {
                        background-position: 400% 0;
                    }

                    100% {
                        background-position: -400% 0;
                    }
                }

                @media screen and (max-width: 768px) {
                    font-size: 15vw;
                    display: block;
                    text-align: center;
                    margin: 0 auto;
                }

                @media screen and (max-width: 480px) {
                    font-size: 17vw;
                    display: block;
                    text-align: center;
                    margin: 0 auto;

                }
            }


            .event-info {
                font-family: 'Merriweather', serif;
                font-size: 1.6rem;
                line-height: 2;
                color: #f4f1e1;
                text-align: center;

                p {
                    margin-bottom: 15px;
                    text-align: center;
                }

                strong {
                    color: #d4a76f;
                    font-weight: bold;
                    text-transform: uppercase;
                }
            }
        }

        @media screen and (max-width: 768px) {
            .content-container {
                display: flex;
                justify-content: center;
                align-items: center;
                height: 100vh;
                flex-direction: column;
            }

            .text-content {
                width: 90%;
                margin-left: 10px;
                margin-right: 10px;
                padding: 30px 20px;
                margin-top: 20px;
            }
        }
    }

    .btn {
        display: inline-block;
        padding: 2px 35px;
        font-family: 'Merriweather', serif;
        font-size: 18px;
        font-weight: bold;
        text-transform: uppercase;
        color: #ffffff;
        margin: 0 30px;
        cursor: pointer;
        text-decoration: none;
        background: linear-gradient(45deg, #003366, #b30000, #000000);
        border-radius: 25px;
        transition: all 0.3s ease-in-out;

        &:hover {
            transform: scale(1.05);
            box-shadow: 0 0 15px 5px rgba(212, 167, 111, 0.8);
        }

        @media screen and (max-width: 768px) {
            font-size: 16px;
            margin: 0 10px;
            padding: 12px 30px;
        }

        @media screen and (max-width: 480px) {
            font-size: 14px;
            margin: 0 10px;
            padding: 12px 30px;
        }
    }

    .btn-group {
        display: inline-block;
        gap: 10px;

        @media screen and (max-width: 768px) {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }
    }


}
</style>
