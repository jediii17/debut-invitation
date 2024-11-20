<template>
    <nav class="navbar desktop-nav">

        <div class="mobile-logo" v-if="isMobileView">Nicolai @18</div>

        <!-- Navigation Links -->
        <ul class="nav-links" :class="{ 'active': isMenuOpen }">
            <li><a @click.prevent="handleNavClick('event-details')">Event Details</a></li>
            <li><a @click.prevent="handleNavClick('dress-code')">Dress Code</a></li>
            <li><a @click.prevent="handleNavClick('outfit-inspiration')">Outfit Inspiration</a></li>
            <li><a @click.prevent="handleNavClick('debutant-info')">Debutant Info</a></li>
            <li class="dropdown">
                <a>18 Celebrants</a>
                <ul class="dropdown-menu">
                    <li><a @click.prevent="handleNavClick('roses')">18 Roses</a></li>
                    <li><a @click.prevent="handleNavClick('blue-bills')">18 Blue Bills</a></li>
                    <li><a @click.prevent="handleNavClick('candles')">18 Candles</a></li>
                    <li><a @click.prevent="handleNavClick('treasures')">18 Treasures</a></li>
                </ul>
            </li>
            <li><a @click.prevent="handleNavClick('rsvp')">RSVP</a></li>
        </ul>

        <!-- Hamburger menu icon -->
        <div class="menu-icon" @click="toggleMenu">
            <span class="bar"></span>
            <span class="bar"></span>
            <span class="bar"></span>
        </div>
    </nav>
</template>

<script>
export default {
    name: 'Navbar',
    data() {
        return {
            isMenuOpen: false,
            isMobileView: false
        };
    },
    methods: {
        scrollToSection(sectionId) {
            const section = document.getElementById(sectionId);
            if (section) {
                section.scrollIntoView({ behavior: 'smooth' });
            }
        },
        toggleMenu() {
            this.isMenuOpen = !this.isMenuOpen;
        },
        handleNavClick(sectionId) {
            this.scrollToSection(sectionId);
            if (this.isMenuOpen) {
                this.toggleMenu();
            }
        },
        checkMobileView() {
            this.isMobileView = window.innerWidth <= 768;
        }
    },
    mounted() {
        this.checkMobileView();
        window.addEventListener('resize', this.checkMobileView);
    },
    beforeDestroy() {
        window.removeEventListener('resize', this.checkMobileView);
    }
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
    display: flex;
    justify-content: center;
    align-items: center;

    .nav-links {
        list-style: none;
        display: flex;
        gap: 20px;
        justify-content: center;
        /* Center nav links on desktop */
        transition: transform 0.3s ease;

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

/* Mobile view */
@media screen and (max-width: 768px) {
    .navbar {
        justify-content: space-between;
        padding: 25px 16px;
        text-transform: capitalize;

        .mobile-logo {
            display: block;
            font-family: "Pinyon Script", serif;
            font-size: 30px;
            font-weight: bold;
            color: #fff;
            letter-spacing: 1px;
            position: absolute;
            left: 20px;
            top: 50%;
            transform: translateY(-50%);
        }

        .nav-links {
            position: absolute;
            top: 30px;
            left: 0px;
            width: 100%;
            background: rgba(0, 0, 0, 0.85);
            flex-direction: column;
            align-items: center;
            padding: 2px 2px;
            justify-content: center;
            transform: translateX(-100%);
            opacity: 0;
            transition: transform 0.3s ease, opacity 0.3s ease;
            z-index: 1000;

            &.active {
                transform: translateX(0);
                opacity: 1;
            }

            .nav-links li {
                margin: 20px 0;
            }

            .dropdown-menu {
                position: relative;
                top: 0;
                background: rgba(0, 0, 0, 0.85);
                padding: 10px 20px;
                //border: 2px solid #d4a76f;
                /* Gold border */
                border-radius: 5px;
                /* Optional: rounded corners */
                box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
                /* Optional: shadow */
            }

            .dropdown:hover .dropdown-menu {
                display: block;
            }
        }

        .menu-icon {
            display: flex;
            flex-direction: column;
            gap: 5px;
            cursor: pointer;
            z-index: 10;
            position: absolute;
            right: 50px;
            /* Move hamburger menu to the right */
            top: 50%;
            /* Center hamburger vertically */
            transform: translateY(-50%);

            .bar {
                width: 25px;
                height: 3px;
                background-color: #ffffff;
            }
        }
    }
}
</style>
