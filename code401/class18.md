# Many to many relationships
* @ManyToMany annotation 
* any given employee can be assigned to multiple projects and a project may have multiple employees working for it, leading to a many-to-many association between the two.
* Let's assume we have an already created database with the name spring_hibernate_many_to_many.
* The model classes Employee and Project need to be created with JPA annotations:
```@Entity
@Table(name = "Employee")
public class Employee { 
    // ...
 
    @ManyToMany(cascade = { CascadeType.ALL })
    @JoinTable(
        name = "Employee_Project", 
        joinColumns = { @JoinColumn(name = "employee_id") }, 
        inverseJoinColumns = { @JoinColumn(name = "project_id") }
    )
    Set<Project> projects = new HashSet<>();
   
    // standard constructor/getters/setters
}
```
```@Entity
@Table(name = "Project")
public class Project {    
    // ...  
 
    @ManyToMany(mappedBy = "projects")
    private Set<Employee> employees = new HashSet<>();
    
    // standard constructors/getters/setters   
}
```
* both the Employee class and Project classes refer to one another, which means that the association between them is bidirectional.
* In order to map a many-to-many association, we use the @ManyToMany, @JoinTable and @JoinColumn annotations.
* The @JoinColumn annotation is used to specify the join/linking column with the main table.
* In the Project class, the mappedBy attribute is used in the @ManyToMany annotation to indicate that the employees collection is mapped by the projects collection of the owner side.
