<script>
	import zarf from '../images/svg/favicon.svg';
	import github from '../images/svg/github-mark-white.svg';
	import slack from '../images/svg/slack.svg';
</script>

<footer>
	<img src={zarf} class="zarf" alt="zarf" loading="lazy" />
	<div class="icon-container">
		<img src={github} class="github" alt="github" loading="lazy" />
		<img src={slack} class="slack" alt="slack" loading="lazy" />
	</div>
	<p>Copyright © 2022 Zarf Project. All rights reserved</p>
</footer>

<style>
	.zarf {
		width: 100px;
	}
	.github,
	.slack {
		width: 24px;
	}
	footer {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		gap: 2rem;
	}
	.icon-container {
		display: flex;
		gap: 1rem;
	}
	p {
		font-size: 12px;
	}
</style>
