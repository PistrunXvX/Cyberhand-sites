<script>
	import { Router, Route, Link } from "svelte-routing";
	import Home from "./Components/Home.svelte";
	import About from "./Components/About.svelte";
	import Portfolio from "./Components/Portfolio.svelte";
	import Prices from "./Components/Prices.svelte";
	import Header from './Components/Header.svelte';
	import Footer from './Components/Footer.svelte';
	import Form from './Components/Form.svelte';
	export let url = "";

	// import { spring } from 'svelte/motion';

	// let coords = spring({ x: 50, y: 50 }, {
	// 	stiffness: 0.1,
	// 	damping: 0.25
	// });

	// let size = spring(10);
  </script>

<!-- <svg
on:mousemove="{e => coords.set({ x: e.offsetX, y: e.offsetY })}"
on:mousedown="{() => size.set(30)}"
on:mouseup="{() => size.set(10)}"
>
<circle cx={$coords.x} cy={$coords.y} r={$size}/>
</svg> -->

<Router url="{url}">
	 <div>
	   <Route path="/"><Home /></Route>
	   <Route path="/portfolio">
			<Header />
			<Portfolio />
			<Form />
			<Footer />
		</Route> 
		<Route path="/about_us">
			<Header />
			<About />
			<Footer />			
	   </Route>
	   <Route path="/price">
			<Header />
			<Prices />
			<Footer />			
   		</Route>
	 </div>
   </Router>

<style>
	/* svg { 
		width: 100%;
		height: 200%;
		position: absolute;
		z-index: 10;
	}
	circle { fill: #ff3e00 } */
</style>