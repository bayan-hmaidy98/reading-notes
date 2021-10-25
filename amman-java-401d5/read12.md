## Spring RequestMapping

### RequestMapping Basics

1. By path: 

`@RequestMapping(value = "/ex/foos", method = RequestMethod.GET)

@ResponseBody

public String getFoosBySimplePath() {

    return "Get some Foos";

}`

2. The HTTP method: ther is **no default** value for methods. We need to specify it.

`@RequestMapping(value = "/ex/foos", method = POST)

@ResponseBody

public String postFoos() {

    return "Post some Foos";

}`

### RequestMapping and HTTP Headers

1. With the headers attribute: it's used to limit the options for the mapping. We can specify one head or more.

`@RequestMapping(value = "/ex/foos", headers = "key=val", method = GET)

@ResponseBody

public String getFoosWithHeader() {

    return "Get some Foos with Header";

}`
 
2. Consumes and Produces: requests can be mapped based on its Accept **header**, till Spring 3.1 was established and @RequestMapping annotation now has the produces and consumes attributes.

`@RequestMapping(

  value = "/ex/foos", 

  method = RequestMethod.GET, 

  produces = "application/json"

)

@ResponseBody

public String getFoosAsJsonFromREST() {

    return "Get some Foos with Header New";

}`

### RequestMapping With Path Variables

1. Single path variable: If the name of the method parameter matches the name of the path variable exactly, then this can be simplified by using @PathVariable with no value as the following 

`@RequestMapping(value = "/ex/foos/{id}", method = GET)

@ResponseBody

public String getFoosBySimplePathWithPathVariable(

  @PathVariable String id) {

    return "Get a specific Foo with id=" + id;

}`

2. Multiple @PathVariable: separate them by comma. 
3. @PathVariabe with regex if only want to specify special value for mapping. 

### RequestMapping With Request Parameters

It's used when maping a request to a URI

`@RequestMapping(value = "/ex/bars", params = "id", method = GET)

@ResponseBody

public String getBarBySimplePathWithExplicitRequestParam(

  @RequestParam("id") long id) {

    return "Get a specific Bar with id=" + id;

}`

### RequestMapping Corner Cases

It can be applied for: 
1. Multiple Paths Mapped to the Same Controller Method
2. Multiple HTTP Request Methods to the Same Controller Method
Fallback for All Requests using * 

## CrudRepository, JpaRepository, and PagingAndSortingRepository in Spring Data

**Every repository in Spring Data extends the generic Repository interface, but beyond that, they do each have different functionality.** Each name describes the methods used in each Repository.

### CrudRepository
We use it when there is no need for JpaRepository and PAgingAndSortingRepository. It's functionality: 
save()
findeOne()
findAll()
count()
delete()
exists()


### PagingAndSortingRepository

This interface extends **CrudRepoistory**. It provides findAll() method. 

###  JpaRepository 
This interface extends PagingAndSortingRepository. All methods in CrudRepository **exists** in this interface. Methods provied in: 
findAll(), findAll(..)
save()
flush()
saveAndFlush(..)
deleteInBatch(..)

