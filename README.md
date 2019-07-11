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
- **Category:** Lifestyle
- **Mobile**: The app being mobile makes it easy to log modes of transportation and keep track of their daily carbon footprint
- **Story:** We care about the earth, and we hope that this app inspires people to be more aware and concious about their daily carbon footprint. We want this app to be as simple and user friendly as possible, so even the laziest people can use it easily. 
- **Market:** For everyone that cares about the future of Mother Nature
- **Habit:** This app should be used daily, if not hourly. Push notifications will remind users to always be aware of their carbon footprint
- **Scope:** V1 would allow users to be able to track their carbon footprint (in terms of transportation) daily. V2 allow users their personal monthly/yearly progress. V3 would have recommendations to users if yheir carbon footprint is too large. V4 would enable users to share with friends through other means of social media. 

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**
* Home activity with bottom navigation menu (Alejandro)
   * Include buttons to other fragments (home, add, detailed list, info)
   * Profile fragment is default view
   
* User can see their carbon score for the day (Lisa)
   * Profile fragment
   * ImageView graphic denoting qualtitative use of carbon -> color/emoji (green/happy, yellow/neutral, red/angry)
   * TextView over the graphic denoting quantitative use (need more research on carbon use)
   * Sum up scores for all posts
   
* Add a transportation post
   * Creation Activity (Jennifer)
      * Buttons to choose mode of transportation (walk, bike, carpool/rideshare, electric car, gas car, public transport)
         * Once clicked, start MapView activity for result
         * Check that a title was entered
   * MapView Activity (need more research on GoogleMap API) - (Alejandro)
      * Enter start and end points
      * Button to confirm - go to confirmation screen
   * Creation Activity - (Jennifer & Lisa)
      * Confirmation Screen
      * EditText for user to enter title of post
      * TextView to see mode of transport
      * TextView
      * Calculate "carbon footprint" of an individual post (need more research on average carbon consumption for each mode of transportation) - (Lisa)
      * Confirmation and Cancellation buttons
  
* See a daily log of posts (Alejandro)
   * Stream fragment
   * RecyclerView
   * User can delete an activity

**Optional Nice-to-have Stories**

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
![](https://scontent.xx.fbcdn.net/v/t1.15752-9/67205101_1340408479433581_5902823603593805824_n.jpg?_nc_cat=107&_nc_oc=AQmqqQYQ62pOpdhM2MAFlSZjFBCA_UMvKn33G9w0ze98iST2JgnWEy43uVjFwyyqQ9TaialSkq-QI0KsNepiKfQp&_nc_ht=scontent.xx&oh=91d9c37bb4077ccc0289b84d518e3eaf&oe=5DB723B8)

### [BONUS] Digital Wireframes & Mockups

### [BONUS] Interactive Prototype

## Schema 
### Models

Post(Carbie)

Property | Type | Description 
| -------- | ---- | ----------- |
| objectID | String |unique id for the post |
| title | String | name or short description of what the carbie is (ie trip to work) |
| createdAt| DateTime | time when post was created | 
| start | LatLng| start point of a carbie (ie 123 Home Way) |
| end | LatLng | end point of a carbie (ie 456 Work Way) |
| distance | Integer | distance of trip |
| author | Pointer to user | user who is entering the carbie |

### Networking
- Login screen
  - (GET) Query logged in user object
  - (Create) create a new user
- Confirmation screen
  - (Create/POST) Create a new carbie/post
- Daily Log Screen (feed)
  - (Read/GET) Query all posts where user is author
  - (Delete) Delete existing post/carbie
- Google Maps Screen
  - Utilizing Google Maps API to enter start and end points for a trip, and get distance.
  - https://developers.google.com/maps/documentation/geocoding/intro
  - More research necessary on using API and making network requests
