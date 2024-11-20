<template>
    <section id="debutant-info" class="scroll-page debutant-info">
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
    </section>
</template>

<script>
export default {
    name: 'DebutantInfo',
};
</script>

<style scoped lang="scss">
#debutant-info {
    background: linear-gradient(135deg, #9b6a3e, #2e4a46);
    padding: 40px;
    font-family: 'Baskerville', serif;

    color: #f4f1e1;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    margin: 20px auto;
    max-width: 800px;

    h2 {
        text-align: center;
        font-size: 28px;
        font-weight: bold;
        margin-bottom: 20px;
        color: #d4a76f;
    }

    ul {
        list-style: none;
        padding: 0;
        font-size: 18px;

        li {
            margin-bottom: 12px;
            line-height: 1.8;

            strong {
                color: #d4a76f;
                font-weight: bold;
            }
        }
    }
}
</style>