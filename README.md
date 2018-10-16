# Python Dictionary
Dictionary in Python is an unordered collection of data values, used to store data values like a map, which unlike other Data Types that hold only single value as an element, Dictionary holds key:value pair. Key value is provided in the dictionary to make it more optimized. Each key-value pair in a Dictionary is separated by a colon :, whereas each key is separated by a ‘comma’.

A Dictionary in Python works similar to the Dictionary in a real world. Keys of a Dictionary must be unique and of immutable data type such as Strings, Integers and tuples, but the key-values can be repeated and be of any type.

* Note – Keys in a dictionary doesn’t allows Polymorphism.

## Creating a Dictionary
In Python, a Dictionary can be created by placing sequence of elements within curly {} braces, separated by ‘comma’. Dictionary holds a pair of values, one being the Key and the other corresponding pair element being its Key:value. Values in a dictionary can be of any datatype and can be duplicated, whereas keys can’t be repeated and must be immutable.

Dictionary can also be created by the built-in function dict(). An empty dictionary can be created by just placing to curly braces{}.

* Note – Dictionary keys are case sensitive, same name but different cases of Key will be treated distinctly.

![dictionary-creation-1](https://user-images.githubusercontent.com/31289155/47039858-7d2fec80-d1a2-11e8-9a01-3d84b7248048.jpg)

 
## Example:
<pre>
# Creating an empty Dictionary 
Dict = {} 
print("Empty Dictionary: ") 
print(Dict) 
  
# Creating a Dictionary  
# with Integer Keys 
Dict = {1: 'Geeks', 2: 'For', 3: 'Geeks'} 
print("\nDictionary with the use of Integer Keys: ") 
print(Dict) 
  
# Creating a Dictionary  
# with Mixed keys 
Dict = {'Name': 'Geeks', 1: [1, 2, 3, 4]} 
print("\nDictionary with the use of Mixed Keys: ") 
print(Dict) 
  
# Creating a Dictionary 
# with dict() method 
Dict = dict({1: 'Geeks', 2: 'For', 3:'Geeks'}) 
print("\nDictionary with the use of dict(): ") 
print(Dict) 
  
# Creating a Dictionary 
# with each item as a Pair 
Dict = dict([(1, 'Geeks'), (2, 'For')]) 
print("\nDictionary with each item as a pair: ") 
print(Dict) 

# Creating a Nested Dictionary 
Dict = {1: {'A' : 'Geeks', 'B' : 'For', 'C' : 'Geeks'}, 
        2: {'D' : 'Welcome', 'E' : 'To', 'F' : 'Geeks'}} 
print("\nNested Dictionary: ") 
print(Dict) </pre>

## Output:
<pre>
Empty Dictionary: 
{}

Dictionary with the use of Integer Keys: 
{1: 'Geeks', 2: 'For', 3: 'Geeks'}

Dictionary with the use of Mixed Keys: 
{1: [1, 2, 3, 4], 'Name': 'Geeks'}

Dictionary with the use of dict(): 
{1: 'Geeks', 2: 'For', 3: 'Geeks'}

Dictionary with each item as a pair: 
{1: 'Geeks', 2: 'For'}

Nested Dictionary: 
{1: {'B': 'For', 'C': 'Geeks', 'A': 'Geeks'}, 2: {'F': 'Geeks', 'E': 'To', 'D': 'Welcome'}}
</pre>

## Adding elements to a Dictionary
In Python Dictionary, Addition of elements can be done in multiple ways. One value at a time can be added to a Dictionary by defining value along with the key e.g. Dict[Key] = ‘Value’. Updating an existing value in a Dictionary can be done by using the built-in update() method. Nested key values can also be added to an existing Dictionary.
* Note- While adding a value, if the key value already exists, the value gets updated otherwise a new Key with the value is added to the Dictionary.

## Example
<pre>
# Creating an empty Dictionary 
Dict = {} 
print("Empty Dictionary: ") 
print(Dict) 
  
# Adding elements one at a time 
Dict[0] = 'Geeks'
Dict[2] = 'For'
Dict[3] = 1
print("\nDictionary after adding 3 elements: ") 
print(Dict) 
  
# Adding set of values  
# to a single Key 
Dict['Value_set'] = 2, 3, 4
print("\nDictionary after adding 3 elements: ") 
print(Dict) 
  
# Updating existing Key's Value 
Dict[2] = 'Welcome'
print("\nUpdated key value: ") 
print(Dict) 
  
# Adding Nested Key value to Dictionary 
Dict[5] = {'Nested' :{'1' : 'Life', '2' : 'Geeks'}} 
print("\nAdding a Nested Key: ") 
print(Dict) 
</pre>


## Output:
<pre>
Empty Dictionary: 
{}

Dictionary after adding 3 elements: 
{0: 'Geeks', 2: 'For', 3: 1}

Dictionary after adding 3 elements: 
{0: 'Geeks', 2: 'For', 3: 1, 'Value_set': (2, 3, 4)}

Updated key value: 
{0: 'Geeks', 2: 'Welcome', 3: 1, 'Value_set': (2, 3, 4)}

Adding a Nested Key: 
{0: 'Geeks', 2: 'Welcome', 3: 1, 5: {'Nested': {'1': 'Life', '2': 'Geeks'}}, 'Value_set': (2, 3, 4)}
</pre>

## Removing Elements from Dictionary
In Python Dictionary, deletion of keys can be done by using the del keyword. Using del keyword, specific values from a dictionary as well as whole dictionary can be deleted. Other functions like pop() and popitem() can also be used for deleting specific values and arbitrary values from a Dictionary. All the items from a dictionary can be deleted at once by using clear() method. Items in a Nested dictionary can also be deleted by using del keyword and providing specific nested key and particular key to be deleted from that nested Dictionary.
* Note- del Dict will delete the entire dictionary and hence printing it after deletion will raise an Error.

## Example:
<pre>
# Initial Dictionary 
Dict = { 5 : 'Welcome', 6 : 'To', 7 : 'Geeks', 
        'A' : {1 : 'Geeks', 2 : 'For', 3 : 'Geeks'}, 
        'B' : {1 : 'Geeks', 2 : 'Life'}} 
print("Initial Dictionary: ") 
print(Dict) 
  
# Deleting a Key value 
del Dict[6] 
print("\nDeleting a specific key: ") 
print(Dict) 
  
# Deleting a Key from 
# Nested Dictionary 
del Dict['A'][2] 
print("\nDeleting a key from Nested Dictionary: ") 
print(Dict) 
  
# Deleting a Key  
# using pop() 
Dict.pop(5) 
print("\nPopping specific element: ") 
print(Dict) 
  
# Deleting a Key 
# using popitem() 
Dict.popitem() 
print("\nPops first element: ") 
print(Dict) 
  
# Deleting entire Dictionary 
Dict.clear() 
print("\nDeleting Entire Dictionary: ") 
print(Dict) 
</pre>

## Output:
<pre>
Initial Dictionary: 
{'A': {1: 'Geeks', 2: 'For', 3: 'Geeks'}, 'B': {1: 'Geeks', 2: 'Life'}, 5: 'Welcome', 6: 'To', 7: 'Geeks'}

Deleting a specific key: 
{'A': {1: 'Geeks', 2: 'For', 3: 'Geeks'}, 'B': {1: 'Geeks', 2: 'Life'}, 5: 'Welcome', 7: 'Geeks'}

Deleting a key from Nested Dictionary: 
{'A': {1: 'Geeks', 3: 'Geeks'}, 'B': {1: 'Geeks', 2: 'Life'}, 5: 'Welcome', 7: 'Geeks'}

Popping specific element: 
{'A': {1: 'Geeks', 3: 'Geeks'}, 'B': {1: 'Geeks', 2: 'Life'}, 7: 'Geeks'}

Pops first element: 
{'B': {1: 'Geeks', 2: 'Life'}, 7: 'Geeks'}

Deleting Entire Dictionary: 
{}
</pre>


# Dictionary Methods

<pre>
* METHODS               	  DESCRIPTION

copy()	                    They copy() method returns a shallow copy of the dictionary.
clear()	                    The clear() method removes all items from the dictionary.
get()	                      It is a conventional method to access a value for a key.
dictionary_name.values()	  returns a list of all the values available in a given dictionary.
str()	                      Produces a printable string representation of a dictionary.
update()	                  Adds dictionary dict2’s key-values pairs to dict
setdefault()	              Set dict[key]=default if key is not already in dict
keys()	                    Returns list of dictionary dict’s keys
items()	                    Returns a list of dict’s (key, value) tuple pairs
has_key()	                  Returns true if key in dictionary dict, false otherwise
fromkeys()	                Create a new dictionary with keys from seq and values set to value.
type()	                    Returns the type of the passed variable.
cmp()	                      Compares elements of both dict.</pre>





# Program to print all distinct elements of a given integer array in Python | Ordered Dictionary

Given an integer array, print all distinct elements in array. The given array may contain duplicates and the output should print every element only once. The given array is not sorted.

## Examples:
<pre>
Input: arr[] = {12, 10, 9, 45, 2, 10, 10, 45}
Output: 12, 10, 9, 45, 2

Input: arr[] = {1, 2, 3, 4, 5}
Output: 1, 2, 3, 4, 5

Input: arr[] = {1, 1, 1, 1, 1}
Output: 1
</pre>

This problem has existing solution please refer Print All Distinct Elements of a given integer array link. We will solve this problem in python quickly using Ordered Dictionary. Approach is simple,

* Convert array into dictionary data structure using OrderedDict.fromkeys(iterable) function, it converts any iterable into dictionary     having elements as Key in the same order they appeared in array.
* Now iterate through complete dictionary and print keys.

## Example
 <pre>  
from collections import OrderedDict 
 
def printDistinct(input): 
     # convert list into ordered dictionary 
     ordDict = OrderedDict.fromkeys(input) 
  
     # iterate through dictionary and get list of keys 
     # list of keys will be resultant distinct elements  
     # in array 
     result = [ key for (key, value) in ordDict.items() ] 
  
     # concatenate list of elements with ', ' and print 
     print (', '.join(map(str, result))) 
     
    
  
# Driver program 
if __name__ == "__main__": 
    input = [12, 10, 9, 45, 2, 10, 10, 45] 
    printDistinct(input) 

 </pre>
 ## Output:

                                                 12, 10, 9, 45, 2
