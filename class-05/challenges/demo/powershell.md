# Loops

## PowerShell `for` loop

    # basic construct
    for (<Init>; <Condition>; <Repeat>)
    {
      command(s)...
    }

For each pass through the loop, the init variable takes on the value of each successive value in the list. Then the command(s) are executed.

    # loop on array member
    $NAMES=("Joe", "Jenny", "Sara", "Tony")

    for ($i = 0; $i -le $NAMES.length; i++)
    {
      echo $NAMES[$i]
    }

## PowerShell `Foreach` loop

The `Foreach` loops through a set of input objects and performs an operation with each input.

    # Basic construct
    foreach (<item> in <collection>)
    {
      command(s)...
    }

    # Example
    $NAMES = "("Joe", "Jenny", "Sara", "Tony")
    foreach ($N in $NAMES)
    {
      echo $N
    }

## PowerShell `while` loop

    # basic construct
    while ( condition )
    {
       command(s)...
    }

The while construct tests for a condition, and if true, executes commands. It keeps looping as long as the condition is true.

    $COUNT=4
    while ( $COUNT -gt 0 )
    {
      echo "Value of count is: $COUNT"
      $COUNT=$(($COUNT - 1))
    }

## PowerShell `Do Until` loop

    # basic construct
    do
    {
      <statement list>
    } until (<condition>)

The until construct tests for a condition, and if false, executes commands. It keeps looping as long as the condition is false (opposite of while construct)

    $COUNT=1
    do
    {
      echo "Value of count is: $COUNT"
      $COUNT=$(($COUNT + 1))
    } until ($COUNT -gt 5)

## `break` and `continue` statements

break and continue can be used to control the loop execution of for, while and until constructs. continue is used to skip the rest of a particular loop iteration, whereas break is used to skip the entire rest of loop. A few examples:

    # Prints out 0,1,2,3,4

    $COUNT=0
    while ( $COUNT -ge 0 )
    {
      echo "Value of COUNT is: $COUNT"
      $COUNT=$(($COUNT+1))
      if ( $COUNT -ge 5 )
      {
        break
      }
    }

    # Prints out only odd numbers - 1,3,5,7,9
    $COUNT=0
    while ( $COUNT -lt 10 )
    {
      $COUNT=$(($COUNT+1))
      # Check if COUNT is even
      if ($(($COUNT % 2)) -eq 0 )
      {
        continue
      }
      echo $COUNT
    }

## Exercise

In this exercise, you will need to loop through and print out all even numbers from the numbers list in the same order they are received. Don't print any numbers that come after 237 in the sequence.

### Tutorial Code

    NUMBERS=(951, 402, 984, 651, 360, 69, 408, 319, 601, 485, 980, 507, 725, 547, 544, 615, 83, 165, 141, 501, 263, 617, 865, 575, 219, 390, 237, 412, 566, 826, 248, 866, 950, 626, 949, 687, 217, 815, 67, 104, 58, 512, 24, 892, 894, 767, 553, 81, 379, 843, 831, 445, 742, 717, 958, 609, 842, 451, 688, 753, 854, 685, 93, 857, 440, 380, 126, 721, 328, 753, 470, 743, 527)

    # write your code here


### Expected Output

    402
    984
    360
    408
    980
    544
    390

### Solution

```powershell
NUMBERS=(951, 402, 984, 651, 360, 69, 408, 319, 601, 485, 980, 507, 725, 547, 544, 615, 83, 165, 141, 501, 263, 617, 865, 575, 219, 390, 237, 412, 566, 826, 248, 866, 950, 626, 949, 687, 217, 815, 67, 104, 58, 512, 24, 892, 894, 767, 553, 81, 379, 843, 831, 445, 742, 717, 958, 609, 842, 451, 688, 753, 854, 685, 93, 857, 440, 380, 126, 721, 328, 753, 470, 743, 527)

# write your code here
foreach ($N in $NUMBERS)
{
  if ( $N -eq 237)
  {
    break;
  }
  elseif ( $(($N % 2)) -eq 0)
  {
    echo $N
  }
}
```
*Adapted from learnshell.org*
