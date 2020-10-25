# Hash Tables

**Data structure that is used to store information and is a way to implement an associative array**

- Purposes
  - Hold unique values
  - Dictionary
  - Library

- Utilizes **key value pairs**

- An array is a specilization of a hash table (in that it has key value pairs as well, index and value at that index)

- Write a hash function
  - Looks at certain key, evaluates the key, and spits out an index number that corresponds to location of that value
  - If chaining is involved, you can get straight to index of original array, but then you have to look through chained items

- Takes a key and returns an integer:
  `Hash (key) -> index`
  `Hash (Tia) -> 3`

- Methods to avoid "collision"
  - Chaining
    - Can create a linked list, or array within array


## Vocabulary

|    **Term**    | **Definition**  |
| -------------- | ----------- |
| Hash | result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. in the case of hashtable, it is used to determine the index of an array |
| Buckets | what is contained in each index of the array of the hashtable. each index is a bucket. an index could potentially contain multiple key/value pairs if a collision occurs |
| Collisions | a collision is what happens when more than one key gets hashed to the same location of the hashtable |
