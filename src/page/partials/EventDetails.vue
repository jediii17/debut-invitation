<template>
    <section id="event-details" class="scroll-page event-details">
        <div class="content-container">
            <div class="text-content">
                <h1>Nicolai @18</h1>
                <div class="event-info">
                    <p><strong>Venue:</strong> Sunlane Resort, Ilang-ilang St. Extension, Solemar Del Pansol Subd.,
                        Brgy. Pansol, Calamba City, Laguna, Philippines</p>
                    <p><strong>Date:</strong> December 13, 2024</p>
                    <p><strong>Time:</strong> 6 PM onwards</p>
                    <p><strong>Theme:</strong> Old Money</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'EventDetails',
};
</script>

<style lang="scss" scoped>
#event-details {
    padding: 100px 20px;
    background-image: url('@/assets/img/oldmoney.jpg');
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #f4f1e1;
    height: 100vh;
    box-shadow: inset 0 0 300px rgba(0, 0, 0, 0.4);

    .content-container {
        max-width: 1200px;
        width: 100%;
        display: flex;
        justify-content: flex-end;
        align-items: center;
        padding-right: 20px;

        .text-content {
            background: rgba(0, 0, 0, 0.65);
            padding: 60px 40px;
            width: 50%;
            margin-left: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.15);
            border: 1px solid rgba(255, 255, 255, 0.3);

            h1 {
                font-family: 'Baskerville', serif;
                font-size: 4rem;
                color: #d4a76f;
                font-weight: bold;
                margin-bottom: 30px;
                text-transform: uppercase;
                letter-spacing: 2px;
                text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.4);
            }

            .event-info {
                font-family: 'Georgia', serif;
                font-size: 1.6rem;
                line-height: 2;
                color: #f4f1e1;
                text-align: left;

                p {
                    margin-bottom: 15px;
                }

                strong {
                    color: #d4a76f;
                    font-weight: bold;
                    text-transform: uppercase;
                }
            }
        }
    }
}
</style>
