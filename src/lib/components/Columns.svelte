<script>
	import rocket from '../images/png/zarf-rocket.png';
	import submarine from '../images/png/zarf-sub.png';
	import nuclear from '../images/png/zarf-nuclear.png';
	$: innerWidth = 0
</script>
<svelte:window bind:innerWidth/>
<section class="columns">
	<div class="L-R-Container">
		<div class="left">
			<div class="text-container">
				<h3>Sometimes Disconnected</h3>
				<p>
					Some systems experience disconnection occasionally due to temporary loss of access, like a
					rocket going around the moon. Zarf keeps those systems running.
				</p>
			</div>
		</div>
		<div class="right">
			<img src={rocket} alt="rocket" loading="lazy" />
		</div>
	</div>
	<div class="L-R-Container">
		<div class="left">
			{#if innerWidth && innerWidth > 899}
			<img src={submarine} alt="submarine" loading="lazy" />
			{:else}
			<div class="text-container">
				<h3>Always Disconnected</h3>
				<p>
					Other systems are always disconnected due to lack of internet access. Maybe they are
					underground, underwater, or on another planet.
				</p>
			</div>
			{/if}
		</div>
		<div class="right">
			{#if innerWidth && innerWidth > 899}
			<div class="text-container">
				<h3>Always Disconnected</h3>
				<p>
					Other systems are always disconnected due to lack of internet access. Maybe they are
					underground, underwater, or on another planet.
				</p>
			</div>
			{:else}
			<img src={submarine} alt="submarine" loading="lazy" />
			{/if}
		</div>
	</div>
	<div class="L-R-Container">
		<div class="left">
			<div class="text-container">
				<h3>Disconnected in Emergencies</h3>
				<p>
					The worlds most important infrastructure needs to be able to control their connection to
					the internet and still run in the case of internet loss or a cyber attack.
				</p>
			</div>
		</div>
		<div class="right">
			<img src={nuclear} alt="nuclear" loading="lazy" />
		</div>
	</div>
</section>

<style>
	.columns {
		display: flex;
		align-items: center;
		justify-content: center;
		padding-left: 5rem;
		padding-right: 5rem;
	}
	.text-container {
		display: flex;
		flex-direction: column;
		gap: 2rem;
		background-color: #0b0e2f;
	}
	h3 {
		font-size: 48px;
	}
	.L-R-Container {
		display: flex;
		width: 100%;
		align-items: center;
		justify-content: center;
		max-width: 1990px;
	}
	.left,
	.right {
		width: 50%;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	img {
		max-width: 500px;
	}
	@media (max-width: 899px) {
		.L-R-Container {
			flex-direction: column;
		}
		.columns {
			gap: 5rem;
		}
		img {
			width: 350px;
		}
	}
</style>
