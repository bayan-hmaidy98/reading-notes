# Save data in a local database using Room   

Apps that handle non-trivial amounts of structured data can benefit greatly from persisting that data locally. The most common use case is to cache relevant pieces of data so that when the device cannot access the network, the user can still browse that content while they are offline.

The Room persistence library provides an abstraction layer over SQLite to allow fluent database access while harnessing the full power of SQLite. In particular, Room provides the following benefits:

* Compile-time verification of SQL queries.
* Convenience annotations that minimize repetitive and error-prone boilerplate code.
* Streamlined database migration paths.

### Primary components
There are three major components in Room:

* The database class that holds the database and serves as the main access point for the underlying connection to your app's persisted data.
* Data entities that represent tables in your app's database.
* Data access objects (DAOs) that provide methods that your app can use to query, update, insert, and delete data in the database.

### Database
The following code defines an AppDatabase class to hold the database. AppDatabase defines the database configuration and serves as the app's main access point to the persisted data. The database class must satisfy the following conditions:

* The class must be annotated with a @Database annotation that includes an entities array that lists all of the data entities associated with the database.
* The class must be an abstract class that extends RoomDatabase.
* For each DAO class that is associated with the database, the database class must define an abstract method that has zero arguments and returns an instance of the DAO class.

### Entity 
By default, Room uses the class name as the database table name. If you want the table to have a different name, set the tableName property of the @Entity annotation. Similarly, Room uses the field names as column names in the database by default. If you want a column to have a different name, add the @ColumnInfo annotation to the field and set the name property. The following example demonstrates custom names for tables and columns:

```
@Entity(tableName = "users")
public class User {
    @PrimaryKey
    public int id;
    @ColumnInfo(name = "first_name")
    public String firstName;
    @ColumnInfo(name = "last_name")
    public String lastName;
}
```

### Index specific columns

If your app must support SDK versions that don't allow for using FTS3- or FTS4-table-backed entities, you can still index certain columns in the database to speed up your queries. To add indices to an entity, include the indices property within the @Entity annotation, listing the names of the columns that you want to include in the index or composite index. 

### Include AutoValue-based objects

When using classes annotated with @AutoValue as entities, you can annotate the class's abstract methods using @PrimaryKey, @ColumnInfo, @Embedded, and @Relation. When using these annotations, however, you must include the @CopyAnnotations annotation each time so that Room can interpret the methods' auto-generated implementations properly.


## Define relationships between objects 

* Intermediate data class

In the intermediate data class approach, you define a data class that models the relationship between your Room entities. This data class holds the pairings between instances of one entity and instances of another entity as embedded objects. Your query methods can then return instances of this data class for use in your app.

* Multimap return types

In the multimap return type approach, you don't need to define any additional data classes. Instead, you define a multimap return type for your method based on the map structure that you want and define the relationship between your entities directly in your SQL query.

### Accessing data with Room 
You can define each DAO as either an interface or an abstract class. For basic use cases, you should usually use an interface. In either case, you must always annotate your DAOs with @Dao

**There are two types of DAO methods that define database interactions:**

* Convenience methods that let you insert, update, and delete rows in your database without writing any SQL code.
* Database methods thatQuery methods that let you write your own SQL query to interact with the database.
 #### Insert
* The @Insert annotation allows you to define methods that insert their parameters into the appropriate table in the database.
* @Insert method must be either an instance of a Room data entity class annotated with @Entity or a collection of data entity class instances.
 #### Update
* The @Update annotation allows you to define methods that update specific rows in a database table. Similarly to @Insert methods, @Update methods accept data entity instances as parameters.
#### Delete
The @Delete annotation allows you to define methods that delete specific rows from a database table. Similarly to @Insert methods, @Delete methods accept data entity instances as parameters.
#### Query methods
The @Query annotation allows you to write SQL statements and expose them as DAO methods.