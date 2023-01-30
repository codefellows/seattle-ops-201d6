# Basic String Operations
Powershell allows some common string operations which can be very useful for script writing.

## String Length

    #     1234567890123456
    $STRING="this is a string"
    echo $STRING.Length          # 16

## Index

Find the numerical position in `$STRING` of any `$SUBSTRING` that matches. Note that if the specified string does not match, it returns the value `-1`

    $STRING="this is a string"
    $SUBSTRING="is"
    $STRING.IndexOf($SUBSTRING)
    2 # 2 is the position of the first $SUBSTRING character in $STRING

## Substring Extraction

The `Substring()` method allows us to extract a part of a string in PowerShell. This method allows us to specify the start and length of the substring that we want to extract from a string. Note that the starting position is `0`.

    # Basic Syntax
    Substring(startIndex, length)

    $STRING="this is a string"
    $STRING.Substring(0, 4)
    this # Extracts the character starting from index 0


If: `length` is omitted, extract substring from `startIndex` to end of line

    $STRING="this is a string"
    $STRING.Substring(1)       # $STRING contents without leading character 't'
    $STRING.Substring(12)      # ring

## Simple data extraction example

    # Code to extract the First name from the data record
    $DATARECORD="last=Clifford,first=Johnny Boy,state=CA"
    $COMMA1=$DATARECORD.IndexOf(",")  # 14 position of first comma
    $CHOP1FIELD=$DATARECORD.Substring($($COMMA1))       #
    $COMMA2=$CHOP1FIELD.LastIndexOf(",")
    $LENGTH=$COMMA2 - 7
    $FIRSTNAME=$CHOP1FIELD.Substring(7, $LENGTH)
    $FIRSTNAME=${CHOP1FIELD:6:$LENGTH}      # Johnny Boy
    echo $FIRSTNAME

## Substring Replacement

    $STRING="to be or not to be"

### Replace first occurrence of substring with replacement

    $STRING="to be or not to be"
    [regex]$pattern = "be"
    $STRING = $pattern.replace($STRING, "eat", 1)
    echo $STRING  # to eat or not to be

### Replace all occurrences of substring

    $STRING="to be or not to be"
    $STRING.Replace('be', 'eat')        # to eat or not to eat

### Delete all occurrences of substring (replace with empty string)

    $STRING="to be or not to be"
    $STRING.Replace('not','')        # to be or to be

## Exercise

In this exercise, you will need to change Warren Buffett's known saying. First create a variable `$ISAY` and assign it the original saying value. Then re-assign it with a new changed value using the string operations and following the 4 defined changes:

Change1: replace the first occurrence of 'snow' with 'foot'.

Change2: delete the second occurrence of 'snow'.

Change3: replace 'finding' with 'getting'.

Change4: delete all characters following 'wet'. Tip: One way to implement Change4, if to find the index of 'w' in the word 'wet' and then use substring extraction.

### Tutorial Code

    $BUFFETT="Life is like a snowball. The important thing is finding wet snow and a really long hill."

    # write your code here

    $ISAY=
    $ISAY=

    # Test code - do not modify

    echo "Warren Buffett said:"
    echo $BUFFETT
    echo "and I say:"
    echo $ISAY

### Expected Output

    Warren Buffett said:
    Life is like a snowball. The important thing is finding wet snow and a really long hill.
    and I say:
    Life is like a football. The important thing is getting wet

### Solution

```powershell

$BUFFETT="Life is like a snowball. The important thing is finding wet snow and a really long hill."

    # write your code here
    $ISAY=$BUFFETT
    [regex]$pattern = "snow"
    $CHANGE1 = $pattern.Replace($ISAY, "foot", 1)
    $CHANGE2 = $pattern.Replace($CHANGE1, "", 1)
    $CHANGE3 = $CHANGE2.Replace( "finding", "getting" )
    $INDEX = $CHANGE3.LastIndexOf("w")
    $CHANGE4 = $CHANGE3.Substring(0, $INDEX+3)
    $ISAY=$CHANGE4

# Test code - do not modify

echo "Warren Buffett said:"
echo $BUFFETT
echo "and I say:"
echo "$ISAY"
```
*Adapted from learnshell.org*
