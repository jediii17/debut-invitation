<template>
    <section id="candles" class="scroll-page scroll-section candles">
        <div class="content-wrapper">
            <div class="text-content">
                <h2>18 Candles</h2>
                <div class="names-container">
                    <ul class="names-list">
                        <li>1. Santina Ratuin</li>
                        <li>6. Achie Fuentes</li>
                        <li>11. Angel Pulgo</li>
                        <li>16. Aidz Batang</li>

                        <li>2. Criscelle Obejas-Imperial</li>
                        <li>7. Jillian Reyes</li>
                        <li>12. Breizzy Teodoro</li>
                        <li>17. Jazel Jacinto</li>

                        <li>3. Akeisha Quitlong</li>
                        <li>8. Rhowee Miguel</li>
                        <li>13. Caroline Cruz</li>
                        <li>18. Josie Jacinto</li>

                        <li>4. Cheska Cipres</li>
                        <li>9. Rianne Mance</li>
                        <li>14. Nerlisa Domingcil</li>

                        <li></li>
                        <li>5. Julia Borromeo</li>
                        <li>10. Nigel Valente</li>
                        <li>15. Emma Esto</li>

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
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #ffffff;
}

.content-wrapper {
    width: 100%;
    max-width: 1000px;
    background-color: rgba(0, 0, 0, 0.7);
    border: 1px solid #d4a76f;
    border-radius: 20px;
    padding: 20px;
    box-shadow: 0px 4px 20px rgba(0, 0, 0, 0.3);
    text-align: center;
    overflow: hidden;
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
    }

    .names-container {
        max-height: 60vh;
        overflow-y: auto;
        padding-right: 10px;

        .names-list {
            font-family: 'Georgia', serif;
            font-size: 1.2rem;
            color: #e1e1e1;
            line-height: 1.6;
            list-style: none;
            padding: 0;
            margin: 0;
            display: grid;
            grid-template-columns: repeat(4, minmax(250px, 1fr));
            /* 4 columns layout */
            gap: 20px;
        }

        li {
            text-align: left;
            position: relative;
            padding-left: 10px;
            word-wrap: break-word;
        }

        li:hover {
            transform: scale(1.05);
            text-shadow: 0 0 20px rgba(212, 167, 111, 0.8);
        }

    }
}
</style>
