# :tv:  Watchly: A Movie & TV Show App
## Created by: Tyler Ivie
### Created in Node.js, Express.js, Mongoose, MongoDB on the backend. Svelte, JS, HTML, CSS on the frontend. This app will help you browse trending movies and add them to your watchlist

[Recipe App URL](https://recipe-app-dgm3760.herokuapp.com/index.html)

----------------------------------------------------------

## :truck:  Routes
### GET
1. As a user I can see all my movies (after adding at least one movie) in my watchlist. (api/movies)
2. As a user I can see all my favorite movies. (api/favorites)
3. As a user I can see all my favorite movies. (api/movies)
4. As a user when navigated to the home screen, it is populated with currently trending movies for me to interact with. (http://localhost:5000/)
### PUT
1. As a user I can check off a movie if I have watched it (api/updateList/:id)
2. As a user I can check off a movie if I have watched it (api/updateFavList/:id)
### POST
1. As a user I can click on any trending movie and click by going to **ADD TO WATCHLIST**. This will add the following movie to my watchlist here: http://localhost:5000/watchlist. (api/addList)
2. As a user I can click on any trending movie and click by going to the **HEART ICON**. This will add the following movie to my favorites list here: http://localhost:5000/watchlist. (api/addList)
### DELETE
1. As a user I can removed a movie from my watchlist or favorites by clicking on the **TRASH ICON**. (api/deleteList/:id)