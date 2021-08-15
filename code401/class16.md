Spring Security overview
* All of the principles apply equally well to applications that do not use Spring Boot.
* Authentication : The main strategy interface for authentication is AuthenticationManager
```public interface AuthenticationManager {

  Authentication authenticate(Authentication authentication)
    throws AuthenticationException;
}
```
* AuthenticationException is a runtime exception ,depending on the style or purpose of the application


## Web Security
* Spring Security in the web depend on Servlet Filters
1. The client sends a request to the application
2.  container decides which filters and which servlet apply to it 
* one servlet can handle a single request
* but filters form a chain, so they are ordered
* Spring Security is installed as a single Filter ,and its concrete type is FilterChainProxy
*  the security filter is a @Bean in the ApplicationContext
* A vanilla Spring Boot application with no custom security configuration has a several (call it n) filter chains, where usually n=6.
* The first (n-1) chains are there just to ignore static resource patterns, like /css/** and /images/**, and the error view: /error

## Method Security
* Spring Security offers support for applying access rules to Java method executions.
* Spring Security is  type of “protected resource”
* The first step is to enable method security :
```@SpringBootApplication
@EnableGlobalMethodSecurity(securedEnabled = true)
public class SampleSecureApplication {
}
```
then :
* This example is a service with a secure method
```@Service
public class MyService {

  @Secured("ROLE_USER")
  public String secure() {
    return "Hello Security";
  }

}
```

* annotations that you can use on methods to enforce security constraints, notably @PreAuthorize and @PostAuthorize
* @PreAuthorize and @PostAuthorize :  let you write expressions containing references to method parameters and return values
## Working with Threads
* Spring Security is fundamentally thread-bound
* The basic building block is the "SecurityContext"
* If you need access to the currently authenticated user in a web endpoint, you can use a method parameter in a @RequestMapping
this annotations pulls the current Authentication out of the SecurityContext and calls the getPrincipal() method on it to yield the method parameter. 
```@RequestMapping("/foo")
public String foo(@AuthenticationPrincipal User user) {
  ... // do stuff with user
}
```

Spring Auth cheat sheet
1. set up a user model and repo
2. create a controller for that model
3. UserDetailsServiceImpl implements UserDetailsService
4. ApplicationUser implements UserDetails
5. WebSecurityConfig extends WebSecurityConfigurerAdapter
6. WebSecurityConfig extends WebSecurityConfigurerAdapter
7. login page
