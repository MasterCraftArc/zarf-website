<script>
	import { onMount } from 'svelte';
	import blob from '../images/svg/hero-blob.svg';
	let blobElement;
	onMount(() => {
		animateBlob(blobElement);
	});
	function animateBlob(element) {
		let scale = 1;
		let direction = 1;
		function step() {
			scale += direction * 0.0001;
			if (scale > 1 || scale < 0.9) {
				direction *= -1;
			}
			element.style.transform = `scale(${scale})`;
			requestAnimationFrame(step);
		}
		requestAnimationFrame(step);
	}
</script>
<section class="blob-section">
<div class="container">
	<img bind:this={blobElement} src={blob} alt="blob" loading="eager" />
</div>
</section>
<style>
.blob-section{
	max-width: 1990px;
	width: 100%;
	overflow: hidden;
	position: absolute;
	padding: 0;
}
.container {
		position: relative;
		z-index: -1;
		width: 100%;
		left: -65rem;
		top: -15rem;
		
	}
	@media (max-width: 899px) {
		.container{
			top: -40rem;
		}
		.blob-section{
			width: 100%;
		}
}
</style>