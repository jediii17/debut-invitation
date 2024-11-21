<template>
    <section id="candles" class="scroll-page scroll-section candles">
        <div class="content-wrapper">
            <div class="text-content">
                <h2>18 Candles</h2>
                <div class="names-container">
                    <ul class="names-list">
                        <li>1. Santina Ratuin</li>
                        <li>2. Criscelle Obejas-Imperial</li>
                        <li>3. Akeisha Quitlong</li>
                        <li>4. Cheska Cipres</li>
                        <li>5. Julia Borromeo</li>
                        <li>6. Achie Fuentes</li>
                        <li>7. Jillian Reyes</li>
                        <li>8. Rhowee Miguel</li>
                        <li>9. Rianne Mance</li>
                        <li>10. Nigel Valente</li>
                        <li>11. Angel Pulgo</li>
                        <li>12. Breizzy Teodoro</li>
                        <li>13. Caroline Cruz</li>
                        <li>14. Nerlisa Domingcil</li>
                        <li>15. Emma Esto</li>
                        <li>16. Aidz Batang</li>
                        <li>17. Jazel Jacinto</li>
                        <li>18. Josie Jacinto</li>
                    </ul>

                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Candles',
};
</script>

<style lang="scss" scoped>
#candles {
    background: linear-gradient(135deg, #003366, #b30000, #000000);
    background-attachment: fixed;
    background-position: center;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #ffffff;
    padding: 20px;

    .content-wrapper {
        width: 100%;
        max-width: 800px;
        background-color: rgba(0, 0, 0, 0.7);
        border: 1px solid #d4a76f;
        border-radius: 20px;
        padding: 20px;
        box-shadow: 0px 4px 20px rgba(0, 0, 0, 0.3);
        text-align: center;
        overflow: hidden;
        margin: 0 auto;

        @media screen and (max-width: 768px) {
            max-width: 90%;
            padding: 15px;
            border-radius: 15px;
        }

        @media screen and (max-width: 480px) {
            max-width: 95%;
            padding: 10px;
            border-radius: 10px;
        }
    }

    .text-content {
        h2 {
            font-family: 'Merriweather', serif;
            font-size: 2.4rem;
            color: #d4a76f;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-weight: bold;
            margin-bottom: 20px;

            @media screen and (max-width: 768px) {
                font-size: 2rem;
            }

            @media screen and (max-width: 480px) {
                font-size: 1.8rem;
            }
        }

        .names-list {
            font-family: 'Georgia', serif;
            font-size: 1rem;
            color: #e2d2d2;
            line-height: 1.6;
            list-style: none;
            padding: 0;
            margin: 0;
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            justify-items: center;
            text-align: left;

            /* Adjust for mobile view */
            @media screen and (max-width: 768px) {
                grid-template-columns: repeat(2, 1fr);
            }

            @media screen and (max-width: 480px) {
                grid-template-columns: repeat(2, 1fr);
                gap: 10px;
            }
        }

        li {
            text-align: left;
            position: relative;
            padding-left: 10px;
            word-wrap: break-word;

            &:hover {
                transform: scale(1.05);
                text-shadow: 0 0 20px rgba(212, 167, 111, 0.8);
            }

            @media screen and (max-width: 768px) {
                font-size: 3.2vw;
            }

            @media screen and (max-width: 480px) {
                font-size: 2.7vw;
            }
        }
    }
}
</style>
