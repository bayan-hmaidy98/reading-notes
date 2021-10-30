## Spring Security Architecture 

Application security is divided to two main parts: 

1. Authentication: who are you?

![](https://c.tenor.com/iKg6Y8j_TWMAAAAM/who-are-you.gif)

2. Authorization: what are you allowed to do?

### Authentication: 

When implementing AuthenticationManager, one of the following would happen: 
1. return true (Authentication)
2. return AuthenticationException (false)
3. return null.

You can implement AuthenticationManager using ProviderManager wich **provides** one more method to see if the query supports the Authentication type.

### Customizing Authentication Managers

In order to get quickly common authentication manager, AuthenticationManagerBuilder can be used as following:

`@Configuration
public class ApplicationSecurity extends WebSecurityConfigurerAdapter {

   ... // web stuff here

  @Autowired
  public void initialize(AuthenticationManagerBuilder builder, DataSource dataSource) {
    builder.jdbcAuthentication().dataSource(dataSource).withUser("dave")
      .password("secret").roles("USER");
  }

}`

**Note** that @Override is only used to build **local** 

### Authorization
 
We **can't step** into Authorization unless 
Authentication is successful. We use AccessDecisionManager. ConfigAttribute is a decoration for AccessDecisionVoter and it also provides with some metadata to **know** the level of permission to access the Object. Since Servlet is an API that provides many interfaces and classes including documentation, `when client sends a request to the application, and the container decides which filters and which servlet apply to it based on the path of the request URI.`

Now lets get back to Spring Security, spring security installs only as single filter in the chain. Also, note that the spring security can has inside it many filters. 

FilterChainProxy can has many containers, `the Spring Security filter contains a list of filter chains and dispatches a request to the first chain that matches it.`

### Creating and Customizing Filter Chains

Adding WebSecurityConfigurerAdapter Bean enable us to define other rules with lower order. Also, Each application **differs** in its access rules. 

### Request Matching for Dispatch and Authorization

WebSecurityConfigurerAdapter is a security filter chain decides whether if there is a **need** to  apply HTTP request or not. 

