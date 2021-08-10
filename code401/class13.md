Related data in Spring (focus on the relationship annotations, not the curl requests)
# Working with Relationships in Spring Data REST
## 1. Overview
how to work with relationships between entities in Spring Data REST.
association resources that Spring Data REST exposes for a repository
## 2. One-to-One Relationship
#### 2.1. The Data Model
* The @RestResource annotation is optional and can be used to customize the endpoint.
* We must be careful to have different names for each association resource. 
* The association name defaults to the property name and can be customized using the rel attribute of @RestResource annotation
* If we were to add the secondaryAddress property above to the Library class, we would have two resources named address, and we would encounter a conflict.
```@OneToOne
@JoinColumn(name = "secondary_address_id")
@RestResource(path = "libraryAddress", rel="address")
private Address secondaryAddress;
```
#### 2.2. The Repositories
* In order to expose these entities as resources, let's create two repository interfaces for each of them, by extending the CrudRepository interface:
```public interface LibraryRepository extends CrudRepository<Library, Long> {}```
```public interface AddressRepository extends CrudRepository<Address, Long> {}```
#### 2.3. Creating the Resources
* Note that if you're using curl on Windows, you have to escape the double-quote character inside the String that represents the JSON body:
```-d "{\"name\":\"My Library\"}"```
#### 2.4. Creating the Associations
* After persisting both instances, we can establish the relationship by using one of the association resources.
* This is done using the HTTP method PUT

## 3. One-to-Many Relationship
* A one-to-many relationship is defined using the @OneToMany and @ManyToOne annotations and can have the optional @RestResource annotation to customize the association resource.
#### 3.1. The Data Model
To exemplify a one-to-many relationship, let's add a new Book entity that will represent the “many” end of a relationship with the Library entity:
```
@Entity
public class Book {

    @Id
    @GeneratedValue
    private long id;
    
    @Column(nullable=false)
    private String title;
    
    @ManyToOne
    @JoinColumn(name="library_id")
    private Library library;
    
    // standard constructor, getter, setter

    @OneToMany(mappedBy = "library")
    private List<Book> books;
}
```
#### 3.2. The Repository
```public interface BookRepository extends CrudRepository<Book, Long> { }```

#### 3.3. The Association Resources
* create a Book instance first by using the /books collection resource
* associate the book with the library created in the previous section by sending a PUT request to the association resource that contains the URI of the library resource
* To remove an association, we can use the DELETE method on the association resource

## 4. Many-to-Many Relationship
* A many-to-many relationship is defined using @ManyToMany annotation, to which we can add @RestResource.

# Baeldung: Spring Integration Testing
## Overview
Integration testing plays an important role in the application development cycle by verifying the end-to-end behavior of a system.
 



























