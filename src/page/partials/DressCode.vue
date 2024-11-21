<template>
    <section id="dress-code" class="scroll-page dress-code">
        <div class="container">
            <h2>Dress Code</h2>
            <p class="banner"><strong>Colors to avoid:</strong> Red and Blue</p>
            <p class="banner"><strong>Color Palette:</strong></p>
            <div class="color-palette">

                <div>
                    <div class="color-circle" style="background-color: #grey;">
                    </div>
                    <span class="color-name">Grey</span>
                </div>

                <div>
                    <div class="color-circle" style="background-color: #000000;">
                    </div>
                    <span class="color-name">Black</span>
                </div>

                <div>
                    <div class="color-circle" style="background-color: #ffffff;">
                    </div>
                    <span class="color-name">White</span>
                </div>

            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'DressCode'
};
</script>

<style scoped>
.dress-code {
    padding: 30px 20px;
    text-align: center;
    background: linear-gradient(135deg, #003366, #b30000, #000000);
    background-attachment: fixed;
    background-position: center;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #f2f1e1;
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
}

p {
    margin-top: 8px;
    font-size: 1.2rem;
    font-family: 'Merriweather', serif;
    color: #white;
}

h2 {
    font-family: 'Merriweather', serif;
    font-size: 2.4rem;
    color: #d4a76f;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
    margin-bottom: 20px;
}


.color-palette {
    display: flex;
    justify-content: center;
    gap: 30px;
    flex-wrap: wrap;
    margin-top: 20px;
}

.color-circle {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 80px;
    height: 80px;
    border-radius: 50%;
    margin: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
    position: relative;
    overflow: hidden;
    background-color: #ccc;
    transition: transform 0.2s ease, box-shadow 0.3s ease;
}

.color-circle:hover {
    transform: scale(1.05);
    box-shadow: 0 0 15px 5px rgba(212, 167, 111, 0.8);
}

.color-name {
    margin-top: 8px;
    font-size: 1.2rem;
    font-family: 'Merriweather', serif;
    color: #white;
}
</style>
