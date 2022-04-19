# PHP Cheatsheet

## INTRO

- PHP: Hypertext Preprocessor
- created by Rasmus Lerdorf in 1994
- executed on server and sent to browser as plain HTML


## FUNCTIONALITY

- generate pages/files dynamically
- access files on a server
- collect data from web forms
- send emails
- track web traffic with cookies
- restrict access to website
- encrypt data


## SCRIPT

- use semicolons to end line ;
- Case sensitivity $color $Color $COLOR (all treated as separate variables) BUT keywords, function and classes names are case-insensitive

- Comments
    `// This is a single line comment`
    `# This is also a single line comment`


## VARIABLES

- dont need to be declared before adding a value to them (php automatically assigns correct data type)
    CASE SENSITIVE

        <?php
        
            $var_name = value;
            
        ?>


## CONSTANTS

- value cannot be changed after it is set
- do not need a leading dollar sign ($)
- can be accessed regardless of scope
- values can only be strings and numbers

eg. database username and password, website's base URL, company name, etc.

        <?php
            // Defining constant
            define("USER_EMAIL", "jane@mail.com");
            
            // Using constant
            echo 'User email is - ' . USER_EMAIL;
        ?>


## ECHO & PRINT

    Almost the same! Both can display anything that can be displayed to the browser, such as string, numbers, variables values, the results of expressions etc.

        <?php
            echo "has no return value, can take multiple parameters";

            print "can only take one argument, and always returns 1 print";
        ?>


## DATA TYPES

#### String

        <?php 
            "Hello World";
        ?>

#### Integer 

        <?php
            $integer = 5985;
        ?>

#### Float (floating point numbers - also called double) 

        <?php
          $float = 10.365;
        ?>

#### Boolean 
        <?php
            $var1 = true;   
            $var2 = false;
        ?>
        
#### Array 

        <?php
            $beerTypes = array("lager","IPA","saison");
        ?>
        

#### Object
            <?php
                class Pet {
                    Pulic $species;
                    public $color;
                    public $size;
                    public function __construct($color, $size) {
                        $this->color = $color;
                        $this->model = $size;
                    }
                    public function message() {
                        return "My pet is a " $this->species "and is " . $this->color . " and" . $this->size . "!";
                }
            }

                    $myPet = new Pet("armadillo", "brown", "small");
                        echo $myPet -> message();
                        echo "<br>";

                    $myPet = new Pet("feral cat", "calico", "large");
                            
            ?> 

#### NULL
            <?php
                $message = "Hello world!";
                $message = null;
                var_dump($message);
            ?> 


## OPERATORS

#### groups:
1. Arithmetic operators
2. Assignment operators
3. Comparison operators
4. Increment/Decrement operators
5. Logical operators
6. String operators
7. Array operators
8. Conditional assignment operators


### Examples Arithmetic
        
| Operator   |      Description      |  Example |
|----------|:-------------:|------:|
| + |  Addition | $x + $y |
| - |  Subtraction   |   $x - $y |
| * | Multiplication | $x * $y |
| / | Division | $x / $y |
| % | Modulus | $x % $y |
| * | Multiplication | $x * $y |


### Examples Assignment

| Operator   |      Description      |  Example |
|----------|:-------------:|------:|
| = |  Assign | $x = $y |
| += | Add and assign  | $x += $y |
| -= |  Subtract and assign | $x -= $y |
| *= | Multiply and assign | $x *= $y |
| /= | Divide and assign quotient | $x /= $y |
| %= | Divide and assign modulus | $x %= $y |


### Examples Comparison

| Operator   |      Description      |  Example |
|----------|:-------------:|------:|
| == |  Equal | $x == $y |
| === |  Identical  |  $x === $y |
| != | Not equal | $x != $y |
| <> | Not equal | $x <> $y |
| !== | Not identical | $x !== $y |
| < | Less than | $x < $y |
| > |  Greater than | $x > $y |
| >= | Greater than or equal to | $x >= $y |
| <= | Less than or equal to | $x <= $y |


### Examples Incrementing and Decrementing 

| Operator   |      Description      |  Effect |
|----------|:-------------:|------:|
| ++$x |  Pre-increment | Increments $x by one, then returns $x |
| $x++ |  Post-increment  | Returns $x, then increments $x by one |
| --$x | Pre-decrement | Decrements $x by one, then returns $x |
| $x-- | Post-decrement | Returns $x, then decrements $x by one |


### Examples Logical 

| Operator   |      Description      |  Example |
|----------|:-------------:|------:|
| and |  And | $x and $y|
| or |  Or  | $x or $y |
| xor | Xor | $x xor $y |
| && |  And | $x && $y |
| || | Or | $x || $y|
| ! | Not | !$x |


### Examples String 

| Operator   |      Description      |  Example |
|----------|:-------------:|------:|
| . |  Concatenation | $str1 . $str2|
| .= |  Concatenation assignment  | $str1 .= $str2 |



### Examples Array 

| Operator   |      Description      |  Example |
|----------|:-------------:|------:|
| + |  Union |  $x + $y |
| == |  Equality  |  $x == $y |
| === |  Identity  |  $x === $y |
| != |  Inequality  |  $x != $y |
| <> |  Inequality  | $x <> $y |
| !== | Non-identity  | $x !== $y |


## CONDITIONAL STATEMENTS: IF & ELSE & ELSEIF

      <?php
        $age = 17;
        //$age=(int)readline("enter age: ");
    
            if ($age>19){
                echo "User is 19 or older" . "<br>";
            }
            else{
                echo "User is under 19" . "<br>";
            }
        ?>



## FUNCTIONS

        <?php
            // Defining function

            function registrationMessage(){
                echo "Your registration was successful!";
            }

            // Calling function
            registrationMessage()
        ?>


       <?php

            $miles = 35;

            function convertMilestoKM($miles){
                $output = $miles * 1.609344;

                echo $miles . " miles equals " . $output . " kilometers"; 
            }

                convertMilestoKM($miles);
        
        ?>


## ARRAYS

### Types:
        
        
Indexed array — An array with a numeric key.

            <?php
                $apples = array("gala", "fuji", "McIntosh");
            ?>

Associative array — An array where each key has its own specific value.

            <?php
                $heightInFeet = array("Shrek"=> 8, "donkey"=> 4, "Fiona"=> 5.10, "Lord Farquad"=>4.6);
                
                 var_dump ($heightInFeet);
            ?>

Multidimensional array — An array containing one or more arrays within itself.
            
            <?php
    
              $guests = array(
                  array(
                      "name" => "Shrek",
                      "age" => "400",
                  ),
                  array(
                      "name" => "Fiona",
                      "age" => "30",
                  ),
                  array(
                      "name" => "Lord Farquad",
                      "age" => "569",
                  )
              );
       
               echo "Shrek is " . $guests[0]["age"] . " years old.";
            ?>



## LOOPS

while loops:

        <?php
            $i = 20;                                        //start countdown at 20

            while($i > 0) {                                 //while i is greater than 0
                $i--;                                       //decrement
                echo "The countdown is at " . $i . "<br>";
            }
        ?>

    
for loops:

       <?php
            //Write a program to count backwards from 20 that stops at 0
            
            function backFromTwenty(){
            
                for($i=20; $i>=0; $i--){
                    echo $i . " ";
                    }
                }
                backFromTwenty()
        ?>