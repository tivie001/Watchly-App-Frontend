<script>
</script>
<section class="app-nav">
    <nav class="nav-list-items">
        <ul>
            <li class="title">Watchly</li>
            <!-- <li><Link to="/">Home</Link><br /></li> -->
            <li>My Shows</li>
            <li><a href="my-movies">My Movies</a></li>
        </ul>
    </nav>

</section>
<style>
    /* ["011627","fdfffc","2ec4b6"] */
    .app-nav {
        height: 70px;
        width: 100%;
        color: #fdfffc;
        background-color: #011627;
        display: flex;
        flex-direction: row;
        justify-content: flex-start;
        font-family: Raleway;
        border-radius: 0 0 5px 5px;
        box-shadow: 0 5px 5px -2px rgba(0,0,0,.9);
    }
    .nav-list-items {
        list-style-type: none;
        text-transform: uppercase;
        font-weight: 500;
        padding: 1rem 3rem 0 0;
    }
    .nav-list-items ul {
        margin: 0;
    }
    .title {
        font-weight: bold;
        font-size: 24px;
        color: #2ec4b6;
    }
    .nav-list-items ul li {
        display: inline;
        padding: 0 20px 0 10px;
    }
    a {
        text-decoration: none;
        color: #fdfffc;
    }
</style>