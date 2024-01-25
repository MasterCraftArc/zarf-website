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
    <img class="blob" src="{maintainedBlob}" alt="blob" loading="lazy">
</section>

<style>
    .dulogo{
        width: 400px;
    }
    p{
        font-size: 24px;
    }
    .blob{
        position: absolute;
        z-index: -2;
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
        .blob{
            height: 500px;
        }
    }
</style>
