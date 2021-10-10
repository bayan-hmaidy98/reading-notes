## Pachages and Import

As we mentioned earlier, class name **must** match file name, package name **must** match folder name. Packages are the same as directories. Thay are made to group Java classes. 

#### Package declaration takes the first statement in the java source file.

### Package declaration syntax 

`
package directory_name; // optional
import class/classes_name; //optional
`

### Import

Import can hace 3 options: 
1. Make all the classes visible (*), even if only one class is used. 
2. Make on class visible. 
3. import it without using (import) keyword Like the following example:
> class ImportTest {
    public static void main(String[] args) {
        javax.swing.JOptionPane.showMessageDialog(null, "Hi");
        System.exit(0);
    }
}

Notes: 
1. Importing all the classes won't affect the size of the file, we have mentioned that in today's lecture and the Instructor Hana' said classed don't occupy a place in memory. Only objects do. 

2. Back to the first note, it also won't affect the efficiency when importing all the classes. 

3. Importing all the classes is pretty easier when: 
a. Getting back and delete the unused classes.
b. It prevents the incorrect naming accidents.
c. Save your time in updating the list of imports.

4. Only the packages that are visible while importing. Subpackages are not. 

5. Classes in Java language are visible. They don't require to be imported.

6. Order in import list is not **required.** 

### NetBeans 

1. Default package name is the same as project name and it can be changed. 

2. Fix Import is used in case you can't recall the classes you want to import. 

## A Guide to Java Loops

1. For loop
It's used in a specified condition related to the counter and of course the counter is modified to exit the loop after numberof times. It can be labled in case of nested loops. 

2. Enhanced for loop
It's functionality is the same as the ordinary for loop. The only differnce is that it has simpler srtucture. 

> for(Type item : items)
> statement;

3. While loop

It's working when a boolean expression is true (passed in). 

4. Do-While loop

It's thesame as while loop, but this one execute the statement or block of statements one time at least. This because it's condition is at the bottom. 

