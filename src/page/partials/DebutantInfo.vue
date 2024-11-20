<template>
    <section id="debutant-info" class="scroll-page debutant-info">
        <div class="content-wrapper">
            <h2>Debutant’s Information</h2>
            <ul>
                <li><strong>Height:</strong> 5’3</li>
                <li><strong>Shoe Size:</strong> 6</li>
                <li><strong>Clothing Size:</strong> Small to Medium</li>
                <li><strong>Waist Size:</strong> 23 inches</li>
                <li><strong>Hips Size:</strong> 25 inches</li>
                <li><strong>Favorite Color:</strong> Blue</li>
                <li><strong>Jewelry:</strong> Silver</li>
                <li><strong>Makeup:</strong> Cool Tone</li>
            </ul>
        </div>
    </section>
</template>

<script>
export default {
    name: 'DebutantInfo',
};
</script>

<style scoped lang="scss">
#debutant-info {
    background: linear-gradient(135deg, #003366, #b30000, #000000);
    background-attachment: fixed;
    background-position: center;
    padding: 60px 0;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #f2f1e1;

    .content-wrapper {
        width: 90%;
        max-width: 800px;
        background-color: rgba(0, 0, 0, 0.7);
        border: 1px solid #d4a76f;
        border-radius: 20px;
        padding: 30px;
        box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
        text-align: center;

        h2 {
            font-family: 'Merriweather', serif;
            font-size: 2.4rem;
            color: #d4a76f;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-weight: bold;
            margin-bottom: 20px;
        }

        ul {
            list-style: none;
            padding: 0;
            font-size: 1.5rem;
            line-height: 2;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;

            li {
                position: relative;
                font-family: 'Merriweather', serif;
                padding-left: 10px;
                background-color: #1a2d50;
                border-radius: 10px;
                padding: 12px;
                color: #e1e1e1;
                box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
                transition: transform 0.3s ease, box-shadow 0.3s ease;
            }

            li:hover {
                transform: scale(1.05);
                box-shadow: 0 0 20px rgba(212, 167, 111, 0.8);
            }

            strong {
                font-family: 'Merriweather', serif;
                color: #d4a76f;
                font-weight: bold;
            }
        }
    }
}
</style>
