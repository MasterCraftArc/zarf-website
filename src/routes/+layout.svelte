<script>
	import '@fontsource/roboto';
	import '@fontsource/aldrich';
	import '../reset.css';
	import '../app.css';
	import zarf from '$lib/images/svg/zarf-logo-animated.svg';
	import Navbar from '$lib/components/Navbar.svelte';
	import Footer from '$lib/components/Footer.svelte';
</script>

<svelte:head>
	<link rel="icon" type="image/x-icon" href={zarf} />
	<title>Zarf</title>
</svelte:head>

<main>
<Navbar />
<div class="content">
<slot />
<Footer />
</div>
</main>