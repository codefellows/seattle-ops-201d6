# Decision Making

As in popular programming languages, the shell also supports logical decision making.

The basic conditional decision making construct is:

```powershell
  if ( $condition )
  {
    # do something
  }
```

    $NAME="John"
    if ( $NAME -eq "John ")
    {
      echo "True - my name is indeed John"
    }

It can be expanded with 'else'

    $NAME="Bill"
    if ( "$NAME" -eq "John" )
    {
      echo "True - my name is indeed John"
    }
    else
    {
      echo "False"
      echo "You must mistaken me for $NAME"
    }

It can be expanded with 'elseif' (else-if)

    $NAME="George"
    if ( "$NAME" = "John" )
    {
      echo "John Lennon"
    }
    elseif ( "$NAME" = "George" )
    {
      echo "George Harrison"
    }
    else
    {
      echo "This leaves us with Paul and Ringo"
    }

The expression used by the conditional construct is evaluated to either true or false.
The expression can be a single string or variable. A empty string or a string consisting of spaces or an undefined variable name, are evaluated as false.

The expression can be a logical combination of comparisons: negation is denoted by `!` or `-not`, logical AND (conjunction) is denoted by `-and`, and logical OR (disjunction) is denoted by `-or`. Conditional expressions should be surrounded by parentheses `()`.

## Types of numeric comparisons

    comparison    Evaluated to true when
    $a -lt $b     $a < $b
    $a -gt $b     $a > $b
    $a -le $b     $a <= $b
    $a -ge $b     $a >= $b
    $a -eq $b     $a is equal to $b
    $a -ne $b     $a is not equal to $b

## Types of string comparisons

    comparison                                Evaluated to true when
    "$a" -eq "$b"                             $a is the same as $b
    "$a" -ne "$b"                             $a is different from $b
    [string]::IsNullOrWhiteSpace($a)          $a is empty

- note1: whitespace around `-eq` is required
- note2: use `""` around string variables to avoid shell expansion of special characters as `*`

### Logical combinations

    if ( $VAR_A -eq 1 -and ($VAR_B -eq "bee" -or $VAR_T -eq "tee") )
    {
        command...
    }

### Switch structure

    Switch (<test-expression>)
    {
      <result1-to-be-matched> {<action>}
      <result2-to-be-matched> {<action>}
    }

### Simple switch PowerShell structure

    $mycase = 1
    switch ($mycase)
    {
       1 {"You selected 1."}
       2 {"You selected 2."}
       3 {"You selected 3."}
       default {"No Match found"}
    }

## Exercise

Change the variables in the first section, so that each if statement resolves as True.

### Tutorial Code

    # change these variables
    $NUMBER=10
    $APPLES=12
    $KING=GEORGE

    # modify above variables
    # to make all decisions below TRUE
    if ( $NUMBER -gt 15 )
    {
      echo 1
    }
    if ( $NUMBER -eq $APPLES )
    {
      echo 2
    }
    if  ( ($APPLES -eq 12) -or ($KING = "LUIS"))
    {
      echo 3
    }
    if ( $($NUMBER + $APPLES) -le 32 )
    {
      echo 4
    }

### Expected Output

    1
    2
    3
    4

### Solution

```powershell
# change these variables
$NUMBER=16
$APPLES=16
$KING="LUIS"
# modify above variables
# to make all decisions below TRUE
if ( $NUMBER -gt 15 )
{
  echo 1
}
if ( $NUMBER -eq $APPLES )
{
  echo 2
}
if  ( ($APPLES -eq 12) -or ($KING = "LUIS"))
{
  echo 3
}
if ( $($NUMBER + $APPLES) -le 32 )
{
  echo 4
}
```
*Adapted from learnshell.org*
