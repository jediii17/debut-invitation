<template>
    <section id="roses" class="scroll-page scroll-section roses">
        <div class="content-wrapper">
            <div class="text-content">
                <h2>18th Roses</h2>
                <div class="names-container">
                    <ul class="names-list">
                        <li>1. Ramon Jackytong Jacinto</li>
                        <li>6. Enrique Cruz</li>
                        <li>11. Cire Paul Cruz</li>
                        <li>16. Jherson Bulanhagui</li>

                        <li>2. Nickson Jacinto</li>
                        <li>7. John Mark Batang</li>
                        <li>12. Earvin Enriquez</li>
                        <li>17. Mirai Shin Takimoto</li>

                        <li>3. Jack Nichols Jacinto</li>
                        <li>8. Ezekiel Domingcil</li>
                        <li>13. Bjorn Custodio</li>
                        <li>18. Nick Jacinto</li>

                        <li>4. Aqui Domingcil</li>
                        <li>9. Timothy Cruz</li>
                        <li>14. Khalil Dwight Ramirez</li>
                        <li></li>

                        <li>5. Joefrey Batang</li>
                        <li>10. Jedidia Cruz</li>
                        <li>15. Thirdy Nabor</li>
                        <li></li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Roses',
};
</script>

<style lang="scss" scoped>
#roses {
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
