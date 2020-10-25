# Reading: <Login /> and <Auth />

### role-based access control (RBAC)
Role-based access control (RBAC) restricts network access based on a person's role within an organization and has become one of the main methods for advanced access control. The roles in RBAC refer to the levels of access that employees have to the network. Using RBAC will help in securing your company’s sensitive data and important applications.

### advantages
- Reducing administrative work and IT support.
- Maximizing operational efficiency.
- Improving compliance.


### Question answer
1. Why is the Context API useful?
This context idea, allows use to pass props from parent to grand child and beyond without the need of useless prop drilling.

2. Can a component outside of a provider get its context?
Negative, context gets one provider and componets get its context from subscribing

3. What are some common use cases for using the Context API?
When there are some global settings and features that you want to reapply to multiple components

4. Describe “Context Hell”
Having multiple components and multiple nested componets that require common / same functions and state.

### Vocabulary Terms
1. **global state:** State at the highest level, that all child components can access
2. **global context:** State and information stored at a central location for ease of use with subscribed components
3. **provider:** Provider is the overall React.Context component that is delivering the context to its subscriber
4. **consumer:** Consumer is the one who utilizes the information stored in the contexts
