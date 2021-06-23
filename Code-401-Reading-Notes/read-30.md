# Hashtables
What is a Hashtable?

- Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.
  
- Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.
- Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.
  
**Why do we use them?**
- Hold unique values
- Dictionary
- Library
  
- Hashtables are a data structure that utilize key value pairs. This means every Node or Bucket has both a key, and a value.
  
 - The basic idea of a hashtable is the **ability to store the key into this data structure, and quickly retrieve the value.** This is done through what we call a hash
  
- `hash` is the ability to encode the key that will eventually map to a specific location in the data structure that we can
  
- `search through the data to look up` a neighborhood and obtain it’s zip code. We could do this using a for loop that looks through each piece of data one by one until it finds the neighborhood name, then returns the zip code there. This would be an` O(N) read operation because it requires searching through each piece of data to find the one piece we want`.

- `Hash maps take advantage of an array’s O(1) read access.` Instead of adding elements to an array from beginning to end, a hash map uses a “hash function” to place each item at a precise index location, based off it’s key.

### Structure
- `Hashing`
Basically, a hash code turns a key into an integer. 

- `Creating a Hash`
A hashtable traditionally is created from an array
  - Add or multiply all the ASCII values together.
  - Multiply it by a prime number such as 599.
  - Use modulo to get the remainder of the result, when divided by the total size of the array.
  - Insert into the array at that index.
  
  **ASCII:**, abbreviated from American Standard Code for Information Interchange, is a character encoding standard for electronic communication. ASCII codes represent text in computers, telecommunications equipment, and other devices.

  ![](https://www.unitronicsplc.com/Download/SoftwareHelp/VisiLogic_Knowledgebase/ASCII_Table.gif)

```js
  Key = "Cat"
Value = "Josie"

67 + 97 + 116 = 280

280 * 599 = 69648

69648 % 1024 = 16

Key gets placed in index of 16. 
  ```
**We now know that our key Cat maps to index 16 of the array. We can view into this index and find “Josie”, our value quickly.**


  **Collisions**
**A collision occurs when more than one key hashes to the same index in an array.** As mentioned earlier, a “perfect hash” will never have any collisions. To put this into perspective, the worst possible hash is one that hashes every single key to the same exact index of an array. The more keys you have hashed to a specific index, the more key/value pair combos you can potentially have.

What would happen if **two different keys resolved to be the same index of the array? This is called a collision.** The hash map needs to be able to handle two keys resolving to the same index.

Collisions are solved by changing the initial state of the buckets. Instead of starting them all as null we can initialize a LinkedList in each one! Now if two keys resolve to the same index in the array then their key/value pairs can be stored as a node in a linked list. Each index in the array is called a “bucket” because it can store multiple key/value pairs.

**Bucket Sizes**
**Hash Maps can have any number of buckets.** If a hash map has only a few buckets it will be densely full and have many collisions. If a hash map has more buckets it will be more sparsely populated, there will be less collisions, but there may be a lot of extra empty space.

It’s possible to compute the `“load factor”` of a hash table. The load factor **tells us something about how full the hash table is**. A hash table can start with only a few buckets, calculate it’s own load factor, recognize when it gets too full and automatically grow and add more buckets to itself to accommodate more data.


**Hash maps do this to store values:**

- accept a key
- calculate the hash of the key
- use modulus to convert the hash into an array index
- store the key with the value by appending both to the end of a linked list
  
**Hash maps do this to read value:**

- accept a key
- calculate the hash of the key
- use modulus to convert the hash into an array index
- use the array index to access the short LinkedList representing a bucket
- search through the bucket looking for a node with a key/value pair that matches the key you were given
  
  ### Internal Methods
  - Add()
  - Find()
  - Contains()
  - GetHash()

## Basics of Hash Tables
Hashing is implemented in two steps:

- An element is converted into an integer by using a hash function. This element can be used as an index to store the original element, which falls into the hash table.
  
- The element is stored in the hash table where it can be quickly retrieved using hashed key.

     `hash = hashfunc(key)
   index = hash % array_size`

   ***Hash table***
   is a data structure that is used to store keys/value pairs. It uses a hash function to compute an index into an array in which an element will be inserted or searched. By using a good hash function, hashing can work well. Under reasonable assumptions, the average time required to search for an element in a hash table is O(1).

   - **The idea of hashing is to distribute the entries (key/value pairs) across an array of buckets. Given a key, the algorithm computes an index that suggests where the entry can be found:**

`index = f(key, array_size)`

Often this is done in two steps:

`hash = hashfunc(key)`
`index = hash % array_size`

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/fd499f2d72d4d62340d6c35ffa1e27649885c381)

where

- n is the number of entries occupied in the hash table.
- k is the number of buckets.