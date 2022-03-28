<template>
    <section class="plateDishesMenu">
        <ul class="plateDishesMenu__list">
            <div> 
                <h1>{{ plateDishesTitle }}</h1>
                <p>{{ plateDishesDescription }}</p>
            </div>

            <li>
                <h3></h3>

                <div>
                    <div class="plateDishesMenu__list-takeAway">
                        <span>{{ takeAwayTitle }}</span>
                        <p>{{ takeAwayPant }}</p>
                    </div>
                    
                    <span>{{ dinningInTitle }}</span>
                </div>   
            </li>

            <li v-for="plateDish in plateDishes" :key="plateDish"> 
                <div>
                    <h3>{{ plateDish.name }}</h3>
                    <p class="plateDishesMenu__list-allergi">{{ plateDish.allergi }}</p>
                </div>
                

                <div>
                    <span>{{ plateDish.takeAway }}</span>
                    <span>{{ plateDish.dinningIn }}</span>
                </div>
            </li>
        </ul>

        <ul class="plateDishesMenu__list">
            <div> 
                <h1>{{ kidsMenuTitle }}</h1>
                <p>{{ kidsMenuDescription }}</p>
            </div>

            <li> 
                <h3></h3>

                <div>
                    <span>{{ takeAwayTitle }}</span>
                    <span>{{ dinningInTitle }}</span>
                </div>
            </li>

            <li v-for="menu in kidsMenu" :key="menu">
                <div>
                    <h3>{{ menu.name }}</h3>
                    <p class="plateDishesMenu__list-allergi">{{menu.allergi}}</p>
                </div> 

                <div>
                    <span>{{ menu.takeAway }}</span>
                    <span>{{ menu.dinningIn }}</span>
                </div>
            </li>

            <figure class="plateDishesMenu__image">
                <img src="/images/kids_menu.jpg" alt="kids_menu-image">
                <figcaption>Barnemeny</figcaption>
            </figure>
        </ul>
    </section> 

    <section class="plateDishesMenu">
        <ul class="plateDishesMenu__list">
            <div> 
                <h3>{{ otherDishesTitle }}</h3>
            </div>

            <li>
                <h3></h3>

                <div>
                    <span>{{ takeAwayTitle }}</span>
                    <span>{{ dinningInTitle }}</span>
                </div>   
            </li>

            <li v-for="otherDish in otherDishes" :key="otherDish"> 
                <div>
                    <h3>{{ otherDish.name }}</h3>
                    <p class="plateDishesMenu__list-allergi">{{ otherDish.allergi }}</p>
                </div>

                <div>
                    <span>{{ otherDish.takeAway }}</span>
                    <span>{{ otherDish.dinningIn }}</span>
                </div>
            </li>
        </ul>
 
        <figure class="plateDishesMenu__image">
            <img src="/images/plate_menu.jpg" alt="Plate_Dishes_menu-image">
            <figcaption>Tallerkenretter</figcaption>
        </figure>

    </section>
</template>

<script>
    export default {
        data() {
            return {
                plateDishesTitle: 'TALLERKENRETTER',
                plateDishesDescription: 'Serveres med salat, tomat, rødløk, mais, dressing, pommes frites, bernaise og 0,5 l drikke',
                otherDishesTitle: 'DIVERSE',
                kidsMenuTitle: 'BARNEMENY',
                kidsMenuDescription: 'Serveres med pommes frites og Kuli',
                takeAwayTitle: 'Ta med',
                takeAwayPant: 'Pant +2Kr',
                dinningInTitle: 'Inne',

                plateDishes: [ {name: '50. Biffsnaddertallerken', takeAway: '194,-', dinningIn: '204,-', allergi: 'Egg, Melk, Selleri, Sennep'}, {name: '51. Kyllingsnaddertallerken', takeAway: '194,-', dinningIn: '204,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri, Sennep'}, {name: '52. Kyllingfiletmiddag', takeAway: '220,-', dinningIn: '230,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri, Sennep' }, {name: '53. Løvstektallerken enkel', takeAway: '150,-', dinningIn: '160,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri, Sennep'}, {name: '54. Løvstektallerken dobbel', takeAway: '184,-', dinningIn: '194,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri, Sennep'}, {name: '55. Nuggetstallerken 7 biter', takeAway: '109,-', dinningIn: '110,-', allergi: 'Gluten (Hvete)' }, {name: '56. Nuggetstallerken 12 biter', takeAway: '149,-', dinningIn: '159,-', allergi: 'Gluten (Hvete)' } ],

                otherDishes: [ {name: 'Pommes frites liten', takeAway: '45,-', dinningIn: '55,-', allergi: 'Selleri (i krydderet)'}, {name: 'Pommes frites stor', takeAway: '55,-', dinningIn: '65,-', allergi: 'Selleri (i krydderet)'}, {name: 'Brus 0,5 l', takeAway: '35,-', dinningIn: '38,-'}, {name: 'Brus 1,5 l', takeAway: '55,-', dinningIn: '60,-'} ],

                kidsMenu: [ {name: 'Grillpølse', takeAway: '80,-', dinningIn: '90,-', allergi: 'Brød: Gluten (Hvete), Egg, Melk, Sesam, Pommes frites: Selleri (i krydderet)'}, {name: 'Nuggets', takeAway: '80,-', dinningIn: '90,-', allergi: 'Pommes frites: Selleri (i krydderet)'} ]
            }
        }    
    }
</script>

<style>
    .plateDishesMenu {
        background: #3A3A3A;
        max-width: calc(886px + 24%);
        margin-left: auto;
        margin-right: auto;
        padding: 10px;
        display: grid;
        grid-template-columns: 1fr 1fr;
        font-size: .85em;
    }

    .plateDishesMenu__list {
        width: 100%;
        height: 100%;
        padding: 20px;
    }

    .plateDishesMenu__list > div > p {
        font-family: var(--second-font-family);
    }

    .plateDishesMenu__list > div > h1 {
        color: var(--foreground);
    }

    .plateDishesMenu__list li {
        width: 100%;
        display: grid;
        grid-template-columns: 2fr 1fr;
        padding: 10px;
    }

    .plateDishesMenu__list-allergi {
        color: rgb(240, 196, 179);
        font-style: italic;
        padding-top: 5px;
        font-family: var(--second-font-family);
    }

    .plateDishesMenu__list > div {
        color: #FBF6E5;
    }

    .plateDishesMenu__list > li > div:nth-child(2) {
        display: grid;
        grid-template-columns: 1fr 1fr;
    }

    .plateDishesMenu__list li > div > span {
        padding: 5px;
        color: #FBF6E5;
        font-size: 1.2em;
        text-align: right;
    }

    .plateDishesMenu__list-takeAway {
        color: #FBF6E5; 
        text-align: right; 
        font-size: 1em;  
    }

    .plateDishesMenu__list-takeAway > p {
        padding-top: 5px;
    }

    .plateDishesMenu__image {
        position: relative;
        padding: 30px;
    }

    .plateDishesMenu__image > figcaption {
        text-align: center;
    }

    .plateDishesMenu__image > img {
        width: 100%;
        object-fit: cover;
    }

    /* small devices (mobiles, 1140px and down) */
    @media screen and (max-width: 1140px) {
        .plateDishesMenu {
            font-size: 1.1em;
            max-width: calc(786px + 14%);
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        .plateDishesMenu__image {
            align-self: center;
        }

        .plateDishesMenu__list li {
            width: 100%;
            display: grid;
            grid-template-columns: 1fr 1fr;
            padding: 10px;
        }
    }
</style>