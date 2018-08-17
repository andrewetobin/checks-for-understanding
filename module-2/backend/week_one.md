## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
As it relates to CRUD.
Post is used to create
Get is used to read
Put is used to update all data except id
Patch is used to update some data
Delete is used to delete

2. What is Sinatra?
It is a DSL in Ruby written to help write web applications

3. What is MVC?
Model View Controller is a design pattern for web applications.

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
because the routes are defined in the configuration. deviation from the conventions will not allow the program to work.

5. What types of variables are accessible in our view templates without explicitly passing them?
instance variables from the controller.

6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    erb :index
  end
  ```
  get '/horses' do
    @horses = Horse.all
    erb :"horses/index"
  end

7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

8. What's the purpose of ERB?
embedded ruby. to embed ruby cody into HTML to make it dynamic so it can render situation specific information to a webpage.

9. Why do I need a development AND test database?

10. What is CRUD and why is it important?
Create, Read, Update, Delete. all the functions necessary for a complete database.

11. What does HTTP stand for?
Hyper text Transfer Protocol

12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
<%   >  and <%=     >    the one with = will print the stuff inside.

13. What's an ORM? What does it do?
Object Relational Mapper. Helps to organize, manage, and analyze data.

14. What's the most commonly used ORM in ruby (Sinatra & Rails)?
ActiveRecord

15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
GET /restaurants renders all restaurants
GET /restaurants/new renders a new restaurant
POST /restaurants creates a new restaurant
GET /restaurants/:id  finds one restaurant
PUT /restaurants/:id updates one restaurant
DELETE /restaurants/:id deletes one restaurant
GET /restaurants/edit edits one restaurant

16. What's a migration?

17. When you create a migration, does it automatically modify your database?

18. How does a model relate to a database?
model creates an object for the database to store

19. What is the difference between `#new` and `#create`?
new makes a new object. create makes and new object and saves it to database.

20. Given a table named `animals`, What is the SQL query that will return all info from that table?
    `id     name        number_of_legs
    -----   ------      --------------
      1     panda       4
      2     giraffe     4
      3     whale       0
      4     bird        2
    `
SELECT * FROM animals;
21. Using the same table, What is the SQL query that will return only the animals that has 4 legs?
SELECT * FROM animals
   WHERE number_of_legs=4;



### Review Questions:  
22. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
CSV.foreach('./data/films.csv', headers: true, header_converters: :symbol) do |film|
  Film.create(
                  id:         film[:id],
                  title:       film[:title],
                  description: film[:description],
                )
end

23. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}
```
How would I add 'granola bar' to things you should have when hiking?
activities[:hiking][:supplies]+= 'granola bar'

24. What are the 4 Principles of OOP? Give a one sentence explanation of each.


### Self Assessment:
Choose One: (erase the others)

* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel overwhelmed by the content presented this week
