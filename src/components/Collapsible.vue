<template>
	<div class="collapsible">
        <div class="collapsible__top">
			<h1 @click="showComponent" :class="`collapsible__title ${ !this.collapsed ? 'collapsible__title--rotated' : ''}`" aria-label="collapsible button">{{ title }}</h1>

			<button @click="showComponent" :class="`collapsible__button ${ !this.collapsed ? 'collapsible__button--rotated' : ''}`" aria-label="collapsible button">		<!-- change styling if not collapsed -->
				<img src="/svg/downArrow.svg" alt="down arrow"/>
			</button>
        </div>

		<div class="collapsible__component" v-if="!this.collapsed">		<!-- view components -->
			<slot />													<!-- placeholder for components (data) -->
		</div>

		<hr class="collapsible__seperator" /> 
	</div>
</template>

<script>
	export default {
		props: {
            title: {			/* Title as prop so give them component name in Collapsible.vue */
                type: String	
			}
		},
		
		data() {
			return {
				collapsed: true
			};
		},

		methods: {
			showComponent() {
				this.collapsed = !this.collapsed
			}
		}
	};
</script>

<style>
	.collapsible {
		width: 100%;
	}

	.collapsible__seperator {
		opacity: 0.33;
		border-style: solid;
		border-bottom-width: 1px;
		border-top-width: 0;
		border-left-width: 0;
		border-right-width: 0;
		border-color: var(--foreground);
    	margin: 1% 10%;
	}

    .collapsible__top {
		width: 100%;
        display: flex;
		flex-direction: row;
		justify-content: center;
        align-items: center;
		padding: 18px;
		gap: 20px;
    }

    .collapsible__button {
        background: none;
        border: none;
        padding: 1em 0;
        cursor: pointer;	
    }

    .collapsible__button--rotated {
        transform: rotate(180deg);
    }

    .collapsible__title {
		display: flex;
		justify-content: center;
		text-align: center;
		font-size: 1.5em;
		cursor: pointer;
    }

	.collapsible__title--rotated {
		color: #FBF6E5;
	}

	.collapsible__component { 
		padding: 0 0 30px 0;
	}
	
	/* small devices (mobiles, 768px and down) */
	@media screen and (max-width: 1140px) {
		.collapsible__component {
			font-size: 1.5em;
		}	

		.collapsible__title {
			font-size: 2.75em;
		}
	}
</style>
	