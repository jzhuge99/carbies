Group Project
===

# CO2 & U

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
App for user's to track their daily/monthly/yearly carbon footprint relating to what modes of transportation they use per day. Users will enter in where they travel and how they travel, and at the end of the day, receive a rating determing how "eco-friendly" they were to the earth that day. :)

### App Evaluation
[Evaluation of your app across the following attributes]
- **Category:** Lifestyle
- **Mobile**: The app being mobile makes it easy to log modes of transportation and keep track of their daily carbon footprint
- **Story:** We care about the earth, and we hope that this app inspires people to be more aware and concious about their daily carbon footprint. We want this app to be as simple and user friendly as possible, so even the laziest people can use it easily. 
- **Market:** For everyone that cares about the future of Mother Nature
- **Habit:** This app should be used daily, if not hourly. Push notifications will remind users to always be aware of their carbon footprint
- **Scope:** V1 would allow users to be able to track their carbon footprint (in terms of transportation) daily. V2 allow users their personal monthly/yearly progress. V3 would have recommendations to users if yheir carbon footprint is too large. V4 would enable users to share with friends through other means of social media. 

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**
* Home activity with bottom navigation menu
   * Include buttons to other fragments (home, add, detailed list, info)
   * Profile fragment is default view
   
* User can see their carbon score for the day
   * Profile fragment
   * ImageView graphic denoting qualtitative use of carbon -> color/emoji (green/happy, yellow/neutral, red/angry)
   * TextView over the graphic denoting quantitative use (need more research on carbon use)
   * Sum up scores for all posts
   
* Add a transportation post
   * Creation Activity
      * EditText for user to enter title of post
      * Buttons to choose mode of transportation (walk, bike, carpool/rideshare, electric car, gas car, public transport)
         * Once clicked, go to MapView activity
         * Check that a title was entered
   * MapView Activity (need more research on GoogleMap API)
      * Enter start and end
      * Button to confirm
   * Calculate "carbon footprint" of an individual post (need more research on average carbon consumption for each mode of transportation)
   
* See a daily log of posts
   * Stream fragment
   * RecyclerView
   * User can delete an activity

**Optional Nice-to-have Stories**

* See detailed overview of post before logging the activity (p1)
   * Detail frgament - confirmation screen
   * See title, mode of transportation, start, end, distance, rating for activity
   * Confirm and cancel buttons
* Recommendations (p1)
   * General recommendation- if user is in red, recommend walking, carpooling, public transportation
   * NOT specific alternatives
* Notifications (p2)
   * Reminder to log
   * encouraging/warning messages 
* “Share” with friends (p3)
* monthly/yearly progress (p3)
   * Calendar fragment
   * Detailed views of day
   * Trend line
* Detailed view of activity from list view (p2)


### 2. Screen Archetypes

* [profile]
    * give a rating - Red/Yellow (warning) vs. Green (encouraging)
    * sum all of the activies up at the end of the day
* [creation]
    * add a transportation activity
    * allows user to input mode of transportation
    * calculates carbon footprint of an individual activity
* [map View]
    *  allows user to input start and endpoint of their travel 
*  [stream]
    *  delete and activity if needed
    * see activities for the day
   
 

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* [fill out your first tab]
* [fill out your second tab]
* [fill out your third tab]

**Flow Navigation** (Screen to Screen)

* [home screen]
   * => creation
   * => stream
* [creation]
   * => map view
   * => home screen
* [map view]
    * => creation
* [stream] 
    * => home screen


## Wireframes
![](https://scontent.xx.fbcdn.net/v/t1.15752-9/65947598_503561243782278_7727859721398386688_n.jpg?_nc_cat=100&_nc_oc=AQkoTWIv1KSWkLWyX5goj4OQYhvRUmwg-FK6qOahAMGB3iRW_gpDPST9yUImVRXfGb8gqPDgHuqj3vPWw3YNGN97&_nc_ht=scontent.xx&oh=de49521c13051b3a039d4c97fd60fde6&oe=5DB00850)

### [BONUS] Digital Wireframes & Mockups

### [BONUS] Interactive Prototype

## Schema 
[This section will be completed in Unit 9]
### Models
[Add table of models]
### Networking
- [Add list of network requests by screen ]
- [Create basic snippets for each Parse network request]
- [OPTIONAL: List endpoints if using existing API such as Yelp]
