<script>
    
</script>


<style>
	.card-wrapper {
		grid-column: 1 / 6;
		grid-row: 1 / 7;
		border-radius: 5px;
		box-shadow: 0 5px 5px -2px rgba(0, 0, 0, 0.9);
		background-color: #262626;
        margin-bottom: 2rem;
	}
    .card-title {
        text-align: left;
        padding-left: 1rem;
        color: #fdfffc;
        font-variant: small-caps;
        font-family: Raleway;
    }
    .movie-grid {
        display: grid;
        grid-template-columns: repeat(5, 1fr);
        gap: 20px;
		grid-auto-rows: minmax(100px, auto);
        padding: 1rem
    }
    .movie-item {
        transition: .5s ease;
    }
    .movie-item:hover {
        transform: scale(1.08);
        cursor: pointer;
    }
    .movie-item small {
        color: #fdfffc;
        margin-top: 10px;
        text-transform: uppercase;
    }
    img:hover {
        background-color: aqua;
    }
    .fav {
        /* border: 3px solid #2ec4b6; */
    }
</style>