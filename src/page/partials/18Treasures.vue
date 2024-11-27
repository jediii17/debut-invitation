<template>
    <section id="treasures" class="scroll-page scroll-section candles">
        <div class="content-wrapper">
            <div class="text-content">
                <h2>18 Treasures</h2>
                <div class="names-container">
                    <ul class="names-list">
                        <li>1. Pam Enriquez</li>
                        <li>2. Divine Madriaga</li>
                        <li>3. Shalom Domingcil</li>
                        <li>4. Melchelyn Limbaga-Batang</li>
                        <li>5. Princess Malabonga</li>
                        <li>6. Kearah Cueto</li>
                        <li>7. Angelita Ratuin</li>
                        <li>8. Steven Rongavilla</li>
                        <li>9. Franzeska Amandy</li>
                        <li>10. Lorenzo Barcenas</li>
                        <li>11. Aaron Bugarin</li>
                        <li>12. Christine Mojica</li>
                        <li>13. Rhian Santillan</li>
                        <li>14. Alleyah Arreza</li>
                        <li>15. Artgie Estrada</li>
                        <li>16. Kylie Celebre</li>
                        <li>17. Jiro Calinao</li>
                        <li>18. Walth Laguador</li>
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
#treasures {
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
