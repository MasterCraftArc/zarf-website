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

			<img class="blob" src={blob} alt="blob" loading="eager"/>

		</div>
		<div class="right"><img class="hero" src={hero} alt="hero" loading="eager"/></div>
	</div>
</section>

<style>
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
	.blob {
		z-index: -1;
		position: absolute;
		
	}
	.hero {
		width: 100%;
	}
	@media (max-width: 899px) {
		.blob{
			top: -40rem;

		}
		.L-R-Container{
			flex-direction: column;
		}
    }
</style>
