# :tv:  Watchly: A Movie & TV Show App (Frontend)
## Created by: Tyler Ivie
### Created in Node.js, Express.js, Mongoose, MongoDB on the backend. Svelte, JS, HTML, CSS on the frontend. This app will help you browse trending movies and add them to your watchlist

[Watchly App URL](https://dazzling-goldberg-74b32f.netlify.app/)

----------------------------------------------------------

## :truck:  Routes
### GET
1. As a user I can see all my movies (after adding at least one movie) in my watchlist. (api/movies)
```javascript
onMount(async () => {
    const options = {
        method: "GET",
        url: "https://watchly-app-backend.herokuapp.com/api/movies",
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
```
2. As a user I can see all my favorite movies. (api/favorites)
```javascript
onMount(async () => {
    const options = {
        method: "GET",
        url: "https://watchly-app-backend.herokuapp.com/api/favorites",
    };
    axios.request(options)
    .then((res) => {
        console.log(res)
        favorites = res.data.favorites
    })
    .catch((err) => {
        console.log(err);
    });
})
```
3. As a user I can see all my favorite movies. (api/movies)
4. As a user when navigated to the home screen, it is populated with currently trending movies for me to interact with. (https://dazzling-goldberg-74b32f.netlify.app)
### PUT
1. As a user I can check off a movie if I have watched it (api/updateList/:id)
2. As a user I can check off a movie if I have watched it (api/updateFavList/:id)
```javascript
const updateMovieToWatched = (movie) => {
    console.log(movie)
    const options = {
        method: "PUT",
        url: `https://watchly-app-backend.herokuapp.com/api/updateList/${movie._id}`,
        data: {
            watched: !movie.watched
        }
    };
    axios.request(options)
    .then((res) => {
        console.log(res)
    })
    .catch((err) => {
        console.log(err);
    });

};
const updateFavMovieToWatched = (movie) => {
    console.log(movie)
    const options = {
        method: "PUT",
        url: `https://watchly-app-backend.herokuapp.com/api/updateFavList/${movie._id}`,
        data: {
            watched: !movie.watched
        }
    };
    axios.request(options)
    .then((res) => {
        console.log(res)
    })
    .catch((err) => {
        console.log(err);
    });

};
```
### POST
1. As a user I can click on any trending movie and click by going to **ADD TO WATCHLIST**. This will add the following movie to my watchlist here (click on my Movies). (api/addList)
2. As a user I can click on any trending movie and click by going to the **HEART ICON**. This will add the following movie to my favorites list here (click on my Movies). (api/addFavorite)
```javascript
let selectedMovie;
const addToWatchList = () => {
    selectedMovie = movie;
    const options = {
        method: "POST",
        url: "https://watchly-app-backend.herokuapp.com/api/addList",
        data: {
            title: selectedMovie.title,
            img: `https://image.tmdb.org/t/p/w500${selectedMovie.poster_path}`,
            dateReleased: selectedMovie.release_date,
            watched: false
        }
    };
    axios.request(options)
    .then((res) => {
        console.log(res)
        alert(res.data.message)
        closeDialog()
    })
    .catch((err) => {
        console.log(err);
    });

};
const addToFavorites = () => {
    selectedMovie = movie;
    const options = {
        method: "POST",
        url: "https://watchly-app-backend.herokuapp.com/api/addFavorite",
        data: {
            title: selectedMovie.title,
            img: `https://image.tmdb.org/t/p/w500${selectedMovie.poster_path}`,
            dateReleased: selectedMovie.release_date,
            watched: false
        }
    };
    axios.request(options)
    .then((res) => {
        console.log(res)
        alert(res.data.message)
        closeDialog()
    })
    .catch((err) => {
        console.log(err);
    });

};
```
### DELETE
1. As a user I can removed a movie from my watchlist or favorites by clicking on the **TRASH ICON**. (api/deleteList/:id)
```javascript
const deleteWatchListMovie = (movie, index) => {
    watchList.splice(index, 1)
    watchList = watchList
    const options = {
        method: "DELETE",
        url: `https://watchly-app-backend.herokuapp.com/api/deleteList/${movie._id}`,
        data: {
            watched: !movie.watched
        }
    };
    axios.request(options)
    .then((res) => {
        console.log(res)
    })
    .catch((err) => {
        console.log(err);
    });
}
```