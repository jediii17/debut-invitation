<template>
    <section id="rsvp" class="scroll-page rsvp">

        <div>
            <a href="https://forms.gle/LMzA357oYqg2wW357" target="_blank" class="btn">RSVP</a>
        </div>
        <div class="content-wrapper">
            <p>
                Bring your enthusiasm and festive spirit! I hope you can make it to celebrate with me. Kindly RSVP on or
                before December 5, 2024 to ensure your spot in my special day.
            </p>
        </div>
    </section>
</template>

<script>
export default {
    name: 'RSVP',
};
</script>

<style lang="scss" scoped>
#rsvp {
    background-image: url('@/assets/img/dress_bg.png');
    //background: linear-gradient(135deg, #003366, #b30000, #000000);
    background-position: center;
    padding: 40px 0;
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

        p {
            font-family: 'Merriweather', serif;
            font-size: 1rem;
        }
    }
}

.btn {
    display: inline-block;
    padding: 12px 30px;
    font-family: 'Merriweather', serif;
    font-size: 18px;
    color: #ddd9d9;
    text-decoration: none;
    background: linear-gradient(45deg, #003366, #b30000, #000000);
    border-radius: 25px;
    transition: all 0.3s ease-in-out;
    margin-bottom: 10px;

    &:hover {
        transform: scale(1.05);
        box-shadow: 0 0 15px 5px rgba(212, 167, 111, 0.8);

    }
}
</style>
