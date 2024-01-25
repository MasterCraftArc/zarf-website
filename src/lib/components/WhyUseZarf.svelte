<script>
    import NoBackgroundCard from "./NoBackgroundCard.svelte";
    import community from '../images/png/cloud-icons/community.png'
    import shield from '../images/png/cloud-icons/cloud-security.png'
    import puzzle from '../images/png/cloud-icons/pieces.png'
    import document from '../images/png/cloud-icons/document.png'
    import hosting from '../images/png/cloud-icons/hosting.png'
</script>

<section>
    <h1>Why Use Zarf</h1>
<div class="card-container">
    <NoBackgroundCard
    img="{community}"
    title1="Free and Open"
    title2="Source Solution
    "
    text="Source code is open and viewable to the public which increases security through transparency. Zarf is also a free tool and available for public use."
    />
    <NoBackgroundCard
    img="{shield}"
    title1="Built to Be"
    title2="Distro
    Agnostic"
    text="Currently offers fully automated support for K3s, K3d, and Kind. Is also compatible with EKS, AKS, GKE, RKE2 and many others distro services.

    "
    />
    <NoBackgroundCard
    img="{puzzle}"
    title1="Automates"
    title2="SBOM Creation"
    text="Automatically generates an SBOM from the images listed within a package, in compliance with federal mandate. Includes a UI for SBOM viewing.

    "
    />
</div>

<div class="card-container">
    <NoBackgroundCard
    img="{document}"
    title1="Installs Packages"
    title2="with Two Commands"
    text="Reduces the risk of installation error and complexity of installation procedures by simplifying the installation of packages to just two steps."
    />
    <NoBackgroundCard
    img="{hosting}"
    title1="Consistently Deploy"
    title2="Across Environments"
    text="Ensures that applications are deployed the same way each time, whether deployed to a different cluster, machine or environment."
    />
    <NoBackgroundCard
    img="{document}"
    title1="Host Registry"
    title2="& Git Server"
    text="Zarf spins up K8 clusters, docker registries and git servers offline to allow for disconnected use. For connected users this provides a fail over solution."
    />
</div>
</section>

<style>
    .card-container{
        display: flex;
        gap: 2rem;
    }
    @media (max-width: 899px) {
        .card-container{
            flex-direction: column;
        }
    }
</style>
