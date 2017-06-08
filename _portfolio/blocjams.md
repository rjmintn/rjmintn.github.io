---
layout: post
title: BlocJams
thumbnail-path: "img/blocjams.png"
short-description: Jam to music while you code!

---

{:.center}
![]({{ site.baseurl }}/img/blocjams.png)

## Explanation

Bloc Jams is a functional web browser based music player application using the jQuery library.

## Problem

While jQuery is a great framework on it's own, I have been asked to take advantage of AngularJS's ability to create and deploy single page applications. Refactoring from jQuery to AngularJS will be completed in several stages.

## Solution

This refactoring project was accomplished in seven stages:

1.  Create starting point
2.  Set routing and states
3.  Starting templates
4.  Establish controllers
5.  Create services
6.  Generate directives
7.  Set filters

#### Starting Point
To set the starting point for this project I installed Node.JS, NPM, and cloned an existing Git repo. I then created a few additional folders to the cloned project, migrated the CSS and assets files, and made some minor updates to the `app/index.html` to prepare the project for AngularJS.

#### Routing and States
Next I created the basic templates for the home, collection, and album pages and added the Angular UI-Router. Within `app.js` the state and location providers were established to allow switching between the 3 different page views and href navigation links were updated to the Angular UI-Router ui-sref directive

#### Starting Templates
Here I modified the album template and created the playerbar template to include the Angular pre-defined directives.

#### Establish Controllers

Now I started creating the controllers to add to the landing and collection templates so that those pages can begin to access the data created by the application.

#### Create Services

Next I began creating the services and injecting them into the controller for the playerbar. These services are the meat and potatoes of the project and provide the user with the functional means to fully utilize the music player. We can now play, pause, and move through the various songs on the albums.

#### Generate Directives

The user needs to observe the status of their music selection as it plays. This functionality is provided by the seekbar directive by providing a means to move forwards and backwards through the song and allow for volume control.

#### Set filters

Finally I set a filter to the seekbar directive to dynamically show the progress of the song as it plays.

## Results

The final result of this project provided a near seamless transition from jQuery to AngularJS with no change to how the end user interacts with the application.

## Conclusion

In larger and more complicated applications, Angular will allow for easier maintenance. This project provided me with an introduction to a new framework that I had never used previously and I look forward to using AngularJS as I expand my Web development knowledge.
