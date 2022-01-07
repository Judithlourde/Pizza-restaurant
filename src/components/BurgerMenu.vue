<template>
    <section class="burgerMenu">
        <ul class="burgerMenu__list">
            <div> 
                <h1>{{ burgerTitle }}</h1>
                <p>{{ burgerDecription }}</p>
                <p class="burgerMenu__list-allergi">{{ allergi }}</p>
            </div>

            <li>
                <p></p>

                <div>
                    <span>{{ takeAway }}</span>
                    <span>{{ dinningIn }}</span>
                </div>   
            </li>

            <li v-for="burgerItem in burgerItemsFirst" :key="burgerItem"> 
                <h3>{{ burgerItem.name }}</h3>
               
                <div>
                    <span>{{ burgerItem.takeAway }}</span>
                    <span>{{ burgerItem.dinningIn }}</span>
                </div>
            </li>
        </ul>

        <ul class="burgerMenu__list">
            <div> 
                <h1>{{ burgerMenu }}</h1>
                <p>{{ burgerMenuDescription }}</p>
                <p class="burgerMenu__list-allergi">{{ allergi }}</p>
            </div>

            <li>
                <p></p>

                <div>
                    <span>{{ takeAway }}</span>
                    <span>{{ dinningIn }}</span>
                </div>   
            </li>

            <li v-for="burgerItem in burgerItemsSecond" :key="burgerItem"> 
                <h3>{{ burgerItem.name }}</h3>
               
                <div>
                    <span>{{ burgerItem.takeAway }}</span>
                    <span>{{ burgerItem.dinningIn }}</span>
                </div>
            </li>
        </ul>
    </section> 

    <section class="burgerMenu">
        <ul class="burgerMenu__list">
            <li> 
                <h3>{{ extraMenu }}</h3>

                <div>
                    <span>{{ takeAway }}</span>
                    <span>{{ dinningIn }}</span>
                </div>
            </li>

           <li v-for="extraMenuItem in extraMenuItems" :key="extraMenuItem"> 
                <h3>{{ extraMenuItem.name }}</h3>
               
                <div>
                    <span>{{ extraMenuItem.takeAway }}</span>
                    <span>{{ extraMenuItem.dinningIn }}</span>
                </div>
            </li>
        </ul>
        
        <ul class="burgerMenu__images">
            <div class="burgerMenu__image">
                <img src="/images/burger.jpg" alt="burger-image">
            </div>

            <div class="burgerMenu__image">
                <img src="/images/burger2.jpg" alt="burger-image">
            </div>

            <div class="burgerMenu__image">
                <img src="/images/cola.jpg" alt="cola-image">
            </div>
        </ul>
        
    </section>
</template>

<script>
    export default {
        data() {
            return {
                burgerTitle: 'HAMBURGER',
                burgerDecription: 'Serveres med brød, salat, dressing, tomat og rødløk',
                burgerMenu: 'HAMBURGERMENY',
                burgerMenuDescription: 'Serveres med brød, salat, dressing, tomat, rødløk, pommes frites og 0,5 l drikke',
                extraMenu: 'Tilbehør:',
                allergi: 'Gluten (Hvete), Egg, Melk, Selleri, Sennep',
                takeAway: 'Ta med',
                dinningIn: 'Inne',
                burgerItemsFirst: [
                    {name: '23. Hamburger 100g', takeAway: '70,-', dinningIn: '80,-'},
                    {name: '24. Hamburger 130g', takeAway: '80,-', dinningIn: '90,-'},
                    {name: '25. Hamburger 160g', takeAway: '90,-', dinningIn: '100,-'},
                    {name: '26. Hamburger 190g', takeAway: '110,-', dinningIn: '120,-'},
                    {name: '27. Hamburger 250g', takeAway: '130,-', dinningIn: '140,-'},
                    {name: '28. Løvstekburger', takeAway: '90,-', dinningIn: '100,-'},
                ],

                burgerItemsSecond: [
                    {name: '29. Hamburger 100g', takeAway: '120,-', dinningIn: '130,-'},
                    {name: '30. Hamburger 130g', takeAway: '130,-', dinningIn: '140,-'},
                    {name: '31. Hamburger 160g', takeAway: '140,-', dinningIn: '150,-'},
                    {name: '32. Hamburger 190g', takeAway: '160,-', dinningIn: '170,-'},
                    {name: '33. Hamburger 250g', takeAway: '180,-', dinningIn: '190,-'},
                ],

                extraMenuItems: [
                    {name: 'Ost', takeAway: '10,-', dinningIn: '12,-'},
                    {name: 'Bacon', takeAway: '12,-', dinningIn: '14,-'}
                ]

            }
            
        },
    }
</script>

<style>
    .burgerMenu {
        background: #3A3A3A;
        max-width: calc(886px + 24%);
        margin-left: auto;
        margin-right: auto;
        padding: 10px;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: flex-start;
        font-size: .85em;
    }

    .burgerMenu__list {
        width: 100%;
        height: 100%;
        padding: 20px;
    }

    .burgerMenu__list > div > p {
        font-family: var(--second-font-family);
    }

    .burgerMenu__list > div > h1 {
        color: var(--foreground);
    }

    .burgerMenu__list li {
        width: 100%;
        display: grid;
        grid-template-columns: 2fr 1fr;
        padding: 10px;
    }

    .burgerMenu__list-allergi {
        color: rgb(240, 196, 179);
        font-style: italic;
        padding-top: 5px;   
    }

    .burgerMenu__list > div {
        color: #FBF6E5;
    }

    .burgerMenu__list > li > div { 
        display: grid;
        grid-template-columns: 1fr 1fr;
    }

    .burgerMenu__list li > div > span {
        padding: 5px;
        color: #FBF6E5;
        font-size: 1.2em;
        text-align: right;
        /* padding: 5px; */
    }

    .burgerMenu__images {
        display: flex;
        gap: 10px;
        padding: 30px 0;
    }

    .burgerMenu__image {
        width: 200px;
        height: 200px;
    }

    .burgerMenu__image > img {
        width: 100%;
        height: 100%;
    }

    /* small devices (mobiles, 768px and down) */
    @media screen and (max-width: 1140px) {
        .burgerMenu {
            font-size: 1.1em;
            max-width: calc(786px + 14%);
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        .burgerMenu__image {
            width: 300px;
            height: 300px;
        }

        .burgerMenu__list li {
            width: 100%;
            display: grid;
            grid-template-columns: 1fr 1fr;
            padding: 10px;
        }
    }
</style>