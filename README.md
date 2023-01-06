# Bored? - GA Project Two - 1.5 days
![Activity index page](https://user-images.githubusercontent.com/114397080/210851353-49fa248c-0536-4fb2-a905-ff1168eea3bf.png)

## Description
In a world filled with ”doom scrolling”, Bored? is a website that seeks to inspire the user with ideas about how they could fill their time in meaningful and productive ways! On entering the site they are presented with a homepage, and click through to a menu of activity categories. On selecting their chosen activity the user is suggested an activity they could try within this category. This is randomly generated, and the user can select  “Try again” to have another suggestion delivered to them within that same category. Alternatively, if the user is feeling adventurous they can  select the “Surprise Me!” category, which will return a random activity of any category. 

## Deployment link
Bored? was deployed with Netlify and can be experienced [here](https://bit.ly/Bored_).

## Getting Started/Code Installation
Clone or download the Github repo. Open it in the editor of your choice and run `yarn` in your terminal to install all dependencies. Add Axios with Yarn `add axios` command, then start the server with `yarn start`. 

## Timeframe & Working Team 
I created this website for General Assembly's project two, along with my other team members Imra Skaliks and Margherita Varosio. We were given 1.5 days to build a website using React.js and a third party public API.

## Brief
* Consume a public API. This could be anything but it must make sense for your project.
* Have several components
* The app can have a router with several "pages", this is up to you and if it makes sense for your project.
* Include wireframes that you designed before building the app.
* Be deployed online and accessible to the public.

## Features
![Screenshot 2023-01-05 at 18 13 39](https://user-images.githubusercontent.com/114397080/210851133-e69b072a-b77d-4b42-9030-7b12bf9aa0a1.png)

* A homepage that is simple, and centered on a striking Gif “stop scrolling, start doing”, which sets the scene for the user.
* A navbar that redirects the user to the homepage and activity page from anywhere on the site.
* An activity menu which seeks to inspire the user about how they can fill their time using strong visuals.
* The “Surprise Me!” button to generate a random activity of any category.
* A single activity page which displays the randomly generated activity suggestion. Further random suggestions within the category can be obtained using the “Try again” button.

![Screenshot 2023-01-05 at 18 21 01](https://user-images.githubusercontent.com/114397080/210852478-318d32b3-8f4c-4b05-bf67-7ba49b6beec1.png)

## Technologies Used
* React.js
* HTML5
* Sass
* CSS
* JavaScript 
* Bootstrap
* Axios
* Yarn
* Insomnia
* Git and GitHub
* VSCode
* Netlify

## Planning
This was a group project but on a very short timescale, in order to optimize the learning opportunity from other colleagues we decided to work together from start to finish. I did the coding and made regular commits to Github, and at completion my colleagues forked from this. 
We made a breif plan of priorities and what must be done to meet the project breif, and other functionality that could be achieved with additional time We used [Trello](https://trello.com/) to keep track of our TODO list.

### Finding an API
We searched the web looking for a clean and easy to use API. The [Bored API](https://www.boredapi.com/documentation#endpoints-participants) returns a single object at random when called. Endpoints can be filtered by any of the keys, for example by activity;

![Screenshot 2023-01-05 at 18 25 20](https://user-images.githubusercontent.com/114397080/210853246-fa2401eb-399c-4392-8d30-b33b1d38b471.png)

### Wireframe
We used [Excalidraw](https://excalidraw.com/) to sketch out how the website would look and function, and define the user journey.
![Screenshot 2023-01-05 at 18 27 05](https://user-images.githubusercontent.com/114397080/210853606-579be761-9556-4a95-b5f0-7a4c4de1c3f7.png)

### Pseudocode
We used pseudocode to work out the logic and framework for our code. 

## Build/Code Process

### App.js

The router was the first part of the code we set up and detailed our endpoints and embedded our page components

![Screenshot 2023-01-05 at 18 42 02](https://user-images.githubusercontent.com/114397080/210856303-bba8f844-9c9f-4ab1-9d00-b03f60818bdc.png)

### Homepage
The homepage is a simple eyecatching call to to the user. It uses `Link` from React-router-dom and `Col` and `Button` components from Bootstrap. 

![Screenshot 2023-01-05 at 18 38 03](https://user-images.githubusercontent.com/114397080/210855516-e61074e0-b0ab-4240-ad8b-f8068bbc9789.png)
### Single activity page

Here we set the activity `choice` object, which contains the `type`(category) and `activity` (description) keys, to state.

The `handeGetChoice` function is set to `useCallback` so the component will not re-render unless the `choice` changes and the API request is made within the `useEffect` when `handleGetChoice ` is called. The `useLocation` object will update each time the URL changes, and makes an API call to the `choice` that is currently held in state `location.state.choice.type`. 

![Screenshot 2023-01-05 at 19 28 55](https://user-images.githubusercontent.com/114397080/210864178-2d183935-0d2f-46fa-83f9-2698c3a81858.png)

“Try again” button makes another call to the API endpoint to show another random endpoint of the same `choice` currently held in state . “Back to Activities” uses a button as a `Link` to navigate back to the main activity menu.

### Activity index page
We saved activity categories and images in the `choiceArray` as the no "show all" endpoint was available in our chosen API. 

We used `useNavigate` in the `navigateToChoice` function, in which params have been set as the `choice` currently held in state, onClick.
If the user clicks the "Surprise Me" button instead, the `getRandomChoice` function is called which randomises a `choice` , saves it to `randomChoice` and uses the `navigateToChoice` function to navigate to it.

![Screenshot 2023-01-05 at 18 46 20](https://user-images.githubusercontent.com/114397080/210857095-b28df5de-76db-44f6-b00d-fc3140546ab0.png)

In the return we map the choices in the `choicesArray` and display the data from the API call made on the single activity page.
![Screenshot 2023-01-05 at 18 50 04](https://user-images.githubusercontent.com/114397080/210857737-83a7e4c5-83cd-4675-9d2f-c1ad49249262.png)

### Styling
This was achieved with a combination of Bootstrap and Sass.

## Challenges
* Working in a group, there were many ideas for APIs at the start of the project.
* The API was not data rich and had some limitations. There were no pictures, and only a couple of entries with links. Although the data was easy to access, only one dataset was returned at a time, and there was no endpoint for us to view all of the objects in the API at once. The documentation was also very minimal and we had to spend time immersing ourselves in it using Insomnia. 
* Working together on the code (with just myself writing the code) meant that things definitely took longer, and although we achieved our minimum viable product, I would have liked to have liked to get some more  functionality into the site. This could have perhaps been achieved if each person had been allocated a different part of the project. 
* I feel the styling and responsiveness were limited by the timeframe of the project. 
* I would have liked to rename the Busywork category, however due to how we used the activity keys in our site, we had to keep the key name as it was written in the database. 

## Wins
* We had a great working dynamic and worked effectively as a team. We initially had a very strong idea involving a different API, but after discussion and some initial planning we came to the decision that we wouldn't be able to achieve a desired endpoint within the allocated time scale.I think it is to our credit that as a group we recognised this and were able to be dynamic and change our plan to a more realistic goal.
* I found working with others a good learning experience. Everyone brought something different to the project and it was helpful to be able to share knowledge, and I found talking through ideas solidified my own understanding. 
* I took on the role of coding and presenter at the end of the project. Writing the code was excellent practice and helped me solidify knowledge. I felt I was able to draw the team members' ideas together well. 
* I feel we kept the user story simple and well defined.
* Making regular commits to Github empowered us to take risks with ideas. 
* We made our code DRY.

## Key Learning Points
* I became much more comfortable with navigating and accessing data returned from an API.
* I was able to practise using React, and have subsequently developed a far greater understanding of this, and when to implement useState and useEffect.
* I learned about and used useNavigate, useLocation, and useCallback.
* I worked with Bootstrap and SASS for the first time.
* I deployed a site for the first time using Netlify. 

## Future Improvements
* With more time I would have liked to make use of some of the other data returned by the API. 
* Transform the API price data and accessibility rating and display this along with the activity in the single activity page( e.g. as £, ££, £££).
* I would like to have added in a filter for number of participants, cost and accessibility.
* The pictures break out of their card on smaller screens, therefore some adjustment is needed to make it a fully responsive design, and suitable for use on the go.
* I would have liked to use another API to dynamically provide the images for the categories, and maybe provide more detail for each activity.
* Adding in a search feature, e.g. if wanting to search for more specific ideas (e.g. search for activities with “baking” in the description).
* The website would make an excellent phone app, and it would be great to get it fully responsive for use on the go.
