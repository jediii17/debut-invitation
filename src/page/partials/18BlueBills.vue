<template>
    <section id="blue-bills" class="scroll-page scroll-section blue-bills">
        <div class="content-wrapper">
            <div class="text-content">
                <h2>18 Blue Bills</h2>
                <div class="names-container">
                    <ul class="names-list">
                        <li>1. Aidz Batang</li>
                        <li>6. Leny</li>
                        <li>11. Josie</li>
                        <li>16. Timmy</li>
                        <li> 2. Nerlisa Domingcil</li>

                        <li>7. Alma</li>
                        <li>12. Len</li>
                        <li>17. Luisa</li>
                        <li>3. Caroline Cruz</li>
                        <li> 8. Waylla</li>

                        <li>13. Laura</li>
                        <li>18. Pastor Diquito</li>
                        <li>4. Cris Ratuin</li>
                        <li>9. Rely</li>
                        <li>14. Edsel</li>

                        <li></li>
                        <li>5. Sherwin Undayag</li>
                        <li>10. Emily</li>
                        <li>15. Herman</li>
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
    width: 100%;
    max-width: 1030px;
    /* Adjust this for responsiveness */
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
        /* Adjust if you want a smaller scrollable area */
        overflow-y: auto;
        padding-right: 10px;

        .names-list {
            font-family: 'Georgia', serif;
            font-size: 1rem;
            color: #e2d2d2;
            line-height: 1.6;
            list-style: none;
            padding: 0;
            margin: 0;
            display: grid;
            grid-template-columns: repeat(4, minmax(250px, 1fr));
            /* 4 columns with adjustable width */
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
