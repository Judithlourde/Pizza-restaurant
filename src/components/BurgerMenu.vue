<template>
<div>
    <section class="burgerMenu">
        <ul class="burgerMenu__list">
            <div> 
                <h1>Hamburger</h1>
                <p>Serveres med brød, salat, dressing, tomat og rødløk</p>
            </div>

            <li>
                <h3></h3>

                <div>
                    <span>Ta med</span>
                    <span>Inne</span>
                </div>   
            </li>

            <li> 
                <h3>23. HAMBURGER 100g</h3>
               
                <div>
                    <span>70,-</span>
                    <span>80,-</span>
                </div>
            </li>

            <li> 
                <h3>24. Hamburger 130g</h3>

                <div>
                    <span>80,-</span>
                    <span>90,-</span>
                </div>
            </li>

            <li> 
                <h3>25. Hamburger 160g</h3>

                <div>
                    <span>90,-</span>
                    <span>100,-</span>
                </div>
            </li>

            <li> 
                <h3>26. Hamburger 190g</h3>

                <div>
                    <span>110,-</span>
                    <span>120,-</span>
                </div>
            </li>

            <li> 
                <h3>27. Hamburger 250g</h3>

                <div>
                    <span>130,-</span>
                    <span>140,-</span>
                </div>
            </li>

            <li> 
                <h3>28. Løvstekburger</h3>

                <div>
                    <span>90,-</span>
                    <span>100,-</span>
                </div>
            </li>
        </ul>

        <ul class="burgerMenu__list">
            <div> 
                <h1>HAMBURGERMENY</h1>
                <p>Serveres med brød, salat, dressing, tomat, rødløk, pommes frites og 0,5 l drikke</p>
            </div>

            <li>
                <h3></h3>

                <div>
                    <span>Ta med</span>
                    <span>Inne</span>
                </div>   
            </li>
            <li> 
                <h3>29. Hamburger 100g</h3>

                <div>
                    <span>120,-</span>
                    <span>130,-</span>
                </div>
            </li>

            <li> 
                <h3>30. Hamburger 130g</h3>

                <div>
                    <span>130,-</span>
                    <span>140,-</span>
                </div>
            </li>

            <li> 
                <h3>31. Hamburger 160g</h3>

                <div>
                    <span>140,-</span>
                    <span>150,-</span>
                </div>
            </li>

            <li> 
                <h3>32. Hamburger 190g</h3>

                <div>
                    <span>160,-</span>
                    <span>170,-</span>
                </div>
            </li>

            <li> 
                <h3>33. Hamburger 250g</h3>

                <div>
                    <span>180,-</span>
                    <span>190,-</span>
                </div>
            </li>
        </ul>
    </section> 

    <section class="burgerMenu">
        <ul class="burgerMenu__list">
            <li> 
                <h3>Tilbehør:</h3>

                <div>
                    <span>Ta med</span>
                    <span>Inne</span>
                </div>
            </li>

            <li> 
                <p>Ost</p>

                <div>
                    <span>10,-</span>
                    <span>12,-</span>
                </div>
            </li>

            <li> 
                <p>Bacon</p>

                <div>
                    <span>12,-</span>
                    <span>14,-</span>
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
</div>
</template>

<style>
    .burgerMenu {
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

    .burgerMenu__list {
        width: 100%;
        height: 100%;
        padding: 30px 0;
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
        gap: 50px;
        padding: 10px;
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
    }

    .burgerMenu__images {
        display: flex;
        gap: 10px;
        padding: 30px 0;
    }

    .burgerMenu__image {
        width: 100%;
        height: 100%;
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
    }
</style>