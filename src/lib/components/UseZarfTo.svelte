<script>
	import Card from './Card.svelte';
	import wireless from '../images/png/cloud-icons/wireless-cloud.png';
	import server from '../images/png/cloud-icons/server.png';
	import webSecurity from '../images/png/cloud-icons/web-security.png';
</script>

<section class="Use-Zarf-To">
	<h1>Use Zarf To</h1>
	<div class="card-container">
		<Card
			img={webSecurity}
			title1="Securely Package"
			title2="Apps & Resources"
			text="Provides the ability to package a chunk of the internet and then securely deliver all of the files and dependencies needed to run an application in a disconnected environment.
        "
		/>
		<Card
			img={wireless}
			title1="Deploy Cloud Apps"
			title2="While Disconnected"
			text="Provides the ability to deploy apps declaratively and without internet connectivity. Opening up the door for modern cloud capabilities to be deployed in disconnected environments.
        "
		/>
		<Card
			img={server}
			title1="Easily Maintain Apps"
			title2="While Disconnected"
			text="Zarf reduces the skill and resources needed to manage and update applications in disconnected environments, ensuring no down time or data loss when updating software.
        "
		/>
	</div>
</section>

<style>
	.card-container {
		display: flex;
		align-items: center;
		justify-content: center;
		gap: 2rem;
	}
	.Use-Zarf-To {
		gap: 2rem;
	}
	h1 {
		text-align: center;
	}
	@media (max-width: 899px) {
		.card-container {
			flex-direction: column;
		}
	}
</style>
