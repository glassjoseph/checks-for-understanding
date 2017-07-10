## Week Two - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What is Webpack and why is it useful?
  - Webpack does the job of Rails' Asset Pipeline, prepping your code for better web transfer by compiling files into one file, minifying, uglifying, etc.  
2. When do you want to use event delegation?
  - When you want to check something dynamically created, you need to delegate event listening to a parent element, as listeners are bound only on elements that exist when the document is ready. 
  
3. What's one difference between ES5 and ES6?
- Syntax is significantly different, the context of `this` also changes in some instances. 

4. How are you using the MVC design pattern in your Quantified Self project?
- We're mimicing the Rails MVC in JS, mapping more or less the same pattern.

5. How do you execute raw SQL in node?
- You can use `knex.raw` to execute SQL

6. What's a callback function and what are some reasons when we use/need callback functions?
- Callback functions are how you control flow in your code. You need to wait for certain actions to be performed before executing later dependent functions, and callbacks are one way of determining when to wait and when to move forward.

7. What is CORS?
- It's a way to allow requesting of resources from another outside domain.
8. What are some steps to avoid CORS?
 - Make sure your backend server accept CORS request.

#### Review  

9. Why do people say "HTTP is stateless"?
- Because no information is carried over from one HTTP request to another. Each one is independent.
10. What is a RESTful API?
- It is an API that follows the Representational State Transfer pattern. Basically you build an api that connects the standard http verbs to the corresponding controller actions of index, show, create, delete, update etc. 

11. What are some main characteristics of a team following an agile workflow?
- Quick iteration, minimum viable product, changing and adaptable product specs.

12. What are some advantages/disadvantages to using OAuth to authenticate a user?
 - Advantages: Secure, easy, fast.
 - Disadvantages: Less control over details, your app is more dependent on outside gems.
