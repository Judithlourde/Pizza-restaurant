<template>
    <section class="main">
        <nav class="header">
            <h1>Spikkestad Pizza og Grill</h1>

            <div class="header__phone">
                <img src="/svg/phone.svg" alt="phone-icon">
                <p>31 28 75 06/ 48 95 96 14</p>
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

    .header__phone {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        padding-bottom: 18px;
    }

    .header__phone > p {
        padding: 10px;
        color: white;
        font-size: 1.25em;
    }

    .header__phone > img {
        width: 30px;
    }

    @media screen and (max-width: 1140px) {
        .header > h1 {
            padding-top: 20px;
            font-size: 3.75em;
        }

        .header__phone > p  {
            font-size: 1.75em;
        }

        .header__phone > img {
            width: 40px;
        }
    }
</style>