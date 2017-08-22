Arrays are collections of values. Every array has the following properties (it also has those every value has):
### Index properties
Elements in an array can be accessed by their index (zero-based). You can use the `get(index)` property, or the `1` property for index 1
(works for every other index too).
```
//result is "c"
["b", "c"].1;
//result is 7
var a = [1,5,7].get(2);
```

### length
Returns: how many elements are stored in this array.
### getOrDefault
Same as get, but when the index does not exist it returns a specified default value. Parameter 1: the index. Parameter 2: what is returned
if the index was not found (e.g. index -1). Returns: the value at the given index, or the default value.
### set
Sets an index to a new value. Parameter 1: the index to set. Parameter 2: the new value. Returns: what was at this index before.
### cut
Returns a sub-array of the original. Parameter 1: The index to skip to. `[1,2,3].cut(1)` is `[2,3]`.
### remove
Currently not working because of a bug. Removes the element at the given index and returns it. Parameter 1: the index to remove.
### add
Returns the sum of the array elements.
### mul
Returns the product of the array elements.
### repeat
Returns an infinite array that contains the original elements and repeats them. `[1,2,3].repeat()` is `[1,2,3,1,2,3,1,2,3,1,2,3` and so on.
### sort
Sorts this array. Reurns: this array.
### zip
Makes one array of a two-dimensional one using an operator function. Parameter 1: the operator. `[[1,2,3],[4,5,6]].zip(+)` is `[5,7,9]`.
### link
Concatenates two arrays. Parameter 2: the second array. `[1,2,3].link([4,5,6])` is `[1,2,3,4,5,6]`.
