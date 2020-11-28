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
        /* @TODO: Add overflow and so on */
       white-space: pre-wrap;
    }

</style>

{#if selectedWork}
    <a href='#portfolio'  on:click={() => onClickWork(undefined)}>Back</a>
    <h1>{selectedWork.title}</h1>
    <div class='reader'>{selectedWork.text}</div>
{:else}
    <h3>Some of my works</h3>
    <ul>
        {#each works as work} 
        <li><a href='#portfolio/{work.href}' on:click={() => onClickWork(work)}>{work.title}</a></li>
        {/each}
    </ul>
{/if}

