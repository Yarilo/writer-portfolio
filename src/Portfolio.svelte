<script>
// @TODO: On click work, show its text

let selectedWork = undefined;

const works = [
    {title: 'The bla & the ble 1', text:'adasdsadsd'}, 
    {title: 'The bla & the ble 2', text:'adsads'}
]

const onClickWork = (work) => {
    selectedWork = work;
}
</script>

<style>
    ul {
        padding: 30px;
    }
    a {
		color: black;
	}
    .reader {
        /* TODO */
    }

</style>
    <h3>Some of my works</h3>
    <ul>
        {#each works as work} 
        <li><a href='#portfolio' on:click={() => onClickWork(work)}>{work.title}</a></li>
        {/each}
    </ul>
    {#if selectedWork}
        <div class='reader'>{selectedWork.text}</div>
    {/if}