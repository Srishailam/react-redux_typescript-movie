# Luxe Software - FE Take Home Assignment
(This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app))

## Project
We will build a simple React + Typescript App in which we will:
1. Fetch a list of movies from a provided API, and apply a typescript type to it
2. Display the list of Movies return by the API as a React Component (Page 1)
3. Add a button for the users to add a movie to their Wishlist in the state, and display their Wishlist movies as a React Component (Page 2)
4. Create a basic Navbar to link between both the Pages

## Using this Repo
### Running the App

In the project directory, you can run:

`yarn start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### Running Linter

`yarn lint` 

Run this and ensure there are not linting errors before submitting the pull request

## Github Usage & How to Submit your take home assessment
1. Clone the repository to your local machine by using `git clone <git_repo_path_from_git_hub>` in your terminal
2. Next create a new branch in your terminal with `git checkout -b <your_name>_take_home_submission`
3. After making the code changes + testing them, commit your changes using `git add . && git commit -m "Take home assignment submission"`
4. Next push your changes to Github using `git push origin <your_name>_take_home_submission`
5. [Optional] on Github UI create a pull request between main branch and your branch
6. [Optional] Send a reply to the email that you used to schedule accessing this repo
7. We will follow up within 2 days after this for the next steps!

## Tasks

### Task 1 - Typescript + API integration Skills
You will be integrating with a REST API that returns a list of movies.
`https://apimocha.com/luxe-software-fe/get_movies` is a GET URL that will return a json object which is a list of Movies data

1. Open the API in your browser and look through what fields it returns
2. Go to `src/types/MovieType.ts` and define a type or class Movie to represent this data
3. Next go to `src/pages/ListMovies/api/FetchMoviesList.tsx` and fetch this above API using fetch or React Query or anything you want to use. Remember to add any package as a dependency using `yarn add <package_name>`
4. The API fetching in #3 should make use of the Type you defined in #2 to sanitize the data
5. The API function in `FetchMoviesList.tsx` should return the data fetched from the API  with data type of `MovieType.ts`
6. For the API to work you might need to send a content header `Content-Type: application/json` 

### Task 2 - React Component + Design + Product Skills

Next we will create a React component to show the movie information returned by the API!
(And optionally style it using MUI / Bootstrap or anything else you'd like)

1. Go to `src/pages/components/Movie.tsx` and create a react component that displays the movies information
2. Use your judgement on what particular fields of the movie response should be shown to the end users for them to decide if they want to wishlist this movie or not (There is a "Poster" field in the response which is an image for the movie if you want to load that)
3. You can use MUI (already setup in the repo) or Bootstrap or any other package you want (add it using `yarn add <package_name>`) to style it
4. Next create a new React Component to display the entire list of these Movies together as Cards or Lists. Use your creativity on whatever seems best for you!

###
### Task 3 - State Management Skills

In this Task we will add a button under each movie for the user to click and add it to their wishlist in the state and also create a page / react component
to show the movies that they wishlisted

1. Go to `src/pages/components/Movie.tsx` and add a button to add this movie to your wishlist
2. Go to `src/pages/Wishlist/components/WishlistedMovies.tsx` to show the list of Movies (reusing the component to show 1 movie if possible) that the user added to their wishlist using the state

### Task 4 - Navigation / Router skills
In this task we will create a basic Left side navigation bar linking to the 2 pages we created so far, List of All Movies & Wishlisted Movies

1. `navigate (pun intended)` to `src/components/Navbar/Navbar.tsx` and implement a React component to show a navigation bar on the left side which is optionally collapsable
2. There should be 2 links to point to the `List All Movies` & `My Wishlist` where the first one shows all Movies from the API, and the second one shows only the movies the user added to their wishlist in the state

### Completion!

In total by the end of this you would have based on how you implement, 4 react components
1. Movie React Component --> Shows 1 movie information
2. List of Movies --> List of Movies React component above
3. Wishlist Movies --> List of Movies react component from #1 that the user added to their wishlist
4. Navigation Bar --> To link to #2 and #3 pages

This concludes the features you need to build for this take home assessment! 
From our side, we would like to thank you for taking the time doing this! Once you submit this, we will strive to get back within 24 hours.

We would also love to hear your feedback on this take home assignment! Do you think something was missing, or was not clear or anyway we can improve this or
just to send a shout-out we would love to hear that through email here: recruitment_feedback@luxesoftware.com

## FAQ
1. Can I add a package that I have worked with in the past?

        Yes! Use any package you want to using yarn add <package_name>
2. Can I use Nextjs or something else?

        Yes! Feel free to delete the entire repo, and create a nextjs typescript app or anything similar.
3. Is there something weird with the API returning data for fields Production or DVD?

        That is intentional, and not a mistake in the API response.
4. Do I have to design or make it look pretty?

        No. Its totally optional and you will penalized for not doing that. A potential is to use MUI to have it styled out of the box for eg.
5. How many hours do I have to complete this assignment once I am given access to it?

        You will have 12 hours from the time you scheduled to get access to this repo
6. I could not complete all the tasks, should I still submit?

        100% please submit. We will still consider it.
7. Can I use an MUI or Bootstrap theme?

        Definitely go for it, but its optional and won't be graded in a positive or negative way
8. Why is the App a js file?

        Good catch! This same template is being used for candidates who have not used typescript and skilled in javascript

Hope you had fun while working through this! If you did not, or it took you more than 2 hours please shoot some feedback at recruitment_feedback@luxesoftware.com to help us make this more streamlined!
