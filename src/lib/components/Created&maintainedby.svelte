<script>
    import maintainedBlob from '../images/svg/captioned-blob.svg'
    import duLogo from '../images/png/full-du-logo.png'
    import Button from './Button.svelte';
</script>

<section class="Created-by">

    <div class="text-container">
        <p>
            Created & Maintained by:
        </p>
        <img src="{duLogo}" alt="logo" class="dulogo">
        <p>For enterprise package support information.</p>
        <Button text="Contact an Expert"/>
    </div>
    <div class="blob-container">
    <img class="blob" src="{maintainedBlob}" alt="blob" loading="lazy">
</div>
</section>

<style>
    .blob-container{
        display: flex;
        align-items: center;
        justify-content: center;
        position: absolute;
        z-index: -2;
        overflow: hidden;
        width: 100vw;
    }

    .dulogo{
        width: 300px;
    }
    p{
        font-size: 24px;
    }

    .text-container{
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
        gap: 1rem;
    }
    .Created-by{
        justify-content: center;
        align-items: center;
        display: flex;
        padding-bottom: 10rem;
    }

    @media (max-width: 899px) {
        .blob-container{
            height: 500px;
        }
    }
</style>
