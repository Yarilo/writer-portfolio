<script>
import { onMount } from 'svelte';
import works from '../public/works';

let selectedWork = undefined;

onMount (() => {
    const workLink = window.location.href.split('#portfolio/')[1]
    selectedWork = works.find(work => work.href == workLink)
}) 

const onClickWork = (work) => {
    selectedWork = work;
}
</script>

<style>
    ul {
        padding: 30px;
    }

    .reader {
        width: 60%;
        max-height: 60%;
        margin-right: 144px; /* 1.5in */
        margin-left: 96px; /* 1in */
    }
    
    #back {
        text-align: left;
        margin-bottom: 20px;
    }
    
    .text {
       white-space: pre-line;
       line-height: 1.5;
       max-height: 100%;
       overflow-y: auto;
    }

</style>

{#if selectedWork}
    <h1>{selectedWork.title}</h1> <!-- Should be h2?-->
    {#if selectedWork.subtitle} 
        <h3>{selectedWork.subtitle}</h3>
    {/if}
    <div class='reader'>
        <p>
            <a href='#portfolio' id='back' on:click={() => onClickWork(undefined)}>{'< Back'}</a>
        </p>
        <div class='text'>
            {selectedWork.text}
        </div>
    </div>
{:else}
    <h2>Some of my works</h2>
    <ul>
        {#each works as work} 
        <li><a href='#portfolio/{work.href}' on:click={() => onClickWork(work)}>{work.title}</a></li>
        {/each}
    </ul>
{/if}

