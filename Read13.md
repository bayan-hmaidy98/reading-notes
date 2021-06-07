# HTML5 storage
HTML5 storage or web storage is `it’s a way for web pages to store named key/value pairs locally, within the client web browser.` It is similar to cookies in maintaining the data even after the client exit the browser! And it's unlike cookies in transmitting the data to the remote web page unless it's done manually. 

### Checking if the browser support HTML5 or not by:
1.
 > function supports_html5_storage() { 
 
 > try {
 
  >  return 'localStorage' in window && window['localStorage'] !== null;
 
  > } catch (e) {
 
   > return false;
 
 > }
 
 > }
2. Modernizer 

**Local Storage** can be treated as a JS object, and we can use objects in:
1. Overwrite the previous data.
2. Remove a value for a given key.
3. Clean the entire storage area.
4. Get the total number of values in the storage area.

### Storage event 
In order to to keep the track of the changes in the storage area, you can trap the storage event. It's fired for all the changes like: `setItem(), removeItem(), or clear()`. **Note** that storage event is not cancelable. 

In HTML5 Storage, the progress can be saved locally, even if the browser window was closed.
