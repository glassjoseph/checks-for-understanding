## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's the most useful thing you learned from completing the intermission week work?
- Learning the basic syntax of JS and the major differences between it and Ruby was very helpful. Learning that JS requires explicit returns and that to make a copy of an array, you need to use Array.prototype.slice() was really useful.

2. What are some tools to help debug JavaScript code?
- Pryjs, debugger and the console.

3. What are some tools you need in order to unit test your JavaScript?
- chai, mocha

4. What is the syntax for invoking a function?
```
function addTwo (a, b) {
  return (a + b)
  }
  
  addTwo (3, 5)
```

5. What's the difference between `==` and `===` in JavaScript?
-  `==` is Abstract Equality, and will consider '1' and 1 to be equal, even though they are different data types.
-  `===` is Strict Equality, and will not consider the two objects of different data types to be equal. 

6. What's the difference between asynchronous and synchronous JavaScript? 
- Synchronous means running in chronological order, each line executed nore or less in the order it is written. 
- Asynchronous means that JS can start a line of code (like a http request, for example), move on to another line to start executing, and then return back once the first line has finished and then send the data along. This asynchonicity is controlled by using either callbacks or by using promises.

7. How do we setup a route when creating an API with Node and Express?
  ```
  app.get("/api/v1/things", (request, response)  => {
  ThingsController.index(request, response)
  })
  ```

8. What do we use Knex for?
- Knex is a DSL like ActiveRecord that we can use to interact with our models and database. It is more lightweight than AR and is not a full-fledged ORM, but it is still very useful.

9. What's `npm` and what do we use it for?
- `npm` is "Node Program Manager" and is used to install and manage dependencies, much like we use rvm.

#### Review  
10. What's the MVC design pattern? Describe each part of MVC?
 - Model View Controller.
 - Model: The model interacts directly with the database, CRUDing objects and data as directed by the controller.
 - Controller: The controller recieves requests and depending on the request, calls the models or passes information on to the views.
 - View: The view receives information from the controller and organizes it in a way the browser can render. 

11. What is AJAX? What are some benefits of using AJAX?
- Asynchronous Javascript And XML. The benefit of AJAX is that it lets us make asynchronous requests, which lets load server info behind the scenes while the user continues browsing the page. You can also update the page without a new HTTP cycle.

12. What's a background worker? When would we want to use a background worker?
- A background worker makes a queue of tasks that need to be performed ranked by priority, and then when there is free memory, the worker can finish tasks in the background without making the user wait. This is useful for any long task like a file upload, where we want to let the user continue browsing and finish the task whenever convenient. It can also be used for routine tasks.
