# SQL-Music-Tour-API
SQL Music assignment
Activity: Creating the Remaining Controllers
Over the past few lessons, we've learned how to query our database tables through Sequelize. With that, we were able to create the base of our bands controller. Before we can move on to learning how to deal with the complex relationships our tables have through Sequelize, let's finish writing the remaining controllers.

 ### Getting Started
- Open your terminal.
- Navigate to the location where you cloned the SQL-music-tour-api repository.
- Open the repository in your code editor of choice.
- In your terminal, run the project.
### Determining the Necessary Controllers
While we technically could create controllers for every single table, some of them are not necessary. A few of our tables will typically be queried in relation to another table.

For example, stage_events is purely a join table, and there would be little reason to query that table alone. As a result, having a whole controller with full CRUD on just the StageEvent alone wouldn't be very useful. To save ourselves some time, we can simply not create a controller for it.

With that in mind, what other models do not need a separate controller?

What other models do not need a separate controller? There are multiple correct answers.

Event
Stage
### MeetGreet
SetTime
From that, we've now deduced that we only need to create new controllers for:

Event
Stage
### As for the other models, we'll learn how to query them after we learn about Sequelize associations.

## Creating the Controllers
Now that we know what controllers need to be created, it's up to you to create them. For both controllers, create the basic CRUD routes as we did for the bands controller:

- Index route
 - For the events controller, order the data by ascending date.
- Show route
- Create route
- Update route
- Delete route
Don't forget to require and use the controllers in your entry file! The base URLs should be:

-/events
-/stages
This will now allow the event organizers to manage bands, events, and stages as they please! Of course, we're still missing some of the key functionality they requested, such as printing out an entire schedule for a particular event or band-but we're getting closer!

## Make sure that you test each route in Postman after you create it.

### Bonus
1- Similar to how we let our band index to be filtered by band name, it would be nice if events and stages did the same. Consider upgrading the index routes of both controllers to filter them by name with a query string.

2- Although the database is small at the moment, you can imagine how large it will get as more events and bands are added. Our index will end up being very long in those cases. To avoid that, consider adding a query string that will limit the amount of data shown on the index.
However, that now presents a problem if the user decides to limit data by a certain amount-they can't see the remaining data. To solve that, make sure to add a pagination query string as well.

### Acceptance Criteria
When viewing the controllers file in VSCode, the Event and Stage controllers exist.
When viewing the Event and Stage controllers, all CRUD routes exist.
When viewing the Event controller, the data served by the index route is ordered by ascending date.
When viewing the entry file, the Event and Stage controllers are required and accessible with app.use().
Each route has been tested using Postman or another API testing tool of your choosing.
Before submitting, make sure you do a self review of your code, check for formatting, spelling, include comments in your code, and ensure you have a healthy commit history.

Make sure to submit your GitHub repository link on the submission page.
