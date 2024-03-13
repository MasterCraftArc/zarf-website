<script>
	import { GITHUB_PROJECT_URL } from '$lib/constants';
	import zarf from '../images/svg/zarf-logo-small.svg';
	import github from '../images/svg/github-mark-white.svg';

	let scrolled = false;

	function handleScroll() {
		scrolled = window.scrollY > 0;
		if (window.scrollY == 0) {
			scrolled = false;
		}
		console.log("scrolling")
	}
</script>

<svelte:window on:scroll={handleScroll} />

<nav class:scrolled>
	<img class="logo" src={zarf} alt="zarf" />
	<div class="links">
		<a href="https://docs.zarf.dev/docs/zarf-overview" target="_blank">Docs</a>
		<a href="https://docs.zarf.dev/examples/" target="_blank">Examples</a>
		<div class="icon-container">
		<a href={GITHUB_PROJECT_URL} class="link" target="_blank"
			><img loading="lazy" class="github" src={github} alt="github_icon" /></a
		></div>

	</div>
</nav>

<style>
	.icon-container{
		border-radius: 100%;
		width: 45px;
		height: 45px;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	.icon-container:hover{
		background-color: rgba(255, 254, 254, 0.2);
	}
	.scrolled {
		backdrop-filter: blur(10px);
		transition: background-color 0.5s ease-in-out;
		box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.5);
		z-index: 100;
	}

	nav {
		position: sticky;
		top: 0;
		margin: 0 auto;
		display: flex;
		justify-content: space-between;
		align-items: center;
		width: 100%;
		height: 4rem;
		z-index: 1;
		padding-top: 0.5rem;
		padding-bottom: 0.5rem;
		background-color: #0b0e2f;
	}

	.github {
		width: 24px;
		height: 24px;
		padding: 0.75rem;
	}

	.links {
		display: flex;
		width: 240px;
		justify-content: flex-end;
		align-items: center;
		padding-right: 0.75rem;
		gap: 1.2rem;
	}

	.logo {
		height: 4rem;
		padding-left: 2rem;
	}

	a {
		color: #9f9fab;
		text-decoration: inherit;
		font-size: 1rem;
		font-family: 'Aldrich';
	}

	a:hover {
		color: white;
	}

	@media only screen and (max-width: 1200px) {
		.logo {
			height: 3rem;
		}
	}
</style>
