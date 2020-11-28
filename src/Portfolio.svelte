<script>
import { onMount } from 'svelte';

const works = [
    {title: 'The bla & the ble 1', text:'adasdsadsd', href:'bla_ble_1'}, 
    {title: 'The bla & the ble 2', text:'adsads', href: 'bla_ble_2'}
]

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
        /* TODO */
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

