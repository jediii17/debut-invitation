<template>
    <section id="blue-bills" class="scroll-page scroll-section blue-bills">
        <div class="content-wrapper">
            <div class="text-content">
                <h2>18th Blue Bills</h2>
                <div class="names-container">
                    <ul class="names-list">
                        <li>Aidz Batang</li>
                        <li>Nerlisa Domingcil</li>
                        <li>Caroline Cruz</li>
                        <li>Cris Ratuin</li>
                        <li>Sherwin Undayag</li>

                        <li>Leny</li>
                        <li>Alma</li>
                        <li>Waylla</li>
                        <li>Rely</li>
                        <li>Emily</li>

                        <li>Josie</li>
                        <li>Len</li>
                        <li>Laura</li>
                        <li>Edsel</li>
                        <li>Herman</li>

                        <li>Timmy</li>
                        <li>Luisa</li>
                        <li>Pastor Diquito</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'BlueBills',
};
</script>

<style lang="scss" scoped>
#blue-bills {
    background: linear-gradient(135deg, #003366, #b30000, #000000);
    background-attachment: fixed;
    background-position: center;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #f2f1e1;
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
            /* 5 items per row */
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
