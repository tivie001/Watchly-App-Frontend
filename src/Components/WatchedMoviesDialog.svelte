<script>
    export let movie;
    import axios from "axios";
    let watchList;

    let selectedMovie;
    onMount(async () => {
        const options = {
			method: "GET",
			url: "http://localhost:3000/api/movies",
		};
		axios.request(options)
		.then((res) => {
            console.log(res)
            watchList = res.data.watchList
		})
		.catch((err) => {
			console.log(err);
		});
    })
</script>
<section class="dialog-container">
    {#each watchList as movie}
        <h1>{movie.title}</h1>
    {/each}
</section>
<style>
    .dialog-container {
        display: flex;
        justify-content: flex-start;
    }
</style>