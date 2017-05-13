## Week Two - Module 3 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. What's OAuth?
  * OAuth is Outside Authorization, a protocol that enables you to authenticate your users using external APIs.
2. What are some advantages/disadvantages of implementing OAuth?
  * Pros: More secure. You don't have to store sensitive user data in your database. It makes it easier to sign up, as users don't have to create an entirely new username and password. Less code to write.
  * Cons: You have to have a preexisting account before signing into your app. You have less flexibilty in how authentication is performed. Your app is dependent on another company's API.
  
3. How many exhanges of information need to take place before a user is authenticated with OAuth?
* Four
4. Why do we want to create services?
* Services communicate between the rest of our application and the external API. This compartmentalizes our app and follows single responsibility practices.
5. Why is it good practice to create PORO's with the data received from an API?
 * It makes it easier to access and modify the data, cuts down on the number of API requests you have to make, and speeds up your application.
6. What do we use VCR for? Why is it a good idea to use this tool?  
* VCRs let you save an incoming API request and reuse the data. This makes your tests run more quickly and also prevents your tests from hitting API rate limits.

#### Review  

7. What does HTTP stand for?
* Hyper Text Transfer Protocol
8. How do you create the following table in SQL? In Active Record?   
   (Users table with columns first_name, last_name, email, and age)  
   
`CREATE Table users (
   first_name varchar(200),
   last_name varchar(200),
   email varchar(200),
   age int,);`

* `rails g migration CreateUsers firstname, lastname, email, age:integer` `rake db:migrate`
9. Writing Files: given a text file located at "/Documents/pizza.txt", write code to read the file from the filesystem, then    write a new file at "/Documents/line_count.txt" containing the number of lines in the original file.
```
handle = File.read('/Documents/pizza.txt')

File.write('/Documents/line_count.txt', handle.lines.count)
```

#### Self Assessment  
Rate yourself on the following scale.  
4 I know and understand all these concepts and did not have to look anything up  
**3 I know and understand most of these concepts but had to look something up**  
2 I am uncertain about some of these concepts and had to look some things up ^^  
1 I am feeling lost about with these concepts and had to look many things up ^^  

^^ Please let an instructor know where you'd like support to catch you up. 



