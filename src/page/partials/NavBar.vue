<template>
    <nav class="navbar">
        <ul class="nav-links">
            <li><a @click.prevent="scrollToSection('event-details')">Event Details</a></li>
            <li><a @click.prevent="scrollToSection('dress-code')">Dress Code</a></li>
            <li><a @click.prevent="scrollToSection('outfit-inspiration')">Outfit Inspiration</a></li>
            <li><a @click.prevent="scrollToSection('debutant-info')">Debutant Info</a></li>

            <li class="dropdown">
                <a>18 Celebrants</a>
                <ul class="dropdown-menu">
                    <li><a @click.prevent="scrollToSection('roses')">18 Roses</a></li>
                    <li><a @click.prevent="scrollToSection('blue-bills')">18 Blue Bills</a></li>
                    <li><a @click.prevent="scrollToSection('candles')">18 Candles</a></li>
                    <li><a @click.prevent="scrollToSection('treasures')">18 Treasures</a></li>
                </ul>
            </li>
            <li><a @click.prevent="scrollToSection('rsvp')">RSVP</a></li>
        </ul>
    </nav>
</template>

<script>
export default {
    name: 'Navbar',
    methods: {
        scrollToSection(sectionId) {
            const section = document.getElementById(sectionId);
            if (section) {
                section.scrollIntoView({ behavior: 'smooth' });
            }
        },
    },
};
</script>

<style lang="scss" scoped>
.navbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    background: linear-gradient(135deg, #003366, #b30000, #000000);
    padding: 8px 16px;
    z-index: 1000;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    font-family: 'Georgia', serif;
    text-transform: uppercase;
    letter-spacing: 1px;

    .nav-links {
        list-style: none;
        display: flex;
        gap: 20px;
        justify-content: center;

        li {
            display: inline;
            position: relative;
        }

        a {
            text-decoration: none;
            color: #ffffff;
            font-size: 14px;
            font-weight: bold;
            padding: 6px 10px;
            border-radius: 6px;
            transition: all 0.3s ease;
            position: relative;
            z-index: 1;

            &:hover {
                color: #d4a76f;
                cursor: pointer;
            }

            &:active {
                transform: translateY(2px);
            }

            &::after {
                content: "";
                position: absolute;
                left: 0;
                bottom: 0;
                width: 100%;
                height: 2px;
                background-color: #d4a76f;
                transform: scaleX(0);
                transform-origin: bottom right;
                transition: transform 0.3s ease-out;
            }

            &:hover::after {
                transform: scaleX(1);
                transform-origin: bottom left;
            }
        }

        .dropdown {
            position: relative;

            .dropdown-menu {
                display: none;
                position: absolute;
                top: 100%;
                right: 0;
                background: rgba(0, 0, 0, 0.85);
                padding: 0px 20px;
                list-style: none;
                box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
                border-radius: 10px;
                z-index: 9999;
                width: auto;
                white-space: nowrap;

                li {
                    width: 100%;
                    padding: 8px 12px;
                }

                li a {
                    font-size: 14px;
                    text-align: left;
                    width: 100%;
                    padding: 0;
                    display: block;
                    color: #ffffff;
                    font-weight: normal;

                    &:hover {
                        color: #d4a76f;
                    }
                }
            }

            &:hover .dropdown-menu {
                display: block;
                cursor: pointer;
            }
        }
    }
}
</style>
