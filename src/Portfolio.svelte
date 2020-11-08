<script>
// @TODO: On click work, show its text
const works = [
    {title: 'The bla & the ble 1'}, 
    {title: 'The bla & the ble 2'}
]
</script>

<style>
    ul {
        padding: 30px;
    }
</style>
    <h3>Some of my works</h3>
    <ul>
        {#each works as work} 
        <li>{work.title}</li>
        {/each}
    </ul>
