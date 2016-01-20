---
title: "Setup Your Dev Environment"
slug: dev-env
---     

#Setting up Meteor

Setting up Meteor is fairly straightforward. 

> [action]
> On a Mac, open your terminal and type the following:
>
> `curl https://install.meteor.com/ | sh`
> 
> Press enter and watch it installing.

<!-- break boxes -->

> [info]
> If you are on another OS, go to [https://www.meteor.com/install]() and follow their instructions.

Let's setup a new project. Meteor tells us how to do this after we've installed it, so let's follow their instructions.

> [action]
> Create a new project, navigate to it and use the *meteor* command to start the server.

<!-- break -->

> [solution]
> Don't type the $! This just indicates a command that needs to be exceuted in the terminal.
> 
>    `$ meteor create ~/coding-time`
> 
>    `$ cd ~/coding-time`
> 
>    `$ meteor`

It should say: 

```
=> Started proxy.
=> Started MongoDB.
=> Started your app.

=> App running at: http://localhost:3000/
```

You can now go to [http://localhost:3000/]() to see your brandnew web application running. Every time you make a change, Meteor will reload the page automatically! How neat is that?

Now, that we have our new project, navigate to it in Finder. You will note that three files were automatically generated. Get rid of them. Time for adding packages.

#Setting up the environment
Normally we would go and download the library and add it to our project manually. We don't need to do this with Meteor as we can add the libraries using Meteor directly in the command line.

> [action]
> Add the libraries using the following command:
> 
> `meteor add react`
> 
> Now do the same for the other libraries we need:
> 
> * **check** (asserts data integrity)
> * **d3js:d3** (our charting library)
> * **momentjs:moment** (a JS library to work with dates)
> * **twbs:bootstrap**
> * **fortawesome:fontawesome**
> 
> We will use Twitter Bootstrap and the FontAwesome library for styling purposes.

The first is the official react package bundled by the Meteor Development Group. The second is the official D3.js package for Meteor. We are doing some date manipulation, so MomentJS is a good choice. Fourth and fifth are Bootstrap and FontAwesome, just for styling purposes.
