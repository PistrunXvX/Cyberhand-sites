<script>
		import Header from './Header.svelte';
		import Main from './Main.svelte';
		import Footer from './Footer.svelte';
</script>

<!-- <svelte:head>
	<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/5.0.0-alpha1/css/bootstrap.min.css" integrity="sha384-r4NyP46KrjDleawBgD5tp8Y7UzmLA05oM1iAEQ17CSuDqnUK2+k9luXQOfXJCJ4I" crossorigin="anonymous">
	<link href="https://fonts.googleapis.com/css2?family=Hammersmith+One&family=Open+Sans:wght@400;700&display=swap" rel="stylesheet">
</svelte:head> -->

<Header/>
<Main/>
<Footer/>


<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>