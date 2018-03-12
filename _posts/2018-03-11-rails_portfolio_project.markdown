---
layout: post
title:      "Rails Portfolio Project"
date:       2018-03-12 02:25:48 +0000
permalink:  rails_portfolio_project
---


For my rails project, I created a FitnessLibrary that can help users find free and fun workouts based on the type of workout and area of the body that the user would like to exercise.  I'm always looking for fun and free workouts online that I can do at home.  Once I find great workouts, I like to organize them so that I can easily located each workout easily again for next time I want to do it.  My FitnessLibrary allows me to do just that!  Now, no matter what website I find a workout on, I can add that site to my FitnessLibrary, categorize it by:
* duration - in minutes
* difficulty level - 1-5
* workout type - HIIT, Yoga, Kickboxing, Cardio, Strength Training, etc. 
* body focus - Upper, Lower, Total, Abs
* equipment needed - Mat, blocks, dumbbells, resistance bands, etc.
... and save it to my workouts for the next time.   I started off with two models (Users and Workouts) and built it out from there to add more functionality for users that would make the app more fun to use!

Users Model - I used devise to set up my User model.  I was so amazed when I learned about this Gem.  Not only does it make the user sign up/ sign in process easy, but it also gives the user messages for any errors in their form,  securely stores the users password, and gives many helper methods that I can use throughout my application.  A few of my favorite helper methods through devise were:
1. current_user
2. user_signed_in?

Once I had the basic flow set up for the users, I added the functionality for them to be able to sign in with Facebook through OmniAuth.  I then spent a lot of time in my Workout Model.  This became the biggest model that I added a lot of functionality to.  Most of the Models to come were to help give my workout instances more options.  For example,  when users were adding workouts, I wanted them to be able to pick from a list of predefined workout types, but if they needed to I wanted them to be able to created their own workout type instance that they could use and that others could use in the future.  I also did this for equipment needed and body focus. 

My dream for this app is for users to add their favorite workouts, and to explore the workouts added by others. Therefore, I added the functionality of Favorites.  This way, users could add a workout created by another user to their list of favorites.  That way they can easily find it.  To get this functionality, I created a Favorite model that belongs to a user and a workout.  In the future, I would like for users to not only be able to add a workout to their favorite list, but to be able to organize their favorite list into categories. For example, favorite yoga workouts, favorite kickboxing workouts, favorite upper body workouts, etc.

iI added filter options to give users another way to easily find workouts.  They can filter by workout type and body focus to find the workout that’s right for them. In the future, I would like to add the option to filter by time, difficulty level, and to have multiple filters at once. 

A few other things I want to work on is for usesr to be able to follow other users.  This way if they find a user who adds workouts they are interested in, they can follow them and have a dashboard that will display workouts recently added by that user.  I also want to create a VirtualTrainer.  The VT will be a quick survey the user takes that asks questions like:
1. What type of workouts do you like to do? (HIIT,  Yoga, Kickboxing, etc.)
2. How many days do you want to workout this week?
3. How long do you like to workout for?
Based off of their answers, VT will create a custom workout plan for the calendar week. Then users will be able to save this calendar or edit it to drag/drop the workouts around or add more.  They can then save their VirtualTrainer, log into their account, and click right on the day to be taken to that workout. 

Once I had my models, controllers, and views set up, I then went back through to dry up my code and add in Scope Methods.  I had a lot of fun with these and used them to create a dashboard.  The dashboard highlights videos with the most views, and newest users.  In the future it will also show user stats.  
