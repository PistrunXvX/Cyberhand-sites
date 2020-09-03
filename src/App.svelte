<script>
		import Header from './Header.svelte';
		import Main from './Main.svelte';
		import Footer from './Footer.svelte';
</script>

<!-- <svelte:head>
	<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/5.0.0-alpha1/css/bootstrap.min.css" integrity="sha384-r4NyP46KrjDleawBgD5tp8Y7UzmLA05oM1iAEQ17CSuDqnUK2+k9luXQOfXJCJ4I" crossorigin="anonymous">
	<link href="https://fonts.googleapis.com/css2?family=Hammersmith+One&family=Open+Sans:wght@400;700&display=swap" rel="stylesheet">
</svelte:head> -->
<div class="container-fluid animation_block">
	<Header/>
	<Main/>
</div>
<Footer/>


<style lang="scss">
	.animation_block{
		background-color: #1D002B;
		background-image: 
						url("/img/logo.svg"),
						url("/img/line-purple-1.svg");
		background-position: 50% 50%, 15% 0%;
		background-repeat: no-repeat;
	}
</style>