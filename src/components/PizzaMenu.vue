<template>
    <section class="pizzaMenu">
        <ol class="pizzaMenu__list">
            <li>
               <h3>{{ eatingHere }}</h3>   

               <div class="pizzaMenu__pizzaSize">
                    <div> 
                        <span>{{ medium }}</span>
                        <span>{{ thirtyCM }}</span>
                    </div>

                    <div> 
                        <span>{{ large }}</span>
                        <span>{{ fourtyCM }}</span>
                    </div>

                    <div> 
                        <span>{{ glutenfri }}</span>
                        <span>{{ thirtyCM }}</span>
                    </div>  
                </div>   
            </li>

            <li v-for="pizzaItem in pizzaItemsFirst" :key="pizzaItem">
                <div class="pizzaMenu__pizzaName"> 
                    <h3>{{ pizzaItem.name }}</h3>
                    <p>{{ pizzaItem.description }}</p> 
                    <p>{{ pizzaItem.allergi }}</p>
                </div> 

                <div class="pizzaMenu__pizzaPrice">
                    <span>{{ pizzaItem.medium }}</span>
                    <span>{{ pizzaItem.large }}</span>
                    <span>{{ pizzaItem.glutenfri }}</span>
                </div>
            </li>
        </ol>

        <ol class="pizzaMenu__list">
            <li class="pizzaMenu__list--mobile">
                <h3></h3>   
                <div class="pizzaMenu__pizzaSize">
                    <div> 
                        <span>{{ medium }}</span>
                        <span>{{ thirtyCM }}</span>
                    </div>

                    <div> 
                        <span>{{ large }}</span>
                        <span>{{ fourtyCM }}</span>
                    </div>

                    <div> 
                        <span>{{ glutenfri }}</span>
                        <span>{{ thirtyCM }}</span>
                    </div>    
                </div>   
            </li> 

            <li v-for="pizzaItem in pizzaItemsSecond" :key="pizzaItem">
                <div class="pizzaMenu__pizzaName"> 
                    <h3>{{ pizzaItem.name }}</h3>
                    <p>{{ pizzaItem.description }}</p>
                    <p>{{ pizzaItem.allergi }}</p>
                </div> 

                <div class="pizzaMenu__pizzaPrice">
                    <span>{{ pizzaItem.medium }}</span>
                    <span>{{ pizzaItem.large }}</span>
                    <span>{{ pizzaItem.glutenfri }}</span>
                </div>
            </li>

            <li>
                <div class="pizzaMenu__list-extra"> 
                    <h2>{{ extraMenu }}</h2>
                </div> 

            </li>
            <li v-for="extraMenuItem in extraMenuItems" :key="extraMenuItem">
                <div class="pizzaMenu__pizzaName-extra"> 
                    <h3 class="pizzaMenu__list-extra">{{ extraMenuItem.name }}</h3>
                    <p>{{ extraMenuItem.allergi }}</p>
                </div> 

                <div class="pizzaMenu__pizzaPrice">
                    <span>{{ extraMenuItem.price }}</span>
                </div>
            </li>
        </ol>
    </section>   
</template>

<script>
	export default {
		data() {
			return {
                eatingHere: 'Spis her + 10kr',
                medium: 'Medium',
                large: 'Stor',
                glutenfri: 'Glutenfri',
                thirtyCM: '30 cm',
                fourtyCM: '40 cm',
                extraMenu: 'Tilbehør:',
				pizzaItemsFirst: [
					{ name: '1. VESUVIO', description: 'Tomatsaus, ost og skinke', medium: '170,-', large: '200,-', glutenfri: '200,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                    { name: '2. CARICCOSA', description: 'Tomatsaus, ost, skinke og champignon', medium: '180,-', large: '210,-', glutenfri: '210,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                    { name: '3. PORTOFINO', description: 'Tomatsaus, ost, skinke, ananas', medium: '180,-', large: '205,-', glutenfri: '205,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                    { name: '4. ROMANO', description: 'Tomatsaus, ost, biff, paprika, løk og bernaisesaus', medium: '180,-', large: '210,-', glutenfri: '210,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                    { name: '5. POSTITANA', description: 'Tomatsaus, ost, biff, paprika, løk, og champignon', medium: '180,-', large: '210,-', glutenfri: '210,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                    { name: '6. OPERA', description: 'Tomatsaus, ost, pepperoni, paprika og løk', medium: '180,-', large: '210,-', glutenfri: '210,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                    { name: '7. NAPOLITANO', description: 'Tomatsaus, ost, skinke, pepperoni og ananas', medium: '180,-', large: '210,-', glutenfri: '210,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                    { name: '8. MAMAROSA', description: 'Tomatsaus, ost, pepperoni og ananas', medium: '180,-', large: '210,-', glutenfri: '210,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                    { name: '9. FELLINI', description: 'Tomatsaus, ost, skinke, kjøttdeig og løk', medium: '180,-', large: '210,-', glutenfri: '210,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                    { name: '10. KEBABPIZZA', description: 'Tomatsaus, ost, kebabkjøtt, løk,champignon og kebabsaus', medium: '180,-', large: '210,-', glutenfri: '210,-', allergi: 'Gluten (Hvete), Egg, Melk, Soya, Selleri', },
                    { name: '11. STORKIOSKENS SPESIAL', description: 'Tomatsaus, ost, biff, bacon, paprika og løk', medium: '190,-', large: '210,-', glutenfri: '210,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                    { name: '12. HUSETS SPESIAL', description: 'Tomatsaus, ost, biff, bacon, paprika og løk', medium: '195,-', large: '230,-', glutenfri: '230,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                    { name: '13. EL TACO', description: 'Tomatsaus, ost, marinert tacokjøtt, jalapenos, mais, løk og tomatskiver', medium: '180,-', large: '210,-', glutenfri: '210,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
				],

                pizzaItemsSecond: [	
                    { name: '14. VEGETARIAN', description: 'Tomatsaus, ost, champignon, løk, mais, ananas, paprika, oliven, tomat', medium: '180,-', large: '210,-', glutenfri: '210,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                    { name: '15. LA FAVOURITA', description: 'Komponer din egen pizza med inntil 6 komponenter', medium: '220,-', large: '250,-', glutenfri: '250,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                    { name: '16. MILANO', description: 'Tomatsaus, ost, marinert biff, skinke, tomat og løk', medium: '190,-', large: '220,-', glutenfri: '220,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                    { name: '17. SICILIA', description: 'Tomatsaus, ost, marinert biff, pepperoni, oliven og løk', medium: '190,-', large: '220,-', glutenfri: '220,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                    { name: '18. PALERMO', description: 'Tomatsaus, ost, marinert kylling, paprika, løk, tomatskiver', medium: '200,-', large: '230,-', glutenfri: '230,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                    { name: '19. CARLEONE', description: 'Tomatsaus, ost, marinert biff, pepperoni, skinke, jalapenos, løk og paprika', medium: '220,-', large: '250,-', glutenfri: '250,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                    { name: '20. MARGHERITA', description: 'Tomatsaus og ost', medium: '170,-', large: '200,-', glutenfri: '200,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                    { name: '21. CALZONE', description: 'Tomatsaus, ost og skinke', medium: '170,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                    { name: '22. CALZONE', description: 'Tomatsaus, ost og pepperoni', medium: '170,-', allergi: 'Gluten (Hvete), Egg, Melk, Selleri', },
                ],

                extraMenuItems: [
                    { name: 'Ekstra kjøtt', price: '30,-' },
                    { name: 'Ekstra ost', price: '30,-' },
                    { name: 'Salsa', price: '25,-' },
                    { name: 'Dressing', price: '25,-', allergi: 'Egg, Melk, Selleri' }, 
                    { name: 'Kebabsaus', price: '25,-', allergi: 'Egg, Melk, Selleri' },    
                ]
			};
		},
    }
</script>

<style>
    .pizzaMenu {
        background: #3A3A3A;
        max-width: calc(886px + 24%);
        margin-left: auto;
        margin-right: auto;
        padding: 30px;
        color: #FBF6E5;
        display: flex;
        flex-direction: row;
        gap: 50px;
        justify-content: space-between;
        line-height: 1.15;
        font-size: .85em;
    }

    .pizzaMenu__list {
        width: 100%;
        height: 100%;
    }

    .pizzaMenu__list li {
        display: grid;
        grid-template-columns:1fr 1fr;
        padding: 20px 0;
        text-align: left;
    }

    .pizzaMenu__pizzaSize {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
    }

    .pizzaMenu__pizzaSize > div > span {
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .pizzaMenu__pizzaSize > div > span:nth-child(2) {
        /* font-size: .85em; */
        font-family: var(--second-font-family);
    }

    .pizzaMenu__pizzaName > p {
        font-family: var(--second-font-family);
        padding-bottom: 5px;
    }

    .pizzaMenu__pizzaName > p:nth-child(3) {
        color: rgb(240, 196, 179);
        font-style: italic;
    }

    .pizzaMenu__pizzaName > h3 {
        color: var(--foreground);
        /* font-size: 1em; */
    }

    .pizzaMenu__pizzaPrice {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
    }

    .pizzaMenu__pizzaPrice > span {
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 1.2em;
    }

    .pizzaMenu__list-extra {
        color: #FED08C;
    }

    .pizzaMenu__pizzaName-extra > p {
        color: rgb(240, 196, 179);
        font-style: italic;
        padding-top: 5px;
    }
    /* .pizzaMenu__list-extra > h3 {
        padding-top: 30px;
    } */

    /* small devices (mobiles, 1140px and down) */
    @media screen and (max-width: 1140px) {
        .pizzaMenu {
            font-size: .95em;
            display: flex;
            flex-direction: column;
            max-width: calc(786px + 14%);
        }	

        .pizzaMenu__pizzaSize > div > span {
            font-size: 1em;
        }

        .pizzaMenu__pizzaName > p {
            font-size: 1em;
            padding-bottom: 10px;
        }

        .pizzaMenu__list--mobile {
            position: absolute;                         /*  position: absolute helps to hide content */
            visibility: hidden;
            display: none;
            /* display: none !important; */             /*  display: none; not working here, tried with !important */
        }

        .pizzaMenu {
            gap: 0;
        }

        
    }
</style>