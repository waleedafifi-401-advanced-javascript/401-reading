


# Hooks Api

### Questions
Why do we not need more .html pages in a multi-page React app?
  - React will use routing and links to populate the front end.  Meaning you have the ability to set the header, footer, and content, and add other information down the line at the app level. 
If we wanted a component to show up on every page, where would we put it and why?
  - You would put the element in the app level of the page.  That is generally where most devs make the choice to render the footer and the header. 
  - Also, Outside the <BrowserRouter/>


***

### Terms

1. Composition - A natural pattern of the component model. It's how we build components from other components, of varying complexity and specialization through props. Depending on how generalized these components are, they can be used in building many other components.
2. Children / Child Components - allow you to pass components as data to other components, just like any other prop you use. ... The special thing about children is that React provides support through its ReactElement API and JSX
3. Hash Routing - Hash value will be handled by react router. It is used to support legacy browsers which usually doesn't support HTML pushState API ✅ It doesn't need any configuration in server to handle routes ✅ This route isn't recommended by the team who created react router package.
4. Link Routing - The primary way to allow users to navigate around your application. <Link> will render a fully accessible anchor tag with the proper href.

  A <Link> can know when the route it links to is active and automatically apply an activeClassName and/or activeStyle when given either prop. The <Link> will be active if the current route is either the linked route or any descendant of the linked route. To have the link be active only on the exact linked route, use <IndexLink> instead or set the onlyActiveOnIndex prop.



Which 3 things had you heard about previously and now have better clarity on?
  - Have a much better understanding of how routing actually works.  
  - I also have a much more clear idea of where to start laying out elements when building a website. 
  -  Finally, I have a much better understanding of exactly how the props are being passed along many different elements. 
Which 2 things are you hoping to learn more about in the upcoming lecture/demo?
  - Curious to know how the front end and back end are talking to eachother in React.
  - At the same time, also curious to know what kind of databases react uses or prefers to use. 
What are you most excited about trying to implement or see how it works?
  - I'm really curious to be able to see the effect hook in action. 
*** 
