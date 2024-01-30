<script>
	import MaintainedByBlob from './MaintainedByBlob.svelte';
</script>

<section class="Airplane-mode">
	<div class="text-container">
		<h1>Airplane Mode for the Cloud</h1>
		<p>
			Modern software assumes your systems have access to the internet. This may work for 99% of the
			world, but certain SECURE systems need to maintain capabilities while being disconnected from
			the internet. Zarf keeps your software running, no matter your connection status.
		</p>
	</div>
	<div class="blob-container">
		<MaintainedByBlob />
	</div>
</section>

<style>
	.blob-container {
		display: flex;
		align-items: center;
		justify-content: center;
		position: absolute;
		z-index: -2;
		overflow: hidden;
		width: 100vw;
	}

	.text-container {
		position: relative;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		text-align: center;
	}
	.Airplane-mode {
		justify-content: center;
		align-items: center;
		display: flex;
		padding: 12rem;
	}

	p {
		max-width: 760px;
	}

	@media (max-width: 899px) {
		.blob-container {
			height: 80vh;
			overflow: hidden;
		}
		h1 {
			font-size: 48px;
		}
		p {
			font-size: 16px;
		}
	}
</style>
