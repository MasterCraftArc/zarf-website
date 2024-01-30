<script>
	export let title1;
	export let title2;
	export let text;
	export let img;
</script>

<div class="card-container">
	<div class="content-container">
		<div class="img-container">
			<slot name="img"><img class="cloud" src={img} alt="cloud" loading="lazy" /></slot>
		</div>
		<div class="text-container">
			<slot>
				<div>
					<h3>{title1}</h3>
					<h3>{title2}</h3>
				</div>
			</slot>
			<slot>
				<p>{text}</p>
			</slot>
		</div>
	</div>
</div>

<style>
	.content-container {
		padding-left: 0.5rem;
	}
	.card-container {
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
		gap: 2rem;
		width: 286px;
		height: 360px;
	}

	.img-container {
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.cloud {
		height: auto;
		width: 84px;
	}

	.text-container {
		display: flex;
		flex-direction: column;
		text-align: center;
		width: 260px;
		gap: 1rem;
		padding-top: 1rem;
	}
	h3 {
		font-size: 24px;
	}
	p {
		font-size: 16px;
	}
</style>
