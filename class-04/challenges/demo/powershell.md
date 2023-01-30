# Arrays

An array can hold several values under one name. Array naming is the same as variables naming.
An array is initialized by assign space-delimited values enclosed in ()

    $my_array=("apple", "banana", "Fruit Basket", "orange")

The total number of elements in the array is referenced by `$ArrayName.Count`

    $my_array=("apple", "banana", "Fruit Basket", "orange")
    echo $my_array.Count                   # 4

The array elements can be accessed with their numeric index. The index of the first element is 0.

    $my_array=("apple", "banana", "Fruit Basket", "orange")
    echo $my_array[3]                       # orange - note that curly brackets are needed
    # adding another array element
    $my_array += "carrot"                    # value assignment without a $ and curly brackets
    echo $my_array.Count                    # 5



## Exercise

In this exercise, you will need to add numbers and strings to the correct arrays. You must add the numbers 1,2, and 3 to the "numbers" array, and the words 'hello' and 'world' to the strings array.

You will also have to correct the values of the variable NumberOfNames and the variable second_name. NumberOfNames should hold the total number of names in the NAMES array, using the $# special variable. Variable second_name should hold the second name in the NAMES array, using the brackets operator [ ]. Note that the index is zero-based, so if you want to access the second item in the list, its index will be 1.

### Tutorial Code

    $NAMES=( "John", "Eric", "Jessica")
    # write your code here
    $NUMBERS=()
    $STRINGS=()
    $NumberOfNames=0
    $second_name='Vladimir'

### Expected Output

    1 2 3
    hello world
    The number of names listed in the NAMES array: 3
    The second name on the NAMES list is: Eric

### Solution

```powershell
$NAMES=( "John", "Eric", "Jessica" )

# write your code here
$NUMBERS=( 1, 2, 3 )
$STRINGS=( "Hello", "World" )
$NumberOfNames=$NAMES.Count
$second_name=$NAMES[1]

Write-Host $NUMBERS
Write-Host $STRINGS
echo "The number of names listed in the NAMES array: $NumberOfNames"
echo "The second name on the NAMES list is: $second_name"
```
*Adapted from learnshell.org*
