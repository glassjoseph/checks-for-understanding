## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?
  * `rails new project_name`
2. What do Models generally inherit from in rails?
  * `ActiveRecord::Base`
3. What do Controllers generally inherit from in a rails project?
  * `ApplicationController`
4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
  * resources :horses, only: [:view]
5. What rake task is useful when looking at routes, and what information does it give you?
  * `rake routes` - gives you the path prefixes, the HTTP Verb, the URI, and the Controller Action
6. What is an example of a route helper? When would you use them?
  * `link_to "See all horses", horses_path`  - They're useful to access routes without having to give the url, decreasing duplication and the number of changes made if the url is updated. 
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
  * `_path` returns the relative path, while `_url` returns the absolute path.
8. What are strong params and why are the necessary?
  * strong params are provided by a function that limits what parameters can be passed through forms. They allow you to accept only the parameters you are expecting, and prevent malicious code from being introduced by passing in extra parameters through forms.
9. What role does `form_for` play in helping us create our forms?
  * It is a rails helper that creates the form html for an existing object. It also validates that the form fields match the object's attributes.
10. How does `form_for` know where to submit the user's input?
  * From the object passed in to it.
11. Create a form using a `form_for` helper to create a new `Horse`.
  * ```
  <%= form_for @horse do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name %>
  <%= f.label :age %>
  <%= f.number_field :age %>
  
12. Why do we want to validate our models?
  * To make sure our objects are not created without all the required attributes. 
