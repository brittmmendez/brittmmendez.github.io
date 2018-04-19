---
layout: post
title:      "Rails App with a jQuery Front End"
date:       2018-04-19 03:54:24 +0000
permalink:  rails_app_with_a_jquery_front_end
---


Up to this point, each portfolio project I’ve built has been from scratch. First, a Ruby GEM that scrapped Amazon’s site providing a CLI interface for a user to search the top books of the week. Then a Sinatra app that provided a way for users to create workouts implementing REST and CRUD conventions. Then, building off of what I learned in Sinatra, and feeling passionate about my workout creator, I made Rails app allowing users to create their own workouts, track other users workouts, and workouts to a favorites list, and filter so it’s easy to find new fun and free workouts.

However, for this project, I didn’t have to start from scratch.  Instead of a new app from scratch, my goal was to expand upon my previous Rails app to add dynamic features that are only possible through jQuery and a JSON API.

To get started, I added a serializer using the gem 'active_model_serializers'. Which is funny because it was one of the last things we learned in the unit, but one of the first that I utilized.  For those that haven’t used the gem yet, let me tell you, it is magic!  This handy gem make data serialization so easy that you’ll never again question whether or not to serialize your data. Usig this gem saves you time on having to creating your own serializer.  It also makes it easy to set up your associations so you can always access the data you need.

For this project, there were five requirements:

Must render at least one index page (index resource - 'list of things') via jQuery and an Active Model Serialization JSON Backend.
For this, I created a comment system allowing users to make comments on workouts to offer reviews for how the liked the workout.  Therefore, I displayed the index of the workout comments by all users on the workout show page.  I did this by fetching the comments via an AJAX GET request, with the backend rendering the comments in JSON format, and then appending the posts to the page.

Must render at least one show page via jQuery and an Active Model Serialization JSON Backend. 
I did this on my workout show page by having a Next and Previous button that allows a user to sift through the workouts the show page, with the next workout being fetched and rendered via JQuery/AJAX.

The next through requirements I combined together into one feature - a comment system.  Users can comment on workouts to leave their workout review for other users.

The rails API must reveal at least one has-many relationship in the JSON that is then rendered to the page. 
Must use your Rails API and a form to create a resource and render the response without a page refresh.
Must translate the JSON responses into Javascript Model Objects. The Model Objects must have at least one method on the prototype. 

I think the hardest thing about the project was building into an app I already had.  However, once I got started, I was able to see a the pattern forming between how to user JQuery/AJAX ad the importance of JSON!  Now, I can’t wait to keep on working in my project to make my app even more dynamic!

