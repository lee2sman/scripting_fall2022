# Learn about APIs and Make a custom weather application

Today:
- APIs
- Weather API
- 1-on-1 Check-ins with Students
- In-class work + homework

## API

Application Program Interface

An API gives a list of commands that programmers can use to access functionality that they themselves haven't coded or even necessarily know how they work but can still access and get the data they need. 

APIs control access to resources such as data.

They are used to communicate between disparate services.

* An interface for different pieces of software to communicate together over networks
* These are created by organizations, programmers, and companies to access their data
* There are open APIs and those requiring authorization.
* start out by using APIs that have tutorials or sample code and consider trying out ones that don’t require authorization as you learn how to use them!

![API](http://lee2sman.github.io/intermediate-programming/images/api.png)

[What Are APIs?](https://www.youtube.com/watch?v=OVvTv9Hy91Q) video

Examples:

- YouTube API - Allows you to display videos on a web site.
- Twitter API - Allows you to display Tweets on a web site.
- Facebook API - Allows you to display Facebook info on a web site.

### Resources

A link of [Open APIs](https://github.com/public-apis/public-apis) not requiring authorization

Web API Intro on [w3schools](https://www.w3schools.com/js/js_api_intro.asp)

## Build your own Weather Application via Weather.gov weather API

[Minimal code starter](https://glitch.com/~purchase-weather-api)

### Purchase Weather API

This is a stripped-down minimal example of getting started using the weather.gov API.

Our class at [Purchase College](https://purchase.edu) is located in the *coterminous town-village* of Harrison, NY. 

## Procedure

### index.html

Our index.html file holds the minimal-ist bit of text with a div that has the ID ```the-forecast```.

In our header we are importing jQuery to make it easier to import json date. This isn't the only or necessarily the best way to import JSON, but it is consistent and easy to use.

### style.css

A nod to style. This is currently minimally functional. Make it compelling, stylish, organized and intuitive.

### script.js

With jQuery imported we can now grab the weather.gov json file holding the weather data from Harrison, NY with a simple line of code: 
```$.getJSON(url, grabMyData );```

The dollar sign indicates we are using jQuery code. We run getJSON(), passing in the json file's url and sending it to our grabMyData() function as input.

Inside grabMyData() we are selecting the index file's *the-forecast* div, and setting its inner text to a sun, cloud or !? depending on the current short weather forecast description value from our weather json data.

And that is the most minimal possible example I can think of. Check out the json file for examples of many more facets of the weather API you can access.

## Rate Limiting

Companies with data APIs may restrict access to their data by requiring registration. If you make a commercial app that uses their live data, they may even charge a fee. Sometimes they may offer a free tier and a commercial tier. Weather.gov does not charge a fee, but they warn that they may limit access to intense users of their data:

> All of the information presented via the API is intended to be open data, free to use for any purpose. As a public service of the United States Government, we do not charge any fees for the usage of this service, although there are reasonable rate limits in place to prevent abuse and help ensure that everyone has access. The rate limit is not public information, but allows a generous amount for typical use. If the rate limit is execeed a request will return with an error, and may be retried after the limit clears (typically within 5 seconds). Proxies are more likely to reach the limit, whereas requests directly from clients are not likely.

Be careful to avoid rapid reloading.

[More information on the Web API service](https://www.weather.gov/documentation/services-web-api).

[More information on the API endpoints/queries](https://weather-gov.github.io/api/gridpoints)

## Homework

For this assignment you are to make a unique weather "app" via accessing the US Government Weather API from the National Weather Service.

See above for documentation of the API.

Using our starter code in class and the json data file for Purchase, create a compelling weather program website/app.

Pay attention to: 
* crafting a compelling visual representation of the data 
* making it unique 
* ensuring all code runs 
* cleaning up the interface to be clear and bug-free

Link to your weather program from your class website landing page.

Upload the link to your finished program.

Advanced: Bonus points for being mobile-responsive!
