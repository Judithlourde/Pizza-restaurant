<template>
	<div class="slideshow">
		<div class="slideshow__buttons">
			<button @click="previousImage" class="slideshow__button" aria-label="previous button">
				<img src="/svg/previous.svg" alt="previous button"/>
			</button>

			<button @click="nextImage" class="slideshow__button" aria-label="next button">
				<img src="/svg/next.svg" alt="next button"/>
			</button>
		</div>

		<div class="slideshow__slides">
			<figure class="slideshow__slide">
				<img class="slideshow__img" :src="currentSlide.file" :alt="currentSlide.title">

				<figcaption v-if="showCaption" class="slideshow__caption">{{ currentSlide.caption }}</figcaption>
			</figure>
		</div>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				index: 0, 
				showCaption: true,
				slides: [
					{ title: 'Pizza', caption: 'Pizza', file:  '/images/img1.jpeg' },
					{ title: 'Noodle', caption: 'Noodle', file:  '/images/img2.jpeg' },
					{ title: 'Pizza', caption: 'Pizza', file:  '/images/img3.jpeg' },
					{ title: 'Pizza', caption: 'Pizza', file:  '/images/img4.jpg' },
					
				],
			};
		},
		
		computed: {
			currentSlide() {
				return this.slides[this.index];
			}
		},
		
		methods: {
			previousImage() {
				this.index = (this.index === 0) ? this.slides.length - 1 : this.index - 1;
			},

			nextImage() {
				this.index = (this.index === this.slides.length - 1) ? 0 : this.index + 1;
			},

			goToIndex(index) {
				this.index = index; 
			}
		}
	}
</script>

<style>
    .slideshow {
		max-width: calc(486px + 14%);
		position: relative;
		padding: 10px;
		margin-right: auto;
        margin-left: auto;
		width: 100%;
	}

	.slideshow__slides {
		width: 100%;
	}

	.slideshow__img {
		object-fit: cover;
		min-width: 100%;
	}

	.slideshow__caption {
		display: none;
		position: absolute;
		left: 0;
		bottom: 0;
		width: 100%;
		text-align: center;
		font-size: 1em;
		padding: 0.5em;
	}

	.slideshow__buttons {
		position: absolute;
        padding: 1.5em;
		top: 0;
		left: 0;
		min-width: 100%;
		height: 100%;
		z-index: 10;
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	.slideshow__button {
		height: 100%;
		padding: 0.5em;
		align-self: center;
		background: none;
		border: none;
	}

	/* Medium devices (landscape tablets, 768px and up) */
    @media screen and (min-width: 768px) {
		.slideshow {
			min-width: calc(786px + 14%);
			margin-right: auto;
			margin-left: auto;
		}	
	}
</style>
    