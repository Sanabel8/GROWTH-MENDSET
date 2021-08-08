Spring App Basics
# Serving Web Content with Spring MVC
## What You Will Build :  build an application that has a static home page and that will also accept HTTP GET requests at: http://localhost:8080/greeting.
* The URL might then be http://localhost:8080/greeting?name=User.

## What You Need
1. A favorite text editor or IDE
2. JDK 1.8 or later
3. Gradle 4+ or Maven 3.2+

## How to complete this guide

1. Download and unzip the source repository for this guide, or clone it using Git: git clone https://github.com/spring-guides/gs-serving-web-content.git

2. cd into gs-serving-web-content/initial

3. Jump ahead to Create a Web Controller.

When you finish, you can check your results against the code in ```gs-serving-web-content/complete```

## Create a Web Controller
1.  identify the controller by the @Controller annotation
2. View is responsible for rendering the HTML content. 

@GetMapping : annotation ensures that HTTP GET requests to /greeting are mapped to the greeting() method.
@RequestParam binds the value of the query string parameter name into the name parameter of the greeting() method. 

Spring Boot Devtools:
1. Enables hot swapping.

2. Switches template engines to disable caching.

3. Enables LiveReload to automatically refresh the browser.

4. Other reasonable defaults based on development instead of production.

* Building an executable jar makes it easy to ship, version, and deploy the service as an application throughout the development lifecycle, across different environments, and so forth.
* If you use Gradle, you can run the application by using ./gradlew bootRun.
* Static resources, including HTML and JavaScript and CSS
*  By default, Spring Boot serves static content from resources in the classpath at /static (or /public).

Spring MVC and Thymeleaf

* @Controller classes are responsible for preparing a model map with data and selecting a view to be rendered.
* Spring MVC calls the pieces of data that can be accessed during the execution of views model attributes. The equivalent term in Thymeleaf language is context variables.
* There are several ways of adding model attributes to a view in Spring MVC:
1. Add attribute to Model via its addAttribute method
2. Return ModelAndView with model attributes included
3. Expose common attributes via methods annotated with @ModelAttribute

*  Request parameters are passed from the client to server like:``` https://example.com/query?q=Thymeleaf+Is+Great!```
* If you access multivalued parameter with ${param.q} you will get a serialized array as a value.

























