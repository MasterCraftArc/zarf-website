<script>
	import blob from '../images/svg/hero-blob.svg';
	import hero from '../images/png/zarf-edge.png';
	import Button from '$lib/components/Button.svelte';
</script>

<section class="Hero">
	<div class="L-R-Container">
		<div class="left">
			<div class="text-container">
				<h1>DevSecOps for Airgap</h1>
				<p>
					A free open source tool that enables continuous software delivery on disconnected
					networks.
				</p>
				<Button text="Contact an Expert" />
			</div>

		</div>
		<div class="right"><img class="hero" src={hero} alt="hero" loading="eager"/></div>
	</div>
	<div class="blob-container">
		<img class="blob" src={blob} alt="blob" loading="eager"/>
		</div>
</section>

<style>
	.blob-container{
		z-index: -1;
		position: absolute;
		width: 100vw;
		left: -25rem;
	}
	.text-container {
		display: flex;
		align-items: flex-start;
		justify-content: flex-start;
		flex-direction: column;
		gap: 1rem;
	}
	.L-R-Container {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: center;
		position: relative;

	}
	.left,
	.right {
		width: 100%;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	.left {
		flex-direction: column;
		text-align: left;
	}

	.hero {
		width: 100%;
	}
	@media (max-width: 899px) {
		.blob-container{
			top: -52rem;
			overflow: hidden;
			left: 0;
		}
		.L-R-Container{
			flex-direction: column;
		}
    }
</style>
