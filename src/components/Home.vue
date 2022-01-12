<template>
    <section class="main">
        <nav class="header">
            <h1>Spikkestad Pizza og Grill</h1>

            <div class="header__contact">
                <div class="header__contact-phone">
                    <img src="/svg/phone.svg" alt="phone-icon">
                    <p>31 28 75 06/ 48 95 96 14</p>
                </div>

                <div class="header__contact-facebook">
                    <img src="/svg/facebook.svg" alt="facebook-icon">

                    <a href="https://www.facebook.com/Spikkestad-pizza-og-grill-112698187314811/"><p>følg oss på Facebook for gode tilbud</p></a>
                </div>    
            </div>
        </nav>

        <Slider />
    
        <Collapsible :title="this.componentTitles.pizzaMenu"> 
            <PizzaMenu />    
        </Collapsible>

        <Collapsible :title="this.componentTitles.burgerMenu"> 
            <BurgerMenu /> 
        </Collapsible>

        <Collapsible :title="this.componentTitles.kebabMenu"> 
            <KebabMenu /> 
        </Collapsible>

        <Collapsible :title="this.componentTitles.plateDishesMenu"> 
            <PlateDishesMenu /> 
        </Collapsible> 

        <ScrollingImages />
    
        <Footer /> 
    </section>
</template>

<script>
    import Slider from '../components/Slider.vue';
    import Collapsible from '../components/Collapsible.vue';
    import PizzaMenu from '../components/PizzaMenu.vue';
    import BurgerMenu from '../components/BurgerMenu.vue';
    import KebabMenu from '../components/KebabMenu.vue';
    import PlateDishesMenu from '../components/PlateDishesMenu.vue';
    import Footer from '../components/Footer.vue';
    import ScrollingImages from '../components/ScrollingImages.vue';

    export default {
        components: {
            Slider,
            Collapsible,
            PizzaMenu,
            BurgerMenu,
            KebabMenu,
            PlateDishesMenu,
            Footer,
            ScrollingImages
        },

        data() {
            return {
                componentTitles: { 
                    pizzaMenu: 'Pizza Meny',
                    burgerMenu: 'Hambuger Meny',
                    kebabMenu: 'Kebab Meny',
                    plateDishesMenu: 'Tallerkenretter / Barnemeny / Diverse'   
                }
            }
        }
    }
</script>

<style>
    .main {
        width: 100%;
    }
    .header {
        width: 100%;
        text-align: center;
        padding-top: 20px;
    }

    .header > h1 {
        font-size: 2.5em;
    }

    .header__contact-phone, .header__contact-facebook {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        padding-bottom: 10px;
    }

    .header__contact-phone > p,
    .header__contact-facebook > a > p {
        padding: 10px;
        color: #FBF6E5;
        font-size: 1.25em;
    }

    .header__contact-facebook > a {
        /* text-decoration: none; */
         color: #FBF6E5;
    }

    .header__contact-facebook > a > p:hover {
        color: var(--foreground);
    }

    .header__contact-phone > img, .header__contact-facebook > img {
        width: 30px;
    }

    /* small devices (mobiles, 1140px and down) */
    @media screen and (max-width: 1140px) {
        .header > h1 {
            padding-top: 20px;
            font-size: 3.75em;
        }

        .header__contact-phone > p, .header__contact-facebook > a > p  {
            font-size: 1.75em;
        }

        .header__contact-phone > img, .header__contact-facebook > img {
            width: 40px;
        }
    }
</style>