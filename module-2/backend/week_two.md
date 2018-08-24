## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
**ActiveRecord is able to take more user friendly commands and formulate the SQL queries. It also is able to formulate the queries no matter what version of SQL is being used.**
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
**We have access to all of the ActiveRecord methods becuase they are being inherited into class Team. We have access to them by calling the ActiveRecord methods on attributes of the Team class, including any relational connections class Team has to other classes.**

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
**team = Team.find(4) to find the team with the id of 4. team.name  Owner.find(team.owner_id)**
4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
**Team.find(4).owner**
5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
**Depending on the school setup, elementary school where students are with same teacher all day, teacher has_many :students and student belongs_to :teacher. After elementary school where students have multiple teachers throughout the day, teacher has_many :students and student has_many :teachers.**
6. Define foreign key, primary key, and schema.
**primary key is a unique id number for an instance of a class. a foreign key is when a class belongs to another class, it will have multiple ids of another class in its table. those ids come from another table and are termed foreign keys. multiple foreign keys can be duplicated in the class that belongs to another. a schema shows the current structure of the database.**
7. Describe the relationship between a foreign key on one table and a primary key on another table.**primary key is a unique id number for an instance of a class. a foreign key is when a class belongs to another class, it will have multiple ids of another class in its table. those ids come from another table and are termed foreign keys. multiple foreign keys can be duplicated in the class that belongs to another.**
8. What are the parts of an HTTP response? **status code, headers, empty line, optional body**


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database? **created_at and updated_at**
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers? **most typically, school has_many :teachers and teacher belongs_to :school.**
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
6. Give an example of when you might want to store information besides ids on a join table. **when other information is needed at for computing or rendering**
7. Describe and diagram the relationship between patients and doctors. **patient belongs_to :doctor, Doctor has_many :patients**
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial? **when different websites utulize the same exact code**

### Self Assessment:
Choose One:

* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel confident about the content presented this week
* I feel comfortable with the content presented this week
* I feel overwhelmed by the content presented this week
* I feel quite lost by the content presented this week
