<script>
		import Header from './Header.svelte';
		import Main from './Main.svelte';
		import Footer from './Footer.svelte';
</script>

<!-- <svelte:head>
	<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/5.0.0-alpha1/css/bootstrap.min.css" integrity="sha384-r4NyP46KrjDleawBgD5tp8Y7UzmLA05oM1iAEQ17CSuDqnUK2+k9luXQOfXJCJ4I" crossorigin="anonymous">
	<link href="https://fonts.googleapis.com/css2?family=Hammersmith+One&family=Open+Sans:wght@400;700&display=swap" rel="stylesheet">
</svelte:head> -->
<canvas class="container-fluid">
	<Header/>
	<Main/>
	<Footer/>
</canvas>


<style lang="scss">
	canvas{
		background-color: #1D002B;
		width:100%;
	}
</style>