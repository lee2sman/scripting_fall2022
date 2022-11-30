# Working with servers

Today:  

* check-in
* saving and accessing data on a server
* in-class studio time

# Saving Data to a Server / Getting Data From A Server

For many of our projects, you may need to save data to a server, or get data from a server, or both.

Json is a common way to organize and store our data.

But to send data to a server, that data must be sent as a string of text.

We can convert a javascript object with ```JSON.stringify()```


### Converting JSON to text

Example

```
var obj = { name: "Shane", age: 39, city: "Los Angeles" };

var myJSONAsString = JSON.stringify(obj);

document.getElementById("demo").innerHTML = myJSON; 

//or in jQuery
//$('#demo).html(myJSON);
```

### Working with the file system using Node.js

Node.js comes with a builtin file system module to work with a computer's file system, or for example on a server.  It can **read files, create files, edit files, delete files, and rename files.**

 To use it, we must import it.
 
 In Node.js we do this with the require statement.

```
let fs = require('fs'); 
```

Note: you may also see this written as ```const fs = require('fs');```

#### Reading a file

We can read from a file saved on a server. This can be a text file or a json data file for example. We use the readfile module, part of ```fs```.

```
fs.readFile()
```

Example

**student.json** file:

```
{
  "name": "Jorge",
  "age": 45,
  "department": "Math and Computer Science"
}
```

**script.js** file

```
let fs = require('fs');

fs.readFile('student.json', function(err,data) {  
    if (err) throw err;
    let student = JSON.parse(data);
    console.log(student);
});

console.log('This is after the read call'); 
```

These two files are in the same directory. We can run our script with ```node script.js```

Doing so will print out:

```
this is printed after the read call
{ name: 'Jorge',
age: 45,
department: 'Math and computer Science'}
```

Since Javascript is asynchronous, we start reading the student.json file, and we have a callback to run when finished. In the meantime, we print to the console in the last line of our script. Our readFile finally finishes and triggers the anonymous callback function that parses our student json data and prints it out. 


#### Writing to a file

You can create a new text file in the file system with ```fs.writeFile()```. If the file already exists, it will overwire the previous content.

You can also add text to the end of a file using ```fs.appendFile()```. This has the advantage of not overwriting a file, and if it doesn't already exist, it will create the file first.

```
let fs = require('fs');
let myText = "This text and the random number "+Math.random()*100+" will be added to the end of the file. ";

fs.appendFile('textFile.txt', myText, function (err) {
  if (err) throw err;
  console.log('Saved to textFile.txt!');
});
```

Again, we can save this as a script file and run it with ```node script.js``` or whatever we've named the file.

### Resources

- Node.js [File System](https://www.w3schools.com/nodejs/nodejs_filesystem.asp) tutorial
- Node.js [modules](https://www.w3schools.com/nodejs/ref_modules.asp)

## In-class studio time

- 1-on-1 meetings

# Final Project

This semester we have built websites for our class, (false) or misleading institutional websites, and a web-based time capsule. These sites have been collections of material: images, galleries, or institutional pages with lots of choices of what to navigate. They give a user multiple modes of entry and allow exploration. Now we are going to go small and concentrate on creating a site, app or extension for a single project or idea that we want to deliver to the world that will be delivered as a speculative work.

We have had multiple discussions on contemporary issues relating to the web today, from companies tracking users' every action, to the loss of privacy and the inability of many users to resist the compulsion to check their various feeds. How can you acknowledge this world and create a new intimacy with your website's visitors?

For this assignment you will make a mobile-responsive site or intervention (in the form of a web extension) that fundamentally alters our engagement with the Internet. The goal is to make a compelling site, app or extension with information, media, or other content but one that respects your user, plays with convention, or distorts a user's expectations on the web. You are a unique individual and your work is too! You may deconstruct your project or even the idea of a website itself. Perhaps your site is playful, mysterious, a game, a poem? How can the website be a work of art?

# Goals:
* the site should be responsive - it must work well on the desktop and mobile browsers
* the site should have interactive elements - you may want to use javascript, jquery or P5js
* the design should be compelling and unique - no cookie cutter sites. Question what the site is, the conventions of such sites, and make it your own!
* the site should be well-executed and original
* Consider how your site works with data and APIs.

**Final projects must be uploaded to the web by Wednesday May 14 at noon. Project presentations will be in class on May 14 at 3PM.** We will have a series of smaller steps to accomplish leading up to that.

# Examples

* [touched-some1](http://touched-some1.com) - For Underneath The Skin
* [Follower](http://follower.today) - art/performance project and commentary
* [Binky](http://binky.rocks) - App/Artwork
* [somebody app](http://somebodyapp.com) - App/performance project?

# Homework

Get a first prototype ready!

Write a development log of half a page.

* What are/were your goals for the session?
* What did you spend your time on during your work session(s)?
* What worked?
* Where are you stuck?
* What are your next steps?
* How does this fit into the overall project idea so far?

