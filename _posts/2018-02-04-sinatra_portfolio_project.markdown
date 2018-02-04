---
layout: post
title:      "Sinatra Portfolio Project"
date:       2018-02-04 21:40:13 +0000
permalink:  sinatra_portfolio_project
---


For my Sinatra Project, I created a website where users can create an account/login in and create a library of their favoraite workouts.  I love finding free workouts to do online, but keeping track of all of my favorite sites and the workouts on each site can be difficult.  I often lose the link for my favorite workouts or have to share the links with others to try.  My app makes it easy to keep track of your favorite workouts, find new favorite workouts stored by other users, and search for users to see all of the workouts they've created. .

Models - I created two models for this project. 
1. User:  which has many workouts.
2. Workout:  which belongs to a user. 

Views - I created multiple views for the user, workouts, and a main layout which held the navigation bar and footer.

Controllers - I had three controllers. 
1. Application Controller - in charge of main sign in/ sign up page and my helper methods.
2. User Controller - in charge of the CRUD process for users.
3. Workout Controller - in charge of the CRUD process for workouts.

I loved this project and kept adding more functionality as I went along! I started this project by first creating all of the folders and files that I thought I would need. I then set up the classes for my models and controllers.  From there, I made sure to add each contoller to the Confug.ru file. OnceIi had my file structure set up, I created my migrations and tables.  I ended up having to go back and create a few extra migrations because I thought of new attributes that I wanted my workouts to have.  

Once the migrations were complete, the fun part started - thinking of how I wanted my site to function.  I felt very prepared for this project based on all of the other labs up to this point.  Once I created the basic CRUD process for Users and Workouts, I went back through to clean it up and make the views look nicer for the user.  I added in a search bar at the top and embedded videos from the URL links provided by users.  I also added in some bootstrap to make containers and organize the view of all workouts.   I still would like to add in a few more features like being able to follow a user so you can easily see thier uploaded workouts and to be able to star your favorite workouts that you fid from other users.      

Feel free to check it out : https://github.com/brittmmendez/sinatra-cms-app-assessment-v-000




