<template>
    <section id="candles" class="scroll-page scroll-section candles">
        <div class="content-wrapper">
            <div class="text-content">
                <h2>18th Candles</h2>
                <div class="names-container">
                    <ul class="names-list">
                        <li>Santina Ratuin</li>
                        <li>Criscelle Obejas-Imperial</li>
                        <li>Akeisha Quitlong</li>
                        <li>Cheska Cipres</li>
                        <li>Julia Borromeo</li>

                        <li>Achie Fuentes</li>
                        <li>Jillian Reyes</li>
                        <li>Rhowee Miguel</li>
                        <li>Rianne Mance</li>
                        <li>Nigel Valente</li>

                        <li>Angel Pulgo</li>
                        <li>Breizzy Teodoro</li>
                        <li>Caroline Cruz</li>
                        <li>Nerlisa Domingcil</li>
                        <li>Emma Esto</li>

                        <li>Aidz Batang</li>
                        <li>Jazel Jacinto</li>
                        <li>Josie Jacinto</li>
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
    width: 90%;
    max-width: 900px;
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
            grid-template-columns: repeat(5, 1fr);
            gap: 20px;
        }

        li {
            text-align: left;
            position: relative;
            padding-left: 10px;
            word-wrap: break-word;
        }
    }
}
</style>
