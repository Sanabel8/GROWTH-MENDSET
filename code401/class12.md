# Baeldung: Spring Request Mapping
* @RequestMapping.Simply put, the annotation is used to map web requests to Spring Controller methods.
* @RequestMapping — by Path: 
```
@RequestMapping(value = "/ex/foos", method = RequestMethod.GET)
@ResponseBody
public String getFoosBySimplePath() {
    return "Get some Foos";
}
```
* To test out this mapping with a simple curl command, run:

```curl -i http://localhost:8080/spring-rest/ex/foos```

* @RequestMapping — the HTTP Method
* The HTTP method parameter has no default.
```@RequestMapping(value = "/ex/foos", method = POST)
@ResponseBody
public String postFoos() {
    return "Post some Foos";
}
```
* To test the POST via a curl command:
```curl -i -X POST http://localhost:8080/spring-rest/ex/foos```

*  @RequestMapping With the headers Attribute
* @RequestMapping Consumes and Produces
* Single @PathVariable
```@RequestMapping(value = "/ex/foos/{id}", method = GET)
@ResponseBody
public String getFoosBySimplePathWithPathVariable(
  @PathVariable("id") long id) {
    return "Get a specific Foo with id=" + id;
}
```
* If the name of the method parameter matches the name of the path variable exactly , this can be simplified by using @PathVariable with no value.
*  Multiple @PathVariable
```@RequestMapping(value = "/ex/foos/{fooid}/bar/{barid}", method = GET)
@ResponseBody
public String getFoosBySimplePathWithPathVariables
  (@PathVariable long fooid, @PathVariable long barid) {
    return "Get a specific Bar with id=" + barid + 
      " from a Foo with id=" + fooid;
}
```
* Ambiguous Mapping Error: occurs when Spring evaluates two or more request mappings to be the same for different controller methods
*  New Request Mapping Shortcuts
@GetMapping
@PostMapping
@PutMapping
@DeleteMapping
@PatchMapping
* These new annotations can improve the readability and reduce the verbosity of the code.
















