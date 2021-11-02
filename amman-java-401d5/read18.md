
# Read: 18 - Web App Security

#### ______________________________________________________

# Hibernate Many to Many

In this Read, we'll have a quick look at how the `@ManyToMany` annotation can be used for specifying this type of relationships in Hibernate.

Let's start with a simple Entity Relationship which is the many-to-many association between two entities `employee` and `project`:

In this scenario, any given `employee` can be assigned to `multiple projects` and a `project` may have `multiple employees` working for it, leading to a many-to-many association between the two.

We have an `employee` table with `employee_id` as its primary key and a `project` table with `project_id` as its primary key. 
A join table `employee_project` is **required** here to connect both sides.

## The Model Classes

The model classes Employee and Project need to be created with JPA annotations:
```
@Entity
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

```
@Entity
@Table(name = "Project")
public class Project {    
    // ...  
 
    @ManyToMany(mappedBy = "projects")
    private Set<Employee> employees = new HashSet<>();
    
    // standard constructors/getters/setters   
}
```

* **As we can see, both the Employee class and Project classes refer to one another, which means that the association between them is bidirectional.**

In order to map a many-to-many association, we use the `@ManyToMany`, `@JoinTable` and @`JoinColumn` annotations. Let's have a closer look at them.

The `@ManyToMany` annotation is used in both classes to create the many-to-many relationship between the entities.

This association has two sides i.e. the owning side and the inverse side. In our example, the owning side is Employee so the join table is specified on the owning side by using the `@JoinTable` annotation in Employee class. The `@JoinTable` is used to define the join/link table. In this case, it is **Employee_Project**.

The @`JoinColumn` annotation is used to specify the join/linking column with the main table. Here, the join column is `employee_id` and `project_id` is the **inverse** join column since Project is on the **inverse** side of the relationship.

In the Project class, the `mappedBy` attribute is used in the `@ManyToMany` annotation to indicate that the employees collection is mapped by the projects collection of the owner side.