## Week One - Module 3 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. What is `json`, what does it stand for, and why is it important?
  * JSON stands for Javascript Object Notation. It is a file format for transmitting data, derived from Javascript. It's organized in key-value pairs like Ruby hashes, and is designed to be machine and human readable for transmitting data across applications. 
2. What's the difference between `joins` and `includes` in ActiveRecord?
  * `joins` joins two tables together. `includes` does the same, but it additionally performs eager loading for any relationships of the data. This can eliminates the need to perform multiple database queries.
3. What's an API?
  * Application Programing Interface
4. How do we test an internal API (in general)?
  * With request and feature tests.
5. What are two different ways to customize your `json`?  
  * using Serializer or Jbuilder

#### Review  
6. What is an ORM, what does it stand for, and why is it helpful?  
  * Object Relational Model. It lets us recreate natural relationships from real world systems in an Object Oriented manner.
7. How do you create a record in the following table in SQL? In Active Record?   
   (Users table with columns first_name, last_name, email, and age)
  * `INSERT INTO users (first_name, last_name, email, age) VALUES ('James', 'Hill', 'j@.com', 30);`
  * User.create(first_name: 'James', last_name: 'Hill', email: 'j@.com', age: 30)
8. Given an array numbers = [1,2,3,4,5], find the sum of the doubles of all the numbers.
  * array.map{ |n| n * 2}.reduce(:+)

#### Self Assessment  
Rate yourself on the following scale.  
4  I know and understand all these concepts and did not have to look anything up  
**3  I know and understand most of these concepts but had to look something up **
2  I am uncertain about some of these concepts and had to look some things up ^^  
1  I am feeling lost about with these concepts and had to look many things up ^^  

^^ Please let an instructor know where you'd like support to catch you up. 
