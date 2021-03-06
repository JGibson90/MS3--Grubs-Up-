# MS3---Grubs' Up!
Third Milestone Project for Code Institute

 ![](static/images/devices.PNG)

I wanted to design a website for users to be able to share their own recipes and view recipes from other users. I used MongoDB 
for the database and I used Flask to facilitate building the bulk of the website with templates.

[The live project can be viewed here.](https://ms3-jgibson90.herokuapp.com/)

---
# Contents
- [UX](#ux)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Testing](#testing)
- [Bugs](#bugs)
- [Deployment](#deployment)
- [Credits](#credits)
- [Special Thanks](#special-thanks)
---

# UX
## User Stories
- User goals 
    - As a user, I want to immediately understand what is offered by the website
    - As a user, I want to be able to seamlessly navigate through the site to easily find
     more information
    - As a user, I want to be able to easily interact with the site and the applications within
    - As a user, I want to be able to view all the recipes that are uploaded
    - As a user, I want to be able to sign up so that I can upload my own recipes
    - As a user, I want to be able to edit/update/delete my own recipes

    I made the wireframe using Balsamiq which you can view the wireframe [here.](static/images/wireframe.png)

## Design Choices
---
When designing this website, I looked at existing recipe sites such as [this one for Hello Fresh](https://www.hellofresh.co.uk) 
for inspiration. I opted for a multi-page website with certain pages only being accessible if a registered user is logged in.

## Fonts
I chose [Hepta Slab](https://fonts.google.com/specimen/Hepta+Slab) for my logo for something eye catching and unique. 
I chose [Catamaran](https://fonts.google.com/specimen/Catamaran) for my headings as I wanted something that
would immediately stand out and be noticeable. I chose 
[Roboto](https://fonts.google.com/specimen/Poppins?preview.text_type=custom#standard-styles)
for my main font for its' excellent readability and clean look.

## Icons
I used [Font Awesome](https://fontawesome.com/) for my form icons as well as my button icons and the social media links in the footer.

## Colours
I used the built in CSS colour styling in Materialize to choose my colour scheme and apply it to all necessary HTML element classes.

# Features
- Responsive on all device sizes
- Ability to sign up and become a registered user
- CRUD Functionality
- MongoDB database linked to the website
- Hashed passwords for user security
- Admin privileges to edit/delete any recipes 
- Social media links

## Future Features
Due to time constraints, I was unable to implement these features but will include them in the future
- Modal popup to confirm recipe deletion 
- Ability to see if a recipe is vegetarian or vegan

# Technologies used
## Languages used
- [HTML5](https://en.wikipedia.org/wiki/HTML)
- [CSS3](https://en.wikipedia.org/wiki/CSS)
- [Python](https://www.python.org/)

## Tools, Frameworks and Libraries used
- [Git](https://git-scm.com/) 
    - Git was used for version control, using the Terminal to commit and push to GitHub.
- [Font Awesome](https://fontawesome.com/)
    - Font Awesome was used to add icons to the footer for better UX and aesthetics.
- [Materialize](https://materializecss.com/)
    - Materialize was used to aid with prebuilt classes and the responsiveness of the website across multiple devices.
- [JQuery](https://jquery.com/)
    - JQuery was used in conjunction with the respective Materialize elements for responsiveness
- [Flask](https://flask.palletsprojects.com/en/2.0.x/)
    - Flask was used to easily create a multi page website through the use of templates 
- [MongoDB](https://www.mongodb.com/)
    - MongoDB was used to create a database to store a collection of users and recipes
- [Google Fonts](https://fonts.google.com/)
    - Google Fonts were used to import the Hepta Slab, Catamaran and Roboto fonts into the style.css file for the main logo, 
    headings and the main body respectively.
- [Balsamiq](https://balsamiq.com/) 
    - Balsamiq was used to create the wireframes for the project.

# Testing
I used the [CSS Validator](https://jigsaw.w3.org/css-validator/) which brought up these errors which can be seen 
[here](static/images/CSS-errors.PNG). I also used the [HTML Validator](https://validator.w3.org/) 
which brought up no warnings or errors other than the parse errors for using Flask and Jinjas templates.

Python code passed the [PEP8](http://pep8online.com/) compliance test

## Testing User Stories from UX 
1. As a user, I want to immediately understand what is offered by the website

    1. Upon entering the website, the user is greeted with an appropriate hero image and a navbar with 4 options 
    to go to anywhere on the page 
    2. The user is also presented with a card panel with two call-to-action buttons, prompting them either to sign up or log in
    2. The user has two options, to either select a link from the navbar or utilise the call-to-action buttons, both of which 
    lead to the same location

2. As a user, I want to be able to seamlessly navigate through the site to easily find more information

    1. The site has a fixed navbar so the user can always navigate wherever they want to go

3. As a user, I want to be able to easily interact with the site and the applications within

    1. The user is presented with a simple register and log in template with only two inputs required: username and password
    2. The add recipe page has a simple layout with the minimum number of inputs needed
    3. The edit recipe page has the same layout as the edit recipe page with 3 large buttons clearly labelled and spaced out 
    to avoid accidentally clicking on an action that the user doesn't wish to use

## Further Testing 
- The project was tested on Google Chrome, Mozilla Firefox, Safari for iOS and Microsoft Edge.
- The project was viewed on a variety of different devices such as Desktop, Laptop, iPhone 7, iPhone 8, iPhone 11, and iPad.
- I asked friends and family to view the project and give feedback on any user experience issues and/or bugs. 

# Bugs
Following on from Testing I also encountered these bugs.
## During development
- Recipe info page wouldn't display the selected recipe after following the link from the previous page
    - My mentor helped me decipher where my app.route function was not targeting the correct information
- Default Materialize footer taking up a large portion of the bottom of the site
    - Removed the `<ul>` from the default footer and replaced with simple `<a>` tags containing Font Awesome icons 


# Deployment

**Grubs' Up!** was developed on **Gitpod**, using **GitHub** to host the repository, **MongoDB** to host the database 
and finally deployed via **Heroku**.
These were the steps taken to successfully deploy the website.
- First, open up your **IDE** of preference, open the **terminal** window and type: ``pip3 freeze -- local > requirements.txt.``
- Also in terminal window of your IDE type: ``python app.py > Procfile``
    - These two files are needed for Heroku to see which files to install (**requirements.txt**) and which file is used as the 
    entry point (**Procfile**)
- You need to set up a Heroku account if you have not done so already and select **create a new app** from the **New** dropdown 
button, after which you will be prompted to give a name to your app and select your region.
- Click on the **Deploy** tab and select the **Connect to GitHub** icon
- Underneath that you will be able to search for your repository and then click the **Connect** button once you have selected it
- Scroll back up and click on the tab named **Settings** and then the button named **Reveal Config Vars**
    - You will now need to enter all the variables and their values contained in your `env.py` file i.e.
    (**IP, PORT, SECRET_KEY, MONGO_URI, MONGO_DBNAME, ADMIN**)
- Go back to your **IDE** and add, commit and push both the `Procfile` and the `requirements.txt` to your repository
- Now return to the **Deploy** tab in Heroku and click on **Enable Automatic Deployment**
- Underneath that under **Manual Deploy** click on **Deploy Branch** button and your app should successfully deploy to Heroku

## Cloning the Website
- Open [**GitHub**](https://github.com/) and log in
- Select the **repository**
- Click the **Code** drop down button next to the green GitPod one
- Select **"Clone with HTTPS"** and copy the link
- Open your **IDE** and the **Terminal**
- Specify a new **path directory** where you want to put the clone
- Type `git clone` and then **paste** the previously copied url from before

- Sign up and Log in to MongoDB
- Create a new cluster using an appropriate Cloud Provider for yourself
- Click the **Collections** tab and then the **Create Database** button
- Choose a name for your database and your first **collection**
- Populate your collection with key value pairs

# Credits

## Code
- I used [Materialize](https://materializecss.com/) to make the site
responsive on different devices.

- I used the Data Centric mini project from Code Institutes' course to base my websites logic on.

## Images
- The hero background image came from
[Pexels.](https://www.pexels.com/photo/fruit-salads-in-plate-1640774/)

## Websites

- I used [ResizeImage](https://resizeimage.net/) to help get the hero image
to display properly.

## recipes

- Recipes were from [Hello Fresh](https://www.hellofresh.co.uk/)

# Special Thanks

Special thanks to the Slack community, Stack Overflow, Tutor Support and my Mentor for all their advice and guidance on this project.
