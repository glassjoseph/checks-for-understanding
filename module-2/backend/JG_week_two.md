## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
* ActiveRecord translates between your database and your ruby controller, taking ruby commands and executing them in SQL, and taking SQL tables and creating ruby objects from them. 
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
* You can call all of the ActiveRecord methods on Team, like Team.find(id) Team.find_by, Team.create, Team.delete, etc. You have access to them because Team is inheriting from ActiveRecord, and so has all of its methods automatically included.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

```
team = Team.find(4)
name = team.name
owner = team.owner
```

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

`owner = Owner.find(Team.owner_id)`

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
* One teacher will have many students. 
6. Define foreign key, primary key, and schema.
* The primary key is the unique identifier of each table row in a table. The foreign key is an imported primary key that belongs to another table, which identifies the row on that 'foreign' table. A schema is a ruby representation of your database. 
7. Describe the relationship between a foreign key on one table and a primary key on another table.
* the foreign key on one table is the primary key of the table it comes from.
8. What are the parts of an HTTP response?
* A header, response code, and body.

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
* .all - lists all objects in a table
* .find - lets you find object by its id
* .find_by(attribute: value) - finds object by any of its characteristics
* .update - lets you change the value of a certain attribute
* .destroy - deletes an object from your table

2. Name your three favorite ActiveRecord rake tasks and describe what they do.
* rake db:create - creates database
* rake db:seed - seeds database with your seed file
* rake db:drop - purges and deletes your database

3. What two columns does `t.timestamps null: false` create in our database?
* created_at, and updated_at
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
* Teacher class will belong_to :school, School class has_many :teachers
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)
* You will need to create a migration to add School's id column as a foreign key to the Teachers table
6. Give an example of when you might want to store information besides ids on a join table.
* If there was a different unique identifier that could be used instead, such as unique names. 
7. Describe and diagram the relationship between patients and doctors.
* Patient belongs_to :doctor, Doctor has_many :patients
8. Describe and diagram the relationship between museums and original_paintings.
* Museum has_many :original_paintings, OriginalPainting belongs_to :museum.
9. What could you see in your code that would make you think you might want to create a partial?
* If you had to create the same html over and over for multiple views, it might be better to use a partial to define it in just one layout file and then yield in anything you need to add.
