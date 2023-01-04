# Bored? - GA Project Two - 1.5 days
BORED? - GA Project Two

## Description

In a world filled with” doom scrolling”  Bored? is a website that seeks to inspire the user with ideas about how they could fill their time in meaningful and productive ways! On entering the site, they are presented with a homepage, and click through to a menu of activity categories. On selecting their chosen activity, the user is suggested an activity they could try within this category. This is randomly generated, and the user can select  “Try again” to have another suggestion delivered to them within that same category. Alternatively, if the user is feeling adventurous, they can  select the “Surprise Me!” category, which will return a random activity of any category. 

## Deployment link

Bored? was deployed with Netlify and can be experienced [here](https://bit.ly/Bored_

## Getting Started/Code Installation

Clone or download the Github repo. Open it in the editor of your choice and run yarn in your terminal to install all dependencies. Add Axios with yarn add axios command, then start the server with yarn start. 

## Timeframe & Working Team 

I created this website for General Assembly's project two, along with my other team members Imra Skaliks and Margherita Varosio. We were given 48 hours to build a website using REACT and a third party public API.

## Brief

* Consume a public API. This could be anything but it must make sense for your project.
* Have several components
* The app can have a router with several "pages", this is up to you and if it makes sense for your project.
* Include wireframes that you designed before building the app.
* Be deployed online** and accessible to the public (hosted on your public github, not GA github!)

## Features

* A homepage that is simple, and centered on a striking Gif “stop scrolling, start doing”which sets the scene for the user.

* A navbar that redirects the user to the homepage and activity page from anywhere on the site.
* An activity menu which seeks to inspire the user about how they can fill their time using strong visuals.
* The “Suprise Me!” button to generate a random activity of any category.
* A single activity page which displays the randomly generated activity suggestion. Further random suggestions within the category can be obtained using the “Try again” button.

## Technologies Used

* REACT
* HTML5
* SCSS
* CSS
* JasvaScript 
* Bootstrap
* Axios
* Yarn
* Insomnia
* Git and GitHub
* VS Code
* Netlify

## Planning

This was a group project but on a very short timescale, in order to optimize the learning opportunity from other colleagues we decided to work together from start to finish. I did the coding and made regular commits to Github, and at completion my colleagues forked from this. 

### Finding an API
We searched the web looking for a clean and easy to use API. The bored API returns a single object at random when called. Endpoints can be filtered by any of the keys, for example by activity;

### Wireframe
We used Excalidraw to design roughly how the website would look and function, and define the user journey.
Project Plan and Pseudocode
We made a brief plan of priorities and what must be done to meet the minimum viable product, and other functionality that could be achieved with additional time.We used pseudocode to work out the logic and framework for our code. 

## Build/Code Process

### Bringing in the API 

Using useEffect to bring in the data from the  API with useCallback. Location variable and handleGetChoice function used in dependency array so data retrieved when user makes choice from the activity index.

Using choice type to extract data for each category


Choice object set to state. Object containing available categories and images assigned. 
Using navigate to go navigate to choice, depending on state.

Single activity page buttons

“Try again” makes another call to the API to show another random activity within the category previously selected via the menu. “Back to Activities” uses a button as a link to navigate back to the activity menu( choice index).


“Surprise Me!” random choice function


### Styling
This was achieved with a combination of Bootstrap and SASS.

## Challenges

* Working in a group, there were many ideas for APIs at the start of the project.
* The API was not data rich and had some limitations. There were no pictures, and only a couple of entries with links. Although the data was easy to access, only one dataset was returned at a time, and there was no endpoint for us to view all of the objects in the API at once. The documentation was also very minimal and we had to spend time immersing ourselves in it using Insomnia. 
* Working together on the code (with just myself writing the code) meant that things definitely took longer, and although we achieved our minimum viable product, I would have liked to have liked to get some more  functionality into the site. This could have perhaps been  achieved if each person had been allocated a different part of the project. 
* I feel the styling and responsiveness were limited by the time frame. 
* I would have liked to rename the Busywork category, however due to how we used the activity keys in our site, we had to keep the key name as it was written in the database. 

## Wins

* We had a great working dynamic and worked effectively as a team.We initially had a very strong idea involving a different API, but after discussion and some initial planning we came to the decision that we wouldn't be able to achieve a desired endpoint within the allocated time scale.I think it is to our credit that as a group we recognised this and were able to be dynamic and change our plan to  a more realistic goal.
* I found working with others a good learning experience. Everyone brought something different to the project and it was helpful to be able to share knowledge, and I found talking through ideas solidified my own understanding. 
* I took on the role of coding and presenter at the end of the project. Writing the code was excellent practice and helped me solidify knowledge. I felt I was able to draw the team members' ideas together well. 
* I feel we kept the user story simple and well defined.
* Making regular commits to Github empowered us to take risks with ideas. 
* We made our code DRY.

## Key Learning Points

* I became much more comfortable with navigating and accessing data returned from an API.
* I was able to practice using REACT, and have subsequently developed a far greater understanding of this, and when to implement useState and useEffect.
* I learned about and used useNavigate, useLocation, and useCallback.
* I worked with Bootstrap and SASS for the first time.
* I deployed a site for the first time using Netlify. 


## Future Improvements

* With more time I would have liked to make use of some of the other data returned by the API ; 
* Transform the API price data and accessibility rating and display this along with the activity in the single activity page( e.g. as £, ££, £££).
* I would like to have added in a filter for number of participants, cost and accessibility.
* The pictures break out of their card on smaller screens, therefore some adjustment is needed to make it a fully responsive design, and suitable for use on the go.
* I would have liked to use another API to dynamically provide the images for the categories, and maybe provide more detail for each activity.
* Adding in a search feature, e.g. if wanting to search for more specific ideas (e.g. search for activities with “baking” in the description).
* The website would make an excellent phone app, and it would be great to get it fully responsive for use on the go.



