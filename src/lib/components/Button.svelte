<script>
	export let link = '';
	export let text = '';
	import zarf from '../images/svg/favicon.svg';
	let show = false;
</script>

<a target="_blank" href={link}>
	<button
		on:mouseenter={() => {
			show = true;
		}}
		on:mouseleave={() => {
			show = false;
		}}
	>
		<span class="text-hidden">{text}</span>
		<img src={zarf} alt="" class="image-hidden" />
	</button>
</a>

<style>
	a {
		text-decoration: none;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	button {
		padding: 15px 40px;
		background: transparent;
		border: 2px solid white;
		color: white;
		font-family: helvetica;
		font-size: 16px;
		background: 0.5s ease;
		background-color: transparent;
		position: relative;
		transition: all 0.4s cubic-bezier(0.645, 0.045, 0.355, 1);
		cursor: pointer;
		display: block;
		border-radius: 50px;
		white-space: nowrap;
		position: relative;
		overflow: hidden;
	}

	.image-hidden {
		opacity: 0;
		transform: translateX(100%);
		transition:
			opacity 0.4s cubic-bezier(0.645, 0.045, 0.355, 1),
			transform 0.4s cubic-bezier(0.645, 0.045, 0.355, 1);
		position: absolute;
		top: 30%;
		right: 10px;
		width: 20px;
		height: auto;
	}

	button:hover {
		padding: 15px 60px 15px 20px;
		background: linear-gradient(to right, #3fb4bb, #1a2883);
		color: white;
	}

	button:hover .text-hidden {
		opacity: 1;
		transform: translateX(0);
	}

	button:hover .image-hidden {
		opacity: 1;
		transform: translateX(0);
	}
</style>
