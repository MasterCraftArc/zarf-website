<script>
	import blob from '../images/svg/hero-blob.svg';
	import hero from '../images/png/zarf-edge.png';
	import Button from '$lib/components/Button.svelte';
	import Blob from './Blob.svelte';
</script>

<section class="Hero">
	<div class="L-R-Container">
		<div class="left">
			<div class="text-container">
				<div>
				<h1>DevSecOps</h1>
				<h1>for Airgap</h1>
				</div>
				<p>
					A free open source tool that enables continuous software delivery on disconnected
					networks.
				</p>
				<Button text="Contact an Expert" link="https://www.defenseunicorns.com/contactus/"/>
			</div>

		</div>
		<div class="right"><img class="hero" src={hero} alt="hero" loading="eager"/></div>
	</div>
	<div class="blob-container">
	<Blob/>
</div>
</section>

<style>
	h1{
		font-size: 96px;
	}
	.blob-container{
		z-index: -1;
		position: absolute;
		width: 100vw;
		left: -55rem;
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
		max-width: 500px;
		min-width: 350px;
	}
	@media (max-width: 899px) {
		h1{
			font-size: 60px;
		}
		.blob-container{
			top: -42rem;
			overflow: hidden;
			left: 0;
		}
		.L-R-Container{
			flex-direction: column;
		}
    }
</style>
