---
title: "Mapping Data"
slug: mapping-data
---     

#Mapping Chart Data
Before we code the chart component, we should think about its functionality and how it could be reused it in a future project.

Things that we would want the chart to have are:

* a flexible width and height to make it resizable on any device
* a label indicating the quantity of a bar (the amount of hours)
* a label showing the date (when did we work)

Our goal is to receive the data in a specific format and then render the chart **agnostic**. It will allow us to reuse this component in any other module should we need to, or even a project that is not Meteor-based. All we need to do is ensure that the data is passed in the correct format.

That being said, let’s define the data parameter which will be an array of objects, each object comprising two parameters: the **quantity** (on the y axis - **q**) and the **label** (on the x axis - **label**). Our chart component will iterate over every object and draw a bar associated for each one, labeling it horizontally with the date value and defining its height based on the hours value.

Now we should add our chart to our App component and fill in the function that will send data to our new HourChart component.

> [action]
> Add the mapData function to your App component. It should initialize an array of objects with no quantities and previously defined labels (the days of the week). Next we map the hours object (returned from our collection) with the help of MomentJS to add the number of hours to the q property. Complete the function based on the comments:
>
>```
>    getMeteorData: function() {
>      ...
>    },
>    
>    // Create a data object and return it
>      mapData: function() {     
>        // Create a key - value store using q on the y-axis and label on x-axis
>        var data = [
>          { q: 0, label: 'Mon' },
>          { q: 0, label: 'Tue' },
>          { q: 0, label: 'Wed' },
>          { q: 0, label: 'Thu' },
>          { q: 0, label: 'Fri' },
>          { q: 0, label: 'Sat' },
>          { q: 0, label: 'Sun' }
>        ];
>    
>        // Loop over the data variable and map the dates from the database to a day of the week
>        CODE HERE
>        
>        // Return the data variable
>        return data;
>      },
>    
>    render: function() {
>      ...
>    }
> ```
> 
> Don't forget to add the HourChart into the righthand column and pass the props as data (data={this.mapData()}).

Now that we have all our components on the App component, let's create the chart component using D3!
