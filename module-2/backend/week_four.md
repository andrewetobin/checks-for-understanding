## Week Four Recap
### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie? **a piece of data on the client side to help mimic state by keeping information**
2. What’s the difference between a session and a cookie? **session used to mimic state in between HTTp requests, session will be destroyed after a session ends, while cookies are stored on users computer so browser can have access to that info everytime the user logs into a site.**
3. What’s a flash and when do you want to use flashes? **flash is a notice that informs client that certain actions have occurred, such as creating an account, being logged in, editing something, creating something, etc. It only last for the duration of one HTTP request cycle.**
4. Why do people say “HTTP is stateless”? **each request and response is treated as new and not with any previous info exchanged to know who the client or server are.**
5. What’s authentication? Explain. **the ability to check someone's credentials on a website.**
6. What’s the difference between authentication and authorization? **authorization is allowing access of certain pages and abilities based on who the logged in user is.**
7. What’s a before filter? **a method that runs before a controller action or set of actions. an example would be, before a certain controller action make sure the current user is logged in. makes sure that client is only accessing the pages they have permission for.**
8. How do we keep track of a user once they’ve logged in? **a session, helps to keep track of who the user is. current_user method in the application controller**
9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches? **generally namespace a resource for an admin.**
10. At a high level, what tools can you use to implement authorization? How would you use them? **assign roles to different types of users, through enums**
11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum? **enums set up roles, statuses, and other ways to differentiate types of data. data type needs to be an integer, declared in the model**
12. What are some strategies you can use to keep your views DRY? **the use of partials, before filters, pass in variables, repetitive code to a minimum.**


### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  
**hashes = [{holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
{holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
{holiday: {name: "Hanukkah", supplies: ["Menorah"]}}]
sorted_holidays = hashes.map { |hash| hash[:holiday][:name]}.sort**
14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?
**"300.00".to_i, money = "$300", money[1..-1].to_i**


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose Two:
* I feel comfortable with the content presented this week
* I feel overwhelmed by the content presented this week
