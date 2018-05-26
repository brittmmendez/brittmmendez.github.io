---
layout: post
title:      "React Redux Project"
date:       2018-05-25 18:23:34 -0400
permalink:  react_redux_project
---


This was my final, and hardest project for Flatiron.   It's called [Trail-Finder](https://www.youtube.com/watch?v=-heKPE6yzVM&t=8s).   This project integrates all of the skills that I've learned through the ENITRE program.   
* Rails API backend to persist data for the application.
* Using fetch() within my actions to GET and POST data from my API 
* Redux middleware to respond to and modify state change
* Redux and redux-thunk middleware are being used to modify state change and make use of async actions to send data and receive data from the server  
* Using react-router and proper RESTful routing
* Using async actions to send data to and receive data from my server
* Written in ES6

For my project, I created an app that that will help me keep track of all of the new trails that I run this summer, and how ofter I run them.  It's a CRUD app so I can add, delete, read, and edit any of my trails.   The trails index page also reorganizes the trails based on their current run counter.  In the future, I would like to also add in a comment system so tha I can comment on my runs each time to keep track of time/pace and date that I ran it. I also want to change the way I create the trail to allow for uploading a picture instead of just randomly generating a photo.  Right now, it's just for me to use, but I'd like to add a way for other users to create accounts.  So user creation, authentication, and authorization.

To get started on this project, the article in the project directions was so helpful: [Setup Rails API with React](https://www.fullstackreact.com/articles/how-to-get-create-react-app-to-work-with-your-rails-api/).  I really recomend using this as a starting point to get your rails API backend and react client side created.  It also walks you through how to have both servers running at the same time and how to create a rake action to just use rake start for both servers to work. 

**Backend** - Following the above directions - I created the API by typing: `rails new project-name --api`.The `--api` flag is new in Rails 5. This flag excludes certain dependencies that aren't necessary for an API-only Rails server. I created only one model - trail with name,distance, image, and discription attributes.  The controller was set up to just render json.  ex: `render json: @trail, status: 200`

**Client Side** - Following the above directions - I created the cleant side by typing: `create-react-app client`

Thr trickiest part for me was figuring out how to get both servers up and running at the same time, but luckily the blog talked about using Foremen.  Foreman is a utility for managing multiple processes.   I then set up the proxy.  This is to have the Webpack development server proxy all requests starting with /api to our API server. 

