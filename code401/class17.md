# Read (no need to do) this tutorial on OAuth
* It starts with a simple, single-provider single-sign on
* The samples are all single-page apps using Spring Boot and Spring Security on the back end.
* They also all use plain jQuery on the front end. 
* All samples are implemented using the native OAuth 2.0 support in Spring Boot.
* There are several samples building on each other, adding new features at each step:
. simple
. click.
. logout.
. two-providers.
. custom-error.
* Each app can be imported into an IDE.
*  You can run the main method in SocialApplication to start an app. 
* You can also run all the apps on the command line using mvn spring-boot:run
## Single Sign On With GitHub
* Creating a New Project in the https://start.spring.io
* Add a Home Page by create index.html in the src/main/resources/static folder.
* Securing the Application with GitHub and Spring Security by add Spring Security as a dependency.
* you need to configure your app to use GitHub as the authentication provider. To achieve this, do the following:
1. Add a New GitHub app
- select New OAuth App 
- Register a new OAuth application 
- Enter an app name and description 
- enter your app’s home page  http://localhost:8080 
- indicate the Authorization callback URL as http://localhost:8080/login/oauth2/code/github
- click Register Application.

2. Configure application.yml
* add the following for application.yml
```spring:
  security:
    oauth2:
      client:
        registration:
          github:
            clientId: github-client-id
            clientSecret: github-client-secret
# ...
```

3. Boot up the application
* you should be redirected to login with GitHub and  and accept any authorizations you are asked to make and the home page will be visible.
* it uses the authorization code grant to obtain an access token from GitHub (the Authorization Server).
*  This cookie (JSESSIONID by default) is a token for your authentication details for Spring
## Add a Welcome Page
index.html
```<div class="container unauthenticated">
    With GitHub: <a href="/oauth2/authorization/github">click here</a>
</div>
<div class="container authenticated" style="display:none">
    Logged in as: <span id="user"></span>
</div>
```
* / since that’s the page you just made dynamic, with some of its content visible to unauthenticated users

* /error since that’s a Spring Boot endpoint for displaying errors, and

* /webjars/** since you’ll want your JavaScript to run for all visitors, authenticated or not
## Add a Logout Button
index.html
```<div class="container authenticated">
  Logged in as: <span id="user"></span>
  <div>
    <button onClick="logout()" class="btn btn-primary">Logout</button>
  </div>
</div>
```
## Adding an Error Page for Unauthenticated Users
. Switching to GitHub
. Detecting an Authentication Failure in the Client
. Adding an Error Message
















































