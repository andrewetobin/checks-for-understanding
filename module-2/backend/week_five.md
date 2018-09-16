### Week 5 Questions

Re-pull from this repository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
**include the notice definition in the correct controller action and put the flash display in the layout page.**
2. Where is cart information/temporary information usually stored?
**in the session**
3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
**additional information to keep in the database, and deciding when to delete that information. would want to keep that info in we wanted to remind customer of their unchecked out cart to try and increase sales**
4. What is the purpose of the asset pipeline?
**how all of the assets and loaded up. loading up css, images, views, etc. the process of condensing them so they can be processed faster**
5. Why do we precompile our assets?
**to load faster**
6. What do each of the following tags do?

```ruby
<%= stylesheet_link_tag "application" %> **loads stylesheets**
<%= javascript_include_tag "application" %> **loads javascripts**
<%= image_tag "rails.png" %> > **loads images**
```
**helps to render in production**

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
**employers will be looking at them to see how well we document our work and our level of sincere interests in helping users**

8. What are the top four accessibility issues that we as developers should be aware of?
**hearing impaired, sight impaired, responsiveness on different sized viewports**
9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
**callback, possible string cleaning before the data is saved.**
10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```

11. What is the difference between a scope and a class method?


### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```


  12a. How would you add item with id of 48 with a quantity of 4?
  **hash[:cart] += "48" => 4**
  12b. How would you increase the quantity of item 29?
  **hash[:cart]["29"] + 4**
  12c. How would you find out how many items your user is thinking about purchasing?  **hash[:cart].values.sum**  

13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications? **having same method do different things in different classes to change dynamically**
14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel comfortable with the content presented this week
