<template>
    <section id="treasures" class="scroll-page scroll-section treasures">
        <div class="content-wrapper">
            <div class="text-content">
                <h2>18th Treasures</h2>
                <div class="names-container">
                    <ul class="names-list">
                        <li>Pam Enriquez</li>
                        <li>Divine</li>
                        <li>Shalom</li>
                        <li>Melchelyn Limbaga-Batang</li>
                        <li>Princess Malabonga</li>
                        <li>Kearah Cueto</li>
                        <li>Angelita Ratuin</li>
                        <li>Steven Rongavilla</li>
                        <li>Franzeska Amandy</li>
                        <li>Lorenzo Barcenas</li>
                        <li>Aaron Bugarin</li>
                        <li>Christine Mojica</li>
                        <li>Rhian Santillan</li>
                        <li>Alleyah Arreza</li>
                        <li>Artgie Estrada</li>
                        <li>Kylie Celebre</li>
                        <li>Jiro Calinao</li>
                        <li>Walth Laguador</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Treasures',
};
</script>

<style lang="scss" scoped>
#treasures {
    background: linear-gradient(135deg, #003366, #b30000, #000000);
    background-attachment: fixed;
    background-position: center;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #f2f1e1;

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
                max-height: 100vh;

                .names-list {
                    font-family: 'Merriweather', serif;
                    font-size: 1.2rem;
                    color: #e1e1e1;
                    line-height: 1.6;
                    list-style: none;
                    padding: 10px;
                    margin: 5px;
                    display: grid;
                    grid-template-columns: repeat(5, 1fr);
                    gap: 10px;
                }

                li {
                    position: relative;
                    padding-left: 20px;
                    text-align: center;
                    border-radius: 10px;
                    padding: 12px;
                    color: #e1e1e1;
                    transition: transform 0.3s ease, box-shadow 0.3s ease;
                }

                li:hover {
                    transform: scale(1.05);
                    text-shadow: 0 0 20px rgba(212, 167, 111, 0.8);
                }
            }
        }
    }
}
</style>
