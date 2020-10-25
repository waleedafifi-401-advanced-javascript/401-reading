# Component Composition

1. Can a parent component access the state of a child component?
  - Yes, you must first declare a reference in the parent component, then pass it as a reference attribute to the child. 

2. What can be passed along in a prop variable?
  - They are generally used to pass data from one component to another. 
  
3. How can a child component “know” the state of another component?
  - if they are passed as values as props to all the components that need to share the functionality. 

4. Which 3 things had you heard about previously and now have better clarity on?
  - It makes sense why we learned about ES6 classes now.  Wondering how many other frameworks also depend on ES6 classes as well.  
  - Coming from running npm i -g, it makes sense why some things would be globally scoped, and why other elements would be locally scoped. 
  - 

5. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
  - Really curious to know how HTML and javascrpt talk to eachtother again.  
  - Now that we are diving in more, is there more that we need to know to really make the front end talk to the back end, or are we just refining our knowledge base at this point?
  -  How do most people who are successful front end developers know where they fit in?  Do they start experimenting with what they like, and then develop a template to work with at a later date?

6. What are you most excited about trying to implement or see how it works?
  - Really excited to start seeing the front end come alive.  Really excited to see all of this hardwork come together. 

***

### Terms

1. Component props: let you split the UI into independent, reusable pieces, and think about each piece in isolation. 
3. Component state: is stored locally within a component and is not accessible from other components unless it's explicitly passed as props to it's sub components.
3. Application state: is stored globally through the app. 