<template>
    <section class="kebabMenu">
        <ul class="kebabMenu__list">
            <div> 
                <h1>{{ kebabItemsFirstTitle }}</h1>
                <p>{{ kebabItemsFirstDescription }}</p>
                <p class="kebabMenu__list-allergi">{{ allergi }}</p>
            </div>

            <li>
                <h3></h3>

                <div>
                    <span>{{ takeAway }}</span>
                    <span>{{ dinningIn }}</span>
                </div>   
            </li>

            <li v-for="kebabItem in kebabItemsFirst" :key="kebabItem"> 
                <h3>{{ kebabItem.name }}</h3>

                <div>
                    <span>{{ kebabItem.takeAway }}</span>
                    <span>{{ kebabItem.dinningIn }}</span>
                </div>
            </li>
        </ul>

        <ul class="kebabMenu__list">
            <div> 
                <h1>{{ kebabItemsSecondTitle }}</h1>
                <p>{{ kebabItemsSecondDescription }}</p>
                <p class="kebabMenu__list-allergi">{{ allergi }}</p>
            </div>

            <li>
                <h3></h3>

                <div>
                    <span>{{ takeAway }}</span>
                    <span>{{ dinningIn }}</span>
                </div>   
            </li>
            <li v-for="kebabItem in kebabItemsSecond" :key="kebabItem"> 
                <h3>{{ kebabItem.name }}</h3>

                <div>
                    <span>{{ kebabItem.takeAway }}</span>
                    <span>{{ kebabItem.dinningIn }}</span>
                </div>
            </li>
        </ul>
    </section> 

    <section class="kebabMenu">
        <ul class="kebabMenu__list">
            <div> 
                <h1>{{ kebabItemsThirdTitle }}</h1>
                <p>{{ kebabItemsThirdDescription }}</p>
                <p class="kebabMenu__list-allergi">{{ allergi }}</p>
            </div>

            <li> 
                <h3></h3>

                <div>
                    <div class="kebabMenu__list-takeAway">
                        <span>{{ takeAway }}</span>
                        <p>{{ takeAwayPant }}</p>
                    </div>

                    <span>{{ dinningIn }}</span>
                </div>
            </li>

            <li v-for="kebabItem in kebabItemsThird" :key="kebabItem"> 
                <h3>{{ kebabItem.name }}</h3>

                <div>
                    <span>{{ kebabItem.takeAway }}</span>
                    <span>{{ kebabItem.dinningIn }}</span>
                </div>
            </li>
        </ul>

        <ul class="kebabMenu__images">
            <div class="kebabMenu__image">
                <img src="/images/burger.jpg" alt="burger-image">
            </div>

            <div class="kebabMenu__image">
                <img src="/images/burger2.jpg" alt="burger-image">
            </div>
                <div class="kebabMenu__image">
                <img src="/images/cola.jpg" alt="cola-image">
            </div>
        </ul>
    </section>
</template>

<script>
    export default {
        data() {
            return {
                kebabItemsFirstTitle: 'KEBAB I PITA',
                kebabItemsFirstDescription: 'Serveres med kjøtt, salat, tomat, rødløk, mais og dressing',
                kebabItemsSecondTitle: 'KEBABRULL',
                kebabItemsSecondDescription: 'Serveres med kjøtt, salat, tomat, rødløk, mais og dressing',
                kebabItemsThirdTitle: 'KEBABTALLERKEN',
                kebabItemsThirdDescription: 'Serveres med kjøtt, salat, tomat, rødløk, mais og dressing, pommes frites, bernaise og 0,5 l drikke',
                allergi: 'Gluten (Hvete), Egg, Melk, Soya, Selleri, Sennep',
                takeAway: 'Ta med',
                takeAwayPant: 'Pant +2Kr',
                dinningIn: 'Inne',
                kebabItemsFirst: [
                    {name: '34. Kebab i pita vanlig', takeAway: '95,-', dinningIn: '105,-'},
                    {name: '35. Kebab i pita stor', takeAway: '110,-', dinningIn: '120,-'},
                    {name: '36.Kylling i pita liten', takeAway: '110,-', dinningIn: '120,-'},
                    {name: '37. Kylling i pita stor', takeAway: '120,-', dinningIn: '130,-'},
                    {name: '38. Falafel i pita', takeAway: '85,-', dinningIn: '95,-'}
                ],

                kebabItemsSecond: [
                    {name: '39. Kebabrull vanlig', takeAway: '120,-', dinningIn: '130,-'},
                    {name: '40. Kebabrull vanlig m/ost', takeAway: '140,-', dinningIn: '150,-'},
                    {name: '41. Kebabrull kylling', takeAway: '140,-', dinningIn: '150,-'},
                    {name: '42. Kebabrull kylling m/ost', takeAway: '160,-', dinningIn: '170,-'},
                    {name: '44. Kebabrull biff m/ost', takeAway: '160,-', dinningIn: '170,-'},
                    {name: '45. Falafelrull', takeAway: '95,-', dinningIn: '105,-'},
                ],

                kebabItemsThird: [
                    {name: '46. Kebabtallerken vanlig', takeAway: '160,-', dinningIn: '170,-'},
                    {name: '47. Kebabtallerken stor', takeAway: '180,-', dinningIn: '190,-'},
                    {name: '48. Kyllingtallerken vanlig', takeAway: '170,-', dinningIn: '180,-'},
                    {name: '49. Kyllingtallerken stor', takeAway: '190,-', dinningIn: '200,-'},
                ]
            }
        }
    }
</script>

<style>
    .kebabMenu {
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

    .kebabMenu__list {
        width: 100%;
        height: 100%;
        padding: 10px;
    }

    .kebabMenu__list > div > p {
        font-family: var(--second-font-family);
    }

    .kebabMenu__list > div > h1 {
        color: var(--foreground);
    }

    .kebabMenu__list li {
        width: 100%;
        display: grid;
        grid-template-columns: 2fr 1fr;
        padding: 10px;
    }

    .kebabMenu__list-allergi {
        color: rgb(240, 196, 179);
        font-style: italic;
        padding-top: 5px;    
    }

    .kebabMenu__list > div {
        color: #FBF6E5;
    }

    .kebabMenu__list > li > div {
        display: grid;
        grid-template-columns: 1fr 1fr;
    }

    .kebabMenu__list li > div > span {
        padding: 5px;
        color: #FBF6E5;
        font-size: 1.2em;
        text-align: right;
    }

    .kebabMenu__images {
        display: flex;
        gap: 10px;
        padding: 100px 0;
    }

    .kebabMenu__list-takeAway {
        color: #FBF6E5; 
        text-align: right; 
        font-size: 1em;  
    }

    .kebabMenu__list-takeAway > p {
        padding-top: 5px;
    }

    .kebabMenu__image {
        width: 200px;
        height: 200px;
    }

    .kebabMenu__image > img {
        width: 100%;
        height: 100%;
    }

    /* small devices (mobiles, 1140px and down) */
    @media screen and (max-width: 1140px) {
        .kebabMenu {
            font-size: 1.1em;
            max-width: calc(786px + 14%);
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        .kebabMenu__image {
            width: 300px;
            height: 300px;
        }

        .kebabMenu__list li {
            width: 100%;
            display: grid;
            grid-template-columns: 1fr 1fr;
            padding: 10px;
        }
    }
</style>