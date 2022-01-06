<template>
    <section class="plateDishesMenu">
        <ul class="plateDishesMenu__list">
            <div> 
                <h1>TALLERKENRETTER</h1>
                <p>Serveres med salat, tomat, rødløk, mais, dressing, pommes frites, bernaise og 0,5 l drikke</p>
            </div>

            <li>
                <h3></h3>

                <div>
                    <span>Ta med</span>
                    <span>Inne</span>
                </div>   
            </li>

            <li> 
                <h3>50. Biffsnaddertallerken</h3>

                <div>
                    <span>194,-</span>
                    <span>204,-</span>
                </div>
            </li>

            <li> 
                <h3>51. Kyllingsnaddertallerken</h3>

                <div>
                    <span>194,-</span>
                    <span>204,-</span>
                </div>
            </li>

            <li> 
                <h3>52. Kyllingfiletmiddag</h3>

                <div>
                    <span>220,-</span>
                    <span>230,-</span>
                </div>
            </li>

            <li> 
                <h3>53. Løvstektallerken enkel</h3>

                <div>
                    <span>150,-</span>
                    <span>160,-</span>
                </div>
            </li>

            <li> 
                <h3>54. Løvstektallerken dobbel</h3>

                <div>
                    <span>184,-</span>
                    <span>194,-</span>
                </div>
            </li>

            <li> 
                <h3>55. Nuggetstallerken 7 biter</h3>

                <div>
                    <span>109,-</span>
                    <span>110,-</span>
                </div>
            </li>

            <li> 
                <h3>56. Nuggetstallerken 12 biter</h3>

                <div>
                    <span>149,-</span>
                    <span>159,-</span>
                </div>
            </li>
        </ul>

        <ul class="plateDishesMenu__list">
            <div> 
                <h3>DIVERSE</h3>
            </div>

            <li>
                <h3></h3>

                <div>
                    <span>Ta med</span>
                    <span>Inne</span>
                </div>   
            </li>
            <li> 
                <h3>Pommes frites liten</h3>

                <div>
                    <span>45,-</span>
                    <span>55,-</span>
                </div>
            </li>

            <li> 
                <h3>Pommes frites stor</h3>

                <div>
                    <span>55,-</span>
                    <span>65,-</span>
                </div>
            </li>

            <li> 
                <h3>Brus 0,5 l</h3>

                <div>
                    <span>35,-</span>
                    <span>38,-</span>
                </div>
            </li>

            <li> 
                <h3>Brus 1,5 l</h3>

                <div>
                    <span>55,-</span>
                    <span>60,-</span>
                </div>
            </li>
        </ul>
    </section> 

    <section class="plateDishesMenu">
        <ul class="plateDishesMenu__list">
            <div> 
                <h1>BARNEMENY</h1>
                <p>Serveres med pommes frites og Kuli</p>
            </div>

            <li> 
                <h3></h3>

                <div>
                    <span>Ta med</span>
                    <span>Inne</span>
                </div>
            </li>

            <li> 
                <h3>Grillpølse</h3>

                <div>
                    <span>80,-</span>
                    <span>90,-</span>
                </div>
            </li>

            <li> 
                <h3>Nuggets</h3>

                <div>
                    <span>80,-</span>
                    <span>90,-</span>
                </div>
            </li>
        </ul>

        <ul class="plateDishesMenu__images">
            <div class="plateDishesMenu__image">
                <img src="/images/burger.jpg" alt="burger-image">
            </div>

            <div class="plateDishesMenu__image">
                <img src="/images/burger2.jpg" alt="burger-image">
            </div>

                <div class="plateDishesMenu__image">
                <img src="/images/cola.jpg" alt="cola-image">
            </div>
        </ul>
    </section>
</template>

<style>
    .plateDishesMenu {
        background: #3A3A3A;
        max-width: calc(786px + 24%);
        margin-left: auto;
        margin-right: auto;
        padding: 10px;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: flex-start;
        font-size: .85em;
    }

    .plateDishesMenu__list {
        width: 100%;
        height: 100%;
        padding: 30px 0;
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
        gap: 50px;
        padding: 10px;
    }

    .plateDishesMenu__list > div {
        color: #FBF6E5;
    }

    .plateDishesMenu__list > li > div {
        display: grid;
        grid-template-columns: 1fr 1fr;
    }

    .plateDishesMenu__list li > div > span {
        padding: 5px;
        color: #FBF6E5;
        font-size: 1.2em;
    }

    .plateDishesMenu__images {
        display: flex;
        gap: 10px;
        padding: 40px 0;
    }

    .plateDishesMenu__image {
        width: 100%;
        height: 100%;
    }

    .plateDishesMenu__image > img {
        width: 100%;
        height: 100%;
    }

    @media screen and (max-width: 1140px) {
        .plateDishesMenu {
            font-size: 1.1em;
            max-width: calc(786px + 14%);
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        .plateDishesMenu__image {
            width: 300px;
            height: 300px;
        }
    }
</style>