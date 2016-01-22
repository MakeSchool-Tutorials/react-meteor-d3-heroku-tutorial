---
title: "Meteor Server"
slug: meteor-server
---     

#Server-Side
Let’s begin defining the only server-side piece of our app (although it is also client-side in order to achieve [latency compensation](http://info.meteor.com/blog/optimistic-ui-with-meteor-latency-compensation)). 

> [action]
> In the top-level directory of your app, create a collections.js file.

Now that we have the file, we need to add some logic. We want to define our collection (Hours) and two methods which will be called in our components. 

> [action]
> Add the following outline to the collections.js file:
> 
> ```
>    Hours = new Meteor.Collection("Hours");
>     
>    Meteor.methods({
>      
>    });

<!-- break -->

This creates a Meteor Collection which maps to the database. The empty Meteor methods object should get some functions now.

> [action]
> Add one method that inserts the hours and another that removes them. Name them *insertHour* and *removeHour* respectively. *insertHour* takes the number of hours and the date, checks for inconsistencies and saves into the DB. It makes use of the [Meteor methods](http://docs.meteor.com/#/basic/methods) **check** and **insert**.  
> 
> On the other hand, removeHour takes an id and removes an entry from the database.

<!-- break -->

> [solution]
> Here is a suggestion for what it should be doing line by line. The full code can be found at the end of the tutorial.
> 
> ```
>    Meteor.methods({
>      //Function insertHour takes 2 parameters, the number of hours and the date
>      insertHour: function() {
>        //Parse the first parameter to make sure it is an int
>        CODE HERE
>        //Use the check function to ensure that the first parameter is a number
>        CODE HERE
>        //Use the check function to ensure that the second parameter is a date
>        CODE HERE
>        //Return the insert function (add a key value pair (JSON) consisting of the first and second parameter into the Hours collection)
>        CODE HERE
>      },
>     
>      // Function removeHour takes 1 parameter, the id to remove an entry
>      removeHour: function() {    
>        //Use the check function to ensure the parameter is a string
>        CODE HERE
>        //Return the remove function (remove an entry from the Hours collection by id)
>        CODE HERE
>      }
>    });

Now that we have our server side code written, let's move on to our frontend code.
