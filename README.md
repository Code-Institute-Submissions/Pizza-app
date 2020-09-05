Pizzapp 
Milestone Project #3 : Data Centric Development Milestone Project  - Code Institute 

## Demo
[Live demo](https://flask-pizza-recipe-manager.herokuapp.com/) is available here.

PizzApp is designed and developed for people who want to explore the very rich and diverse world of pizza, but also for people who have already explored it extensively and want to share their knowledge.
New users are able to register and login in order to view the different categories/styles of pizzas around the world and recipes belonging to each category. Users will also be able to search specific recipies, add, update and delete their own recipes and categories.
Any user may add a new recipe or catetegory as well as view existing recipes and categories added by other users. 
Only the user to uploaded a particular recipe as well as the admin of the page may edit or delete the particular recipe.
Moreover, while any user may add a category, only the admin may edit or delete it. The reason for that is that we want users from anywhere in the world to introduce us to a new category of pizzas, but once the category is created and recipes are added to it, we want only the admin to be able to modify or  delete the category.
was built using the Flask Microframework in Python with a NoSQL (MongoDB) database on the backend, with HTML, CSS, Javascript, and jQuery

## UX, Features and CRUD functionality.


**Client Stories**

1. As a user I would like a website that contains numerous pizza recipes for me to learn,
2. As a user I would like to be able to have a search recipe option.
3. As a user I would like to be able to see what category each pizza recipe belongs to.
4. As a user I would like to be able to view a page where all different available categories of pizza as well as a summary on them, are included.
5. As a user I would like to have a proper register, register, login and logout functionality.
6. As a user I would like to have a profile page once I am registered/ logged in.
7. As a user I would like to be able to add my own recipes and categories.
8. As a user I would like to be able to edit and delete my own recipes.
9. As a user I would like to see who posted each recipe.
10. As a user I would like to see numerous cards of recipes in the homepage.
11. As a user I would like to be able to click and view each recipe on a whole separate page.


**In order to achieve the above goals I did the following:**

- When visiting the site the user first sees the homepage with the navbar, a list of all recipes and a seach bar.

- On the navbar the first time user has the option to register to the site and the returning user to login.

- Once the user is logged in/registered she/he has more options in the navbar: A Profile link to view the profile, add recipe link and a logout link.

- If the wishes to logout she/he just clicks on the logout button and the site takes them back to the login page.

- Once a user has logged in she/he can go back to the homepage to view all recipes and search a particular recipe or click on the New recipe on the navbar in order to add a new recipe. That takes her/him to the add recipe form.

- A user may also go to the categories page on the navbar and click on it whick takes her/him to the page with all available categories.
Since the user is logged in she/he the ADD CATEGORY button appears on the top of the screen just below the navbar. 

- Also the user can click the category name button on each of the category card and that will take her/him to the view category page where the entire selected category is displayed in a single page.

- While anyone can add a Category of styles of pizzas, only the the admin may edit or delete a category. So for regular user will not have a dispaly of the edit and delete category button.
If the admin chooses to edit a Category she/he will press the edit button and that will take her/him to the edit category page.

- Admin may also delete a category by clickin the delete button when she visits the view category page by clicking the category button in the bottom of the card in the Categories page of the navbar.

- In the Homepage every recipe is rendered in a separate card with an image, title, short summary, as well as a button with the category it belongs to and a button to view the entire recipe.
If the user clicks on the style button the site takes her/him to the categories page where cards for different styles of pizzas are rendered.

- If the user clicks on the view recipe button on one of the recipe cards in the homepage that takes her/him to the page where the entire recipe is rendered. On the bottom of the view recipe page the user finds the edit and delete buttons(only if the user posted the recipe her/himself or if the user is the admin.) 
A user may only edit or delete a recipe if the recipe was posted by her/him or she/he is the admin. The Edit/Delete buttons do not appear otherwise.

- A user may edit a recipe she/he has posted by clicking on the edit on the bottom of the recipe which takes her/him to the edit for.

- The user might also press the delete button which will just delete the recipe and return the user to the homepage.

- Finally the user may click on the logout navbar option which will display a message of succesful logout and return the user back to the login page.
 
 ## Wireframe Mockups
 
 These can be found in the static/wireframes folder of this project.
 
 ## Database schema:
I have used three types of MongoDB collections: Recipes, Categories and Users:
- Recipes example:
{
   - "_id": {
     -   "$oid": "5f4cb20343ec23196edc3bd7"
    },

   - category_name: "NY-Style"
   - recipe_name: "Tremendous Brooklyn Pizza"
   - recipe_intro: "A traditional NY style pizza pie from notorious old brooklyn!"
   - ingredients: "Eggs, flour, salt, pepper, tomatoe sauce,cheese."
   - description: "Mix eggs and flour to make dough. Let the dough sit for half an hour. ..."
   - photo_url: "https://upload.wikimedia.org/wikipedia/commons/6/64/NYPizzaPie.jpg"
   - created_by: "Admin"
}

- Categories example:
{
   - "_id": {
       - "$oid": "5f4cb1e043ec23196edc3bd6"
    },
  
    - category_name: "NY-Style"
    - category_description: "Traditional New York style recipes that focus on the notoriously chunk..."
    - photo_url: "https://feelingfoodish.com/wp-content/uploads/2013/06/Pizza-sauce.jpg"
}

- Users example:
{
  - "_id": {
      - "$oid": "5f4ced94f37851c277141274"
    },

  - username: "taposto"
  - password: "pbkdf2:sha256:150000$YydbbTEC$1c8b82ab7596dd07db58c2fcef99764fef59ab43..."
}


## Technologies
- HTMI5 to implement website project.
- CSS3 to implement website project.
- JavaScript, Jquery provided by materializecss.
- Python3, flask framework and its libraries.
- Mongodb database
- GIT POD online web workspace for coding.
- Git Hub hosting services and data storage services.
- Heroku to host project online
- Google Chrome to run GIT POD workspace for development process.
- Google chrome Git extension button to log into Git Pod workspace.
- Google Chrome Developer tools.
- Firefox browser latest version for testing purposes.
- Opera latest version for testing purposes.
- EDGE latest version for testing purposes.
- Materializecss to implement website.
- Font awesome free version.
- Google icons.

## Testing

- This web application was physically tested for display as well as gameplay across multiple browsers  (Chrome, Safari, FireFox, Opera) and on multiple mobile devices using Google developer tool(iPad, iPad Pro, iPhone X, iPhone 6/7/8 (Plus), iPhone 5/SE, Pixel 2 (XL), Galaxy S5). 
- The site is compatible and responsive in all of the above.
- I have tested for layout, functionality and responsive interactivity and it all runs smooth.
- When running the app physically on my iphone I noticed that some buttons did not display properly, either the icon or the text was missing. I spent many hours trying to figure out what in my code may cause that but finally realized that my phone and safari was not up to date.
- Moreover when testing on different mobile devices I noticed that some of the button included icons and some not, which cause the buttons to shrink on smaller screens unevenly. Something I immediately corrected.
- The back end CRUD fuctionality works perfectly and was tested extensively.
- The Admin functionality is amateurish, it is not really a proper admin functionality. It rather is a user by the name Admin who acts as a superuser able to edit and delete things regular users are not.
I achievd the above with simple if functions in which if the username = Admin the certain buttons are displayed for Update and Delete functionality. In the future I plan to have a proper admin functionality.



## Development
- I used Gitpod for a developer tool (IDE) in this project.

## Deployment
All requirements to run and execute project are included in requirements.txt. The following command is required to install all requirements to workspace:
• - pip3 install -r requirements.txt

Database name, password, PORT address, IP address and secret key for sessions are hidden in env.py and added to config vars in heroku settings. These details are not provided for public view. To view implemented and running version of site please click on the Live Demo link at the top of this page. User name and password for admin login are not provided for GitHub public view though they can be provided on request. For assesment these details are provided to code institute student care team. Site is hosted using Heroku platform services. GitHub repository is linked to Heroku app, commits to GitHub are automatically committed to deployed site on heroku platform. Following steps were taken to deploy application and link both platforms:
1. I created a Heroku app, go on Heroku.com. I gave the app a name that is unique and chose Europe as the region.
2. I run following commands before deployment on myworkspace's terminal:
- pip3 freeze –local > requirements.txt, this command will create a requirements file which is required by heroku to install requirements before deploying project.
- echo web: python app.py > Procfile This will create a Procfile. The Procfile is required by Heroku as the entry point for the project.
- Commit workspace to git hub repository by giving commands on your terminal:
- Git add .
- Git commit -m “final commit”
- Git push.
3. I took the following steps to Automatically deploy my project on heroku"
- In the deployment method section of the apps deploy tab on heroku, I selected the option GitHub connect to Github.
- I made sure my github profile was displayed when I pressed the Github connect to github button and wrote the repository's name before clicking search.
- Once the repo was found I clicked connect.
- Since I have hidden my environment variables in my env.py file, heroku won't be able to read them. So I had to tell heroku which vars are required:
- MONGO_DBNAME.
- PORT .
- IP .
- SECRET_KEY.
- MONGO_URI.
4. Finally I clicked on Enable automatic deployment back at the deploy tab of my App.
5. Everything worked perfectly and the project was deployed and automatically updated every time I added, commited and pushed to Github from my workspace.

## Features not yet added
- Display all recipes added by a User on user's profile page.
- Save different recipes as favorite on profile page.
- Share recipes on social media, through email, etc.
- Print Recipes to pdf.
- Download recipe as pdf.
- Add comment section beneath every recipe where users can comment.
- Add like button for users to like recipes.
- Make it possible for user to view other user's profile page and contact them.

### Acknowledgements
- [Code Institute](https://www.codeinstitute.net/) I have learned everything from start to finish by watching Tutor Tim Nelson's tutorials in the data centric development mini-project.
- The images used the project were taken from numerous recipies found on google. I do not own any of the right, I used them strictly for educational purposes.