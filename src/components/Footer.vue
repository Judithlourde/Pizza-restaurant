<template>
    <hr class="footer-seperator" />

    <section class="footer">
        <ul class="footer__address">
            <li>
                <h1>Adresse</h1>
            </li>

            <li>
                <p>Nye Stasjonsvei 27,</p>
            </li>

            <li>
                <p>3430 Spikkestad, Røyken</p>
            </li>       
        </ul>

        <ul class="footer__contact">
            <li>
                <h1>Kontakt Oss</h1>
            </li>

            <li>
                <div class="footer__contact-icon">
                    <img src="/svg/email.svg" alt="email-icon">
                    <p>shahinzatgar@hotmail.com</p>
                </div>  
            </li>

            <li>
                <div class="footer__contact-icon">
                    <img src="/svg/phone.svg" alt="phone-icon">
                    <p>31 28 75 06/ 48 95 96 14</p>
                </div>
            </li>   

            <li>
                <div class="footer__contact-icon">
                    <img src="/svg/facebook.svg" alt="facebook-icon">
                    <a href="https://www.facebook.com/Spikkestad-pizza-og-grill-112698187314811/"><p>følg oss på Facebook</p></a>
                </div>
                
            </li>     
        </ul>

        <ul class="footer__openingTime">
            <li>
                <h1>Åpnings Tider</h1>
            </li>

            <li>
                <p>Mandag - Torsdag</p>
                <p>11.00 - 20.30</p>
            </li>

            <li>
                <p>Fredag - Lørdag</p>
                <p>11.00 - 22.00</p>
            </li>   

            <li>
                <p>Søndag</p>
                <p>13.00 - 22.00</p>
            </li>     
        </ul>
    </section>

    <div class="footer-bottom">
        <h1>Spikkestad Pizza og Grill AS</h1>
        <p>Designed and developed by Judith Peter</p>
    </div>   
</template>

<style>
    .footer {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        max-width: calc(786px + 24%);
        margin-left: auto;
        margin-right: auto;
        padding: 20px 0;
    }

    .footer > ul {
        width: 100%;
        height: 100%;
        padding: 0 20px;
    }

    .footer > ul > li {
        list-style: none;
    }

    .footer__address li h1 {
        padding-bottom: 10px;
    }

    .footer__address li p {
        padding: 5px 0;
    }

    .footer__contact li h1 {
        padding-bottom: 10px;
    }

    .footer__contact li div p {
        padding: 10px 0;
    }

    .footer__openingTime li {
        padding-bottom: 15px;
        text-align: center;
    }

    .footer__openingTime li p:nth-child(2) {
        color: #FBF6E5;
        font-family: var(--second-font-family);
    }

    .footer > ul > li > h1 {
        color: #FBF6E5;
    }

    .footer__contact-icon {
        display: flex;
        /* flex-direction: row;
        justify-content: center; */
    }

    .footer__contact-icon > img {
        width: 30px;
        margin: 0 10px 0 0;
    }

    .footer__contact-icon > a {
        color: var(--foreground);
    }

    .footer-bottom {
        text-align: center;
        padding: 20px 0 50px 0;
    }

    .footer-bottom h1 {
        padding: 10px 0;
    }

    .footer-bottom p {
        color: #FBF6E5;
        font-size: .75em;
    }

    .footer-seperator {
        opacity: 0.55;
        border-style: solid;
        border-bottom-width: 1px;
        border-top-width: 0;
        border-left-width: 0;
        border-right-width: 0;
        border-color: var(--foreground);
        margin: 2% 10%;
    }

    /* small devices (mobiles, 768px and down) */
    @media screen and (max-width: 1140px) {
        .footer {
            flex-direction: column;
            align-items: center;
            text-align: center;
            font-size: 2em;
        }

        .footer > ul {
            padding: 20px;
            margin: 20px;
        }

        .footer__contact-icon > img {
            width: 50px;
        }

        .footer__contact-icon {
            display: flex;
            flex-direction: row;
            justify-content: center;
            /* align-items: center; */
        }

        .footer-bottom > h1 {
            font-size: 2.5em;
        }

        .footer-bottom > p {
            font-size: .85em;
            margin-bottom: 30px;

        }
    }
</style>