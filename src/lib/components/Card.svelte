<script>
    import zarfCard from '../images/png/zarf-card.png'
    export let title1
    export let title2
    export let text
    export let img
</script>

<div class="card-container">
    <img class="card" src="{zarfCard}" alt="card" loading="lazy">
    <div class="content-container">
    <div class="img-container">
        <slot name="img"><img class="cloud" src="{img}" alt="cloud" loading="lazy"></slot>
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
    .content-container{
        padding-left: .5rem;
    }
    .card-container{
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        gap: 2rem;
        width: 286px;
        height: 360px;
    }

    .img-container{
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .cloud{
        height: auto;
        width: 84px;
    }
    .card{
        position: absolute;
        z-index: -1;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .text-container{
        display: flex;
        flex-direction: column;
        width: 260px;
        gap: 1rem;
        padding-top: 1rem;
    }
    h3{
        font-size: 24px;
    }
    p{
        font-size: 16px;
    }

</style>
