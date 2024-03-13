<script>
    import Button from './Button.svelte';
    import statscard from '$lib/images/png/stats-card.png'
    import statscardsm from '$lib/images/png/stats-card-sm.png'
    import zarf from '../images/svg/favicon.svg'
    $: innerWidth = 0
</script>
<svelte:window bind:innerWidth/>
<section>
    {#if innerWidth && innerWidth >= 1045} 
    <img src="{statscard}" alt="stats-card" class="card" loading="lazy">
    {:else if innerWidth && innerWidth < 1045}
    <img src="{statscardsm}" alt="stats-card" class="card" loading="lazy">
    {/if}
    <div class="L-R-container">
        <div class="left">
            <h5>OPEN SOURCE PROJECT</h5>
            <h1>Join Our Mission</h1>
            <p>Zarf makes modern software capabilities a reality in disconnected environments. We aim to deliver secure software to the worlds most important environments.</p>
            <Button text="VIEW CONTRIBUTOR GUIDE"/>
        </div>
        <div class="right">
            {#if innerWidth && innerWidth >= 1045} 
            <div class="column1">
                <div class="text-container">
                    <h1>875</h1>
                    <h5>Stars</h5>
                </div>
                <div class="text-container">
                    <h1>1319</h1>
                    <h5>Pull Requests</h5>
                </div>
            </div>
            <div class="column2">
                <div class="text-container">
                    <h1>65</h1>
                    <h5>Contributors</h5>
                </div>
                
                <img class="zarf" src="{zarf}" alt="">
                
            </div>
            {:else}
            <div class="column1">
                <div class="text-container">
                    <h1>875</h1>
                    <h5>Stars</h5>
                </div>
                <div class="text-container">
                    <h1>65</h1>
                    <h5>Contributors</h5>
                </div>
                <div class="text-container">
                    <h1>1319</h1>
                    <h5>Pull Requests</h5>
                </div>
                
            </div>
            {/if}
        </div>
    </div>
</section>

<style>
    .zarf{
        width: 200px;
    }
    .column1,.column2{
        display: flex;
        flex-direction: row;
        justify-content: flex-start;
        align-items: flex-start;
        gap: 3rem;
    }



    .text-container{
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
    }
    h5{
        font-size: 20px;
    }
    p{
        font-size: 16px;
    }
    .card{
        width: 100%;
    }
    .L-R-container{
        position: absolute;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 2rem;
        width: 80%;
        max-width: 1600px;
    }
    .left,.right{
        width: 50%;
    }
    .left{
        display: flex;
        align-items: flex-start;
        text-align: start;
        flex-direction: column;
        gap: 1rem;
    }
    .right{
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: start;
        flex-direction: column;
        gap: 1rem;
    }

    section{
        padding-bottom: 6rem;
    }

@media (max-width: 1045px) {
	.L-R-container{
        flex-direction: column;
    
    }
    .left{
        padding-top: 3rem;
    }
    .card{
        max-width: 450px;
        max-height: 900px;
    }
    section{
        padding: 4rem 0rem;
        justify-content: flex-start;
    }
    .column1{
        flex-direction: column;
        align-items: center;
    }
    .L-R-container{
        width: 100%;
    }
    .left,.right{
        width: 100%;
        max-width: 350px;
    }
}

</style>
