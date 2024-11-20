<template>
    <section id="rsvp" class="scroll-page rsvp">
        <h2>RSVP</h2>
        <a href="https://forms.gle/LMzA357oYqg2wW357" target="_blank" class="btn">RSVP Here</a>
    </section>
</template>

<script>
export default {
    name: 'RSVP',
};
</script>

<style lang="scss" scoped>
.btn {
    display: inline-block;
    padding: 12px 30px;
    font-family: 'Georgia', serif;
    font-size: 18px;
    font-weight: bold;
    color: #ffffff;
    text-decoration: none;
    background: linear-gradient(45deg, #5f7a9a, #b24c63);
    border: 2px solid #2e2e2e;
    border-radius: 25px;
    transition: all 0.3s ease-in-out;

    &:hover {
        background: linear-gradient(45deg, #b24c63, #5f7a9a);

        transform: scale(1.05);

    }
}
</style>