<script>
    import Header from './Header.svelte';
    import Main from './Main.svelte';
    import Footer from './Footer.svelte';
    import { draw } from 'svelte/transition';
    import { quintOut } from 'svelte/easing';
    let condition = false;
    setTimeout(() => condition = true);
</script>

<div class="container-fluid animation_block">
	<div class="purple_line">
		<svg>
			{#if condition}
			<path 
				in:draw="{{delay: 400, duration: 2000, easing: quintOut}}"
				d="M 0 0 L 5 140"
				style="stroke: #700151; stroke-width: 5;" 
			/>
			<path 
				in:draw="{{delay: 2200, duration: 2000, easing: quintOut}}"
				d="M 5 140 L 138 100"
				style="stroke: #700151; stroke-width: 5;" 
			/>
		{/if}
		</svg>
	</div>
	<div class="draw_line">
		<svg>
			{#if condition}
			<path 
				in:draw="{{delay: 1000, duration: 2000, easing: quintOut}}"
				d="M 0 0 L 250 100"
				style="stroke:#F2AE00; stroke-width: 5;" 
			/>
		{/if}
		</svg>
	</div>
	<Header/>
	<div class="draw_line__2">
		<svg>
			{#if condition}
			<path 
				in:draw="{{delay: 1000, duration: 2000, easing: quintOut}}"
				d="M 1 1 L 250 100"
				style="stroke:#F2AE00; stroke-width: 5;" 
			/>
			<path
				in:draw="{{delay: 3000, duration: 2000, easing: quintOut}}"
				d="M 250 100 L 0 100"
				style="stroke:#F2AE00; stroke-width: 5;" 
			/>
		{/if}
		</svg>
	</div>
	<Main/>
</div>
<Footer/>


<style lang="scss">
	@import 'style/resize.scss';

	.animation_block {
		background-color: #1D002B;
	}

	.purple_line{
		position: absolute;
		left: 30%;
	}
	.draw_line{
		position: absolute;
		left: 1%;
		top: 30%;
	}

	.draw_line__2{
		position: absolute;
		right: 1%;
		top: 100%;
	}
</style>