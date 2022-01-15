<template>
    <div class="marquee">
        <div class="marquee-content">
            <figure v-for="image in images" :key="image">
                <img class="slideshow__img" :src="image.file" :alt="image.caption">
                
                <figcaption v-if="showCaption">{{ image.caption }}</figcaption>  
            </figure>
             
            <figure v-for="image in images" :key="image">
                <img v-if="index >= 2" class="slideshow__img" :src="image.file" :alt="image.caption">

                <figcaption v-if="showCaption">{{ image.caption }}</figcaption>  
            </figure>
        </div>
    </div>
</template>

<script>
export default {
		data() {
			return {
				index: 4,
				showCaption: false, 
				images: [ { title: 'Pizza', caption: 'Pizza', file: '/images/img1.jpeg' }, { title: 'Noodle', caption: 'Nudler', file: '/images/img2.jpeg' }, { title: 'Pizza', caption: 'Pizza', file: '/images/img3.jpeg' }, { title: 'Pizza', caption: 'Pizza', file: '/images/img4.jpg' }, { title: 'Pizza', caption: 'Italiensk Pizza', file: '/images/img5.jpeg' }, { title: 'Pizza', caption: 'Wok', file: '/images/img6.jpeg' }, { title: 'Pizza', caption: 'Wok', file: '/images/img7.jpeg' }, { title: 'Pizza', caption: 'Wok', file: '/images/img8.jpeg' }, ],  
			};
		},
}
</script>

<style>
    :root {
        --marquee-width: 80vw;
        --marquee-height: 30vh;
        --marquee-elements: 8;
        --marquee-elements-displayed: 3;
        --marquee-element-width: calc(var(--marquee-width) / var(--marquee-elements-displayed));
        --marquee-animation-duration: calc(var(--marquee-elements) * 3s);
    }

    .marquee {
        margin: 30px 0;
        min-width: var(--marquee-width);
        height: var(--marquee-height);
        overflow: hidden;
        position: relative;
    }

    .marquee:before, .marquee:after {
        position: absolute;
        top: 0;
        width: 12rem;
        height: 100%;
        content: "";
        z-index: 1;
    }

    .marquee:before {
        left: 0;
        background: linear-gradient(to right, #242422 0%, transparent 100%);
    }

    .marquee:after {
        right: 0;
        background: linear-gradient(to left, #242422 0%, transparent 100%);
    }

    .marquee-content {
        width: 100%;
        height: 100%;
        list-style: none;
        display: flex;
        animation: scrolling var(--marquee-animation-duration) linear infinite;
    }

    @keyframes scrolling {
        0% { transform: translateX(0); }
        100% { transform: translateX(calc(-1 * var(--marquee-element-width) * var(--marquee-elements))); }
    }

    .marquee-content:hover {
        animation-play-state: paused;
    }

    .marquee-content figure {
        display: flex;
        justify-content: center;
        align-items: center;
        width: var(--marquee-element-width);
        flex-shrink: 0;
        white-space: nowrap;
        margin: 20px;
        position: relative;
    }

    .marquee-content figcaption {
        position: absolute;
        bottom: 0;
    }

    .marquee-content > figure > img {
        min-width: 100%;
        min-height: 100%;
        object-fit: cover;
        border: .5px solid  #FBF6E5;
    }

    /* small devices (mobiles, 1140px and down) */
    @media screen and (max-width: 1140px) {
        :root {
            --marquee-width: 100%;
            --marquee-height: 20vh;
            --marquee-element-displayed: 2;
        }

        .marquee:before, .marquee:after {
            width: 7rem;
        }

        .marquee-content figure {
            width: 500px;
        }
    }
</style>