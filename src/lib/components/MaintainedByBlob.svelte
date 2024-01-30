<script>
	import { onMount } from 'svelte';
    import blob from '../images/svg/captioned-blob.svg'

	let blobElement;

	onMount(() => {
		animateBlob(blobElement);
	});

	function animateBlob(element) {
		let scale = 1;
		let direction = 1;

		function step() {
			scale += direction * 0.0001;
			if (scale > .9 || scale < 0.8) {
				direction *= -1;
			}
			element.style.transform = `scale(${scale})`;
			requestAnimationFrame(step);
		}

		requestAnimationFrame(step);
	}
</script>

<div class="container">
    <img bind:this={blobElement} src={blob} alt="blob" loading="lazy">
</div>
