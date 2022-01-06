<template>
    <section class="kebabMenu">
        <ul class="kebabMenu__list">
            <div> 
                <h1>KEBAB I PITA</h1>
                <p>Serveres med kjøtt, salat, tomat, rødløk, mais og dressing</p>
            </div>

            <li>
                <h3></h3>

                <div>
                    <span>Ta med</span>
                    <span>Inne</span>
                </div>   
            </li>

            <li> 
                <h3>34. Kebab i pita vanlig</h3>

                <div>
                    <span>95,-</span>
                    <span>105,-</span>
                </div>
            </li>

            <li> 
                <h3>35. Kebab i pita stor</h3>

                <div>
                    <span>110,-</span>
                    <span>120,-</span>
                </div>
            </li>

            <li> 
                <h3>36.Kylling i pita liten</h3>

                <div>
                    <span>110,-</span>
                    <span>120,-</span>
                </div>
            </li>

            <li> 
                <h3>37. Kylling i pita stor</h3>

                <div>
                    <span>120,-</span>
                    <span>130,-</span>
                </div>
            </li>

            <li> 
                <h3>38. Falafel i pita</h3>

                <div>
                    <span>85,-</span>
                    <span>95,-</span>
                </div>
            </li>
        </ul>

        <ul class="kebabMenu__list">
            <div> 
                <h1>KEBABRULL</h1>
                <p>Serveres med kjøtt, salat, tomat, rødløk, mais og dressing</p>
            </div>

            <li>
                <h3></h3>

                <div>
                    <span>Ta med</span>
                    <span>Inne</span>
                </div>   
            </li>
            <li> 
                <h3>39. Kebabrull vanlig</h3>

                <div>
                    <span>120,-</span>
                    <span>130,-</span>
                </div>
            </li>

            <li> 
                <h3>40. Kebabrull vanlig m/ost</h3>

                <div>
                    <span>140,-</span>
                    <span>150,-</span>
                </div>
            </li>

            <li> 
                <h3>41. Kebabrull kylling</h3>

                <div>
                    <span>140,-</span>
                    <span>150,-</span>
                </div>
            </li>

            <li> 
                <h3>42. Kebabrull kylling m/ost</h3>

                <div>
                    <span>160,-</span>
                    <span>170,-</span>
                </div>
            </li>

            <li> 
                <h3>43. Kebabrull biff</h3>

                <div>
                    <span>140,-</span>
                    <span>150,-</span>
                </div>
            </li>

            <li> 
                <h3>44. Kebabrull biff m/ost</h3>

                <div>
                    <span>160,-</span>
                    <span>170,-</span>
                </div>
            </li>

            <li> 
                <h3>45. Falafelrull</h3>

                <div>
                    <span>95,-</span>
                    <span>105,-</span>
                </div>
            </li>
        </ul>
    </section> 

    <section class="kebabMenu">
        <ul class="kebabMenu__list">
            <div> 
                <h1>KEBABTALLERKEN</h1>
                <p>Serveres med kjøtt, salat, tomat, rødløk, mais og dressing, pommes frites, bernaise og 0,5 l drikke</p>
            </div>

            <li> 
                <h3></h3>

                <div>
                    <span>Ta med</span>
                    <span>Inne</span>
                </div>
            </li>

            <li> 
                <h3>46. Kebabtallerken vanlig</h3>

                <div>
                    <span>160,-</span>
                    <span>170,-</span>
                </div>
            </li>

            <li> 
                <h3>47. Kebabtallerken stor</h3>
                
                <div>
                    <span>180,-</span>
                    <span>190,-</span>
                </div>
            </li>

            <li> 
                <h3>48. Kyllingtallerken vanlig</h3>

                <div>
                    <span>170,-</span>
                    <span>180,-</span>
                </div>
            </li>

            <li> 
                <h3>49. Kyllingtallerken stor</h3>

                <div>
                    <span>190,-</span>
                    <span>200,-</span>
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

<style>
    .kebabMenu {
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

    .kebabMenu__list {
        width: 100%;
        height: 100%;
        padding: 30px 0;
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
        gap: 50px;
        padding: 10px;
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

    .kebabMenu__image {
        width: 100%;
        height: 100%;
    }

    .kebabMenu__image > img {
        width: 100%;
        height: 100%;
    }

    /* small devices (mobiles, 768px and down) */
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
    }
</style>