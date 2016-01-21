---
title: "Refactoring & Bugs"
slug: refactoring-and-bugs
---     

Bonus content! This is just extra content that will improve your code and make you a better developer! It is not necessary to do this step before deploying to Heroku but if you have the time, do it!

#Refactoring
React is all about small components that can be reused. For that we should make the components that we have created so far, smaller and into individual components. 

> [action]
> Go over the each component again and move the divs that contain content into their individual components. For example the title could be a container:
> 
> ```
>    <div className="page-header text-center">
>      <h1>
>        <i className="fa fa-clock-o"></i> Hours Spent Coding 
>      </h1>
>    </div>
> ```
> 
> And each row in a column should be in a component as well:
> 
> ```
>    <div className="col-md-4">
>      <HourForm />
>      <HourList data={this.data.hours}/>    
>    </div>
> ```
> 
> ```
>    <div className="col-md-offset-2 col-md-6"> 
>      <HourChart data={this.mapData()} />
>    </div>
> ```
> 
> Have a look at the other components too. The smaller, the better and more reusable ultimately. 

#Bugs
Check your code, play with your web app. Do you notice something odd when you add and remove hours? Why is that? What is happening?

Once you're finished with all of this, let's go and deploy our new web app to Heroku.