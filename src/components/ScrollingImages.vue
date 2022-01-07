<template>
    <div class="marquee">
        <ul class="marquee-content">
            <li v-for="image in images" :key="image">
                <img class="slideshow__img" :src="image.file" :alt="image.caption">
            </li>

            <li v-for="image in images" :key="image">
                <img class="slideshow__img" :src="image.file" :alt="image.caption">
            </li>
        </ul>
    </div>
</template>

<script>
export default {
		data() {
			return {
				index: 0,
				showCaption: true, 
				images: [
					{ title: 'Pizza', caption: 'Pizza', file: '/images/img1.jpeg' },
					{ title: 'Noodle', caption: 'Noodle', file: '/images/img2.jpeg' },
					{ title: 'Pizza', caption: 'Pizza', file: '/images/img3.jpeg' },
					{ title: 'Pizza', caption: 'Pizza', file: '/images/img4.jpg' },
                    { title: 'Pizza', caption: 'Pizza', file: '/images/img5.jpeg' },
                    { title: 'Pizza', caption: 'Pizza', file: '/images/img6.jpeg' },
                    { title: 'Pizza', caption: 'Pizza', file: '/images/img7.jpeg' },
                    { title: 'Pizza', caption: 'Pizza', file: '/images/img8.jpeg' },
                    { title: 'Pizza', caption: 'Pizza', file: '/images/img9.jpeg' },

				],  
			};
		},
}
</script>

<style>
    :root {
        --marquee-width: 80vw;
        --marquee-height: 30vh;
        --marquee-elements: 9;
        --marquee-elements-displayed: 3;
        --marquee-element-width: calc(var(--marquee-width) / var(--marquee-elements-displayed));
        --marquee-animation-duration: calc(var(--marquee-elements) * 4s);
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
        width: 1rem;
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

    .marquee-content li {
        display: flex;
        justify-content: center;
        align-items: center;
        width: var(--marquee-element-width);
        flex-shrink: 0;
        /* font-size: calc(var(--marquee-height) * 2 / 3); */
        white-space: nowrap;
        margin: 20px;
        width: 300px;
    }

    .marquee-content > li > img {
        width: 100%;
        border: 2px solid  #FBF6E5;
    }

    /* small devices (mobiles, 768px and down) */
    @media screen and (max-width: 1100px) {
        .marquee { font-size: 12px; }
        :root {
            --marquee-width: 100vw;
            --marquee-height: 16vh;
            --marquee-element-displayed: 3;
        }

        .marquee:before, .marquee:after {
            width: 5rem;
        }

        .marquee-content li {
            width: 500px;
        }
    }
</style>