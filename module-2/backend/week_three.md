## Week Three Recap
### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
**rails new project name**
2. What do Models generally inherit from in rails?
**ApplicationRecord**
3. What do Controllers generally inherit from in a rails project?
**ApplicationController**
4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
**resources :horses only [:show]**
5. What rake task is useful when looking at routes, and what information does it give you?
**rake routes, it gives the the path helpers, the url, and action**
6. What is an example of a route helper? When would you use them?
**merchants_path would be a route helper to the merchant index page. they are helpful in writing tests and direction in controller**
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
8. What are strong params and why are they necessary?
**to limit what comes into the object. addded security for database**
9. What role does `form_for` play in helping us create our forms?
**form_for allows us to make forms easier and assigns model attributes from the form**
10. How does `form_for` know where to submit the user's input?
**from the instance variable that is being passed from the controller**
11. Create a form using a `form_for` helper to create a new `Horse`.
**<%= form_for @horse do |f| %>
<%= f.label :title %>
<%= f.text_field :title %>
<%= f.label :breed %>
<%= f.text_field :breed %>
<%= f.submit%>**

12. Why do we want to validate our models?
**to make sure they have all of the relationships set up correctly so that we can actually perform data analysis methods on the models from the tables**
13. What are the steps of the DNS lookup?
**computer tries to find IP address from cached info, will go to ISP next, and then more specific servers to find IP address for URL address typed into browser.**

### Review Questions
14. Within a feature test and given the following HTML, write the code necessary to target the following section and check the person's name?

  `<section id="personal-info">
    <h3><%= @person.name%></h3>
   </section>
  `
  **within .css(personal-info)**
15. How would you call the method `prance` from within the method `move` on a `Horse` instance?
**def move
  prance
end**
16. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?
**to return true: furniture[:purchased], to return 3: furniture[:table][:height]**
17. What is inheritance?
**classes can inherit methods from other classes. class Dog < class Animal, in this setup class Dog has access to the methods in class Animal.**

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel comfortable with the content presented this week
