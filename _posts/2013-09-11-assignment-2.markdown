---
layout: post
title: "Assignment 2"
---
#Modifying AppInventor
[ArcDemo.apk](http://web.mit.edu/ankush/www/6.S198/files/ArcDemo.apk)

<img src="{{ site.url }}/assets/arcdemo.png" style="width: 240px;"/>



I learned how to create new modules that combine AppEngine components and Android SDK components. I also learned about the Android Canvas API which I hadn't used before, as the addition to AppInventor was the ability to draw curves onto a Canvas.


#AppInventor vs Android SDK Report
##The Idea
My app idea is one that I've actually been working on for a little over a semester. The goal is to create a fully-functional client app for Quizlet.com's web service. The website allows users to create, discover, share and study flashcards in several modes, and the eventual goal of the app is to allow users to do the same on mobile devices.

###Screenshots and Descriptions
<img src="{{ site.url }}/assets/quizletscreens/1_login.png" style="width: 240px;"/>

Login screen where user can either Login or Signup

<img src="{{ site.url }}/assets/quizletscreens/2_classes.png" style="width: 240px;"/>

Once the user is logged in, they see a list of recent events in their classes, an option to filter events, and an option to switch classes though an ActionBar drop down menu.

<img src="{{ site.url }}/assets/quizletscreens/3_classes_tablet.png" style="height: 240px;"/>

On tablets, the Classes page has a different layout

<img src="{{ site.url }}/assets/quizletscreens/4_setpage.png" style="width: 240px;"/>

When the user clicks on a specific set, they are taken to the Set page where they can see terms and images of the set, who created the set, and options to study the set.

<img src="{{ site.url }}/assets/quizletscreens/5_cards.png" style="width: 240px;"/>

In Cards mode, the user can scroll through the terms in the set.

<img src="{{ site.url }}/assets/quizletscreens/6_learnmode.png" style="width: 240px;"/>

In Learn mode, the user is prompted with one side of a Term (and optionally the image) and must enter the other.

<img src="{{ site.url }}/assets/quizletscreens/7_match.png" style="width: 240px;"/>

In Match mode, the user must match the terms and definitions and competes to minimize the time taken for a high score.

<img src="http://web.mit.edu/ankush/www/6.S198/images/quizletscreens/8_userprofile.png" style="width: 240px;"/>

On a user's Profile page, one can see public Sets they've created and Classes they are publicly in.

<img src="{{ site.url }}/assets/quizletscreens/9_search.png" style="width: 240px;"/>

The search page allows users to find new study materials.

##The Implementation
###Android SDK
This app is most definitely feasible through the Android SDK (assuming the server-side API does not have to use the Android SDK). The app isn't functionally very complicated, but a large portion of coding it is based on the representation of objects (Sets, Terms, Users, Groups) which, due to the ability to create custom objects in Java, is not a particularly complicated issue.

A significant component of the app is simply "looking pretty." The Android SDK gives the developer significant control over the design of the app through standard components such as the ActionBar and slide-out menus, fine-tuned Drawable controls (ninepatch images, xml drawables), an Animation and LayoutTransition API, and most of all, the ability to use third-party libraries for functionality that may not already exist.


###AppInventor
Several limitations of AppInventor that would prevent this app from being built are primarily UI-related issues. General noncompliance with the latest Android Design Principles (the lack of ActionBar, overflow menu, navigation drop-downs, slide-out menus, and alternative layout support among many) makes it difficult to have a cohesive, professional-looking application. Having animations and multiple resolutions of graphics for UI elements is also not simple or efficient to do in AppInventor.

The need for a robust data layer, while tricky to implement in Java/Android code, is so cumbersome in AppInventor that it's near impossible to implement. Though the API's JSON requests could be stored in a TinyDB as dictionaries and referenced with advanced knowledge of their types, the inability to create custom objects with their own methods, fields and properties adds additional complications. Queuing network calls while offline, cacheing results in a database, and updating the caches when the user has network access again are relatively doable with the AppInventor platform, but are just so tedious that it is definitely a significant barrier.

Social integration in AppInventor is also not in-depth enough to make developing this app simple. Though AppInventor could allow for Google and Facebook logins through OAuth and web requests, having a simple module in the Social bucket would be a lot more simple. Though Android doesn't support this for Facebook by default, the fact that one can simply add the Facebook library makes this a clear area where AppInventor lags behind.

##The Takeaway
Overall, AppInventor is most definitely a great resource for learning how to program, seeing immediate results, and learning the basics of app creation. In terms of creating professional-looking, robust applications however, there is a significant disadvantage to using AppInventor over the Android SDK.
