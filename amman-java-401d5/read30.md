# Hashtables: 

Before we start talking about hashtables, we need to define some terms.

Hash: hashing is the process of converting a string to value, in our case the value is an index.
Buckets: each index can be looked at as a container to the buckets. These indecies live in the hashtable. 
Collisions: collision ocurrs when there's more than one key in the same index. We'll discus further why would collisions may occur in hashtables. 

Now, What are the hashtables?

Hashtables are **data steucture** store data as key/value pair. Hashtable can have many indecies, each index has many buckets that store key/value pair one at each. As "I have mentioned earlier, hashing occurs to convert a sting to value, this value is called an index. We use the index to retrieve the key/value from hashtable. Hashtables use the index concept, like arrays. This would make the time comlexity equals O(1) becuase we are looking to a specified index in the hashedtable. 

So, after hashing the key, we have an index that is the same as the location where key/value pair will allocate. Hashcode is **obtained** and **read** in constant time. 

## Creating a Hash 

When hashing a key, a specific integer is obtained. This integer **must** be the same in each time we hash the key. In order to hash a key, these steps are implemented:

1. **Add** or **multiply** the ASCII values.
2. Multiply it by prime number.
3. Get the reminder of the result when divided to array size (total).
4. Now you have the index, insert the key/value pair in it. 

**Note:** in order to store values at the same index in buckets, linked list are used to store key/value pain in nodes. Each time you add to the same index, node is added to the end of the linked list. 

Let's move to storing and reading value part! 

In order to *store* in a hash map, you need to accept the key, hash it, convert to index, and store the key/value pait in the obtained index. 

To read a value from a hashtable, accept the key, hash it, convert it to index, search for the index till you reach the short linked list, get the node that contains the provided key. 

### Bucket size 

When you are determining the size of the bucket, bare in mind that you don't want to have many collisions neither an empty space. To do this, oad factor is calculated fr the hashtable and hashtable will be aware when it's full and need tp add more buckets to it. 

### Internal methods

`GetHash()` is used in `Add()`, `Find()`, and `Contains()` methods. It's responsible for converting the string and return an index.

`Add()` is used to add to the hashtable after checking if there's data stored in the index.

`Find()` is used to find a key in hashtable and retun it's value. 

`Contains()` return a boolean if the key exists in the hashtable. 

### Hash functions

Hash functions are used to map a data set of **arbitary size** to a data set of fixed size. There are multiple hash functions, but we nedd a hash function that is easy to use and compute, doesn't result in clustering, and has less collisions. 

### Linear probing

Instead of adding data to linked lists, data are store in the array itself after extended. When an new value is added. it is ashed and the returned index is looked up to find whether it's occupied or not. `When searching for an entry, the array is scanned in the same sequence until either the target element is found or an unused slot is found.` Open addressing refered to  the fact that this method is not **strict** to the hash value. 

There are also Quadratic probing and Double probing.