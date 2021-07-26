# Forms

What are forms?
A document that have questions and needed to be filled from someone in order to collect data. HTML can be used to build form and be used in the website. 

## What are the types of **form controls** used to collect information from vusutors to the website?
1. Adding texts

a. Text input: Single line text (Usernames and emails).
b. Password input: Also single line but it **masks** the characters entered.
c. Text area: Multiple lines of text (messages and comments)

2. Making Choises 
a. Single choise even by **selecting** one of the list or by **drop down** boxes of a list.
b. Checkboxes: Choosing number of choises.

3. Submitting forms:
a. Submit button
b. Image button 
Both submit data from your page to another webpage but in the image button, you can use image.

4. Uploding file:
It allows the user to fill the form through uploading files to the website.

Forms can have many types of form controls and the server needs to know each inputted information corressponds with which element. In order to acheive this, the browser sends the information as name/value pair.

**Note:** You should never change the name of a form control in a page unless 
you know that the code on the server will understand this new value.

### Form structure:
To build a form, `<form>` element is used and have 3 attribues **(not all of them are necessary to included)** :
1. Action: Its value is the URL for the page on the server that will receive the information in the form when it is submitted.
2. Method and have 2 values: get and post. 
When `get` is used, the values from the form are added to the end of the URL specified in 
the action attribute. It's the default method when no method is delared. Also, when `post` is used, the values from the form are added to 
the end of the URL specified in the action attribute.

3. `id` is used to identify the form distinctly.

### `<input>` 
input element is used to define the type of the form control. `type` attribute determines the type of the control form, `name` attribute determines the name of the control form that is send as a pair with the value to the server, and `maxlength` determine the maximum number of charcters the user can enter.

While in radio button, there is a `checked` attribute that must be inserted only in one input. It means which value you want to sent with the name as a pair to the server. **Please keep in mind** that the radio button can't be deselected unless the user choose another radio button. 

### Drop-down list box 

A drop down list box (also known as a select box) allows users to select one option from a 
drop down list. The `<select>` element is used 
to create a drop down list box. It contains two or more <option> elements. `<option>` is used to determine the options the users have. it hase `value`attribute, too. Also, there is `selected` attribute to determine the value of the name to be send as a pair to the server. 

### File input box 
It's used to allow the user to upload file to the input box. Note that the method of the `<form>` element must be set to `post` incase of file input box. 

For the case of image button, an image is uploaded to be the submit button using `src` attribute. There are also height, width and alt attribues. 

# CSS of tables, lists and forms:

**In bullet point style**, ypu can define the shape or style of the bullet, for ordered and unordered lists. You also specify it to be an image.

### Tables Properities:
1. Width 
2. Padding
3. Text-transform
4. Letter spacing and font size
5. Background color 
6. `:hover`: highlightes a table row when user's mouse haver over it.

### Forms styling

It is most common to style:
● Text inputs and text areas
● Submit buttons
● Labels on forms, to get the form controls to align nicely