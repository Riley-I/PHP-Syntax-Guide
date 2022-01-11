INTRO

    PHP: Hypertext Preprocessor
    created by Rasmus Lerdorf in 1994
    executed on server and sent to browser as plain HTML


FUNCTIONALITY

    generate pages/files dynamically
    access files on a server
    collect data from web forms
    send emails
    track web traffic with cookies
    restrict access to website
    encrypt data


SCRIPT

    use semicolons to end line ;
    Case sensitivity $color $Color $COLOR (all treated as separate variables) BUT keywords, function and classes names are case-insensitive

Comments
    // This is a single line comment
    # This is also a single line comment


VARIABLES

    dont need to be declared before adding a value to them (php automatically assigns correct data type)
    CASE SENSITIVE

        <?php
            $var_name = value;
        ?>


CONSTANTS

    value cannot be changed after it is set
    do not need a leading dollar sign ($)
    can be accessed regardless of scope
    values can only be strings and numbers
    eg. database username and password, website's base URL, company name, etc.

        <?php
            // Defining constant
            define("USER_EMAIL", "jane@mail.com");
            
            // Using constant
            echo 'User email is - ' . USER_EMAIL;
        ?>


ECHO & PRINT

    Almost the same! Both can display anything that can be displayed to the browser, such as string, numbers, variables values, the results of expressions etc.

        <?php
            echo "has no return value, can take multiple parameters";

            print "can only take one argument, and always returns 1 print";
        ?>


DATA TYPES

    String

        <?php 
            "Hello World";
        ?>

    Integer 

        <?php
            $integer = 5985;
        ?>

    Float (floating point numbers - also called double) 

        <?php
          $float = 10.365;
        ?>

    Boolean 
        <?php
            $var1 = true;   
            $var2 = false;
        ?>
        
    Array 

        <?php
            $beerTypes = array("lager","IPA","saison");
        ?>
        

    Object
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

    NULL
            <?php
                $message = "Hello world!";
                $message = null;
                var_dump($message);
            ?> 


OPERATORS

groups:
    Arithmetic operators
    Assignment operators
    Comparison operators
    Increment/Decrement operators
    Logical operators
    String operators
    Array operators
    Conditional assignment operators

        1. Arithmetic

                + 	Addition 	    $x + $y 	Sum of $x and $y 	
                - 	Subtraction 	$x - $y 	Difference of $x and $y 	
                * 	Multiplication 	$x * $y 	Product of $x and $y 	
                / 	Division 	    $x / $y 	Quotient of $x and $y 	
                % 	Modulus 	    $x % $y 	Remainder of $x divided by $y 	
                ** 	Exponentiation 	$x ** $y 	Result of raising $x to the $y'th power


        2. Assignment

                x = y 	x = y 	The left operand gets set to the value of the expression on the right 	
                x += y 	x = x + y 	Addition 	
                x -= y 	x = x - y 	Subtraction 	
                x *= y 	x = x * y 	Multiplication 	
                x /= y 	x = x / y 	Division 	
                x %= y 	x = x % y 	Modulus


        3. Comparison

                == 	    Equal 	$                   x == $y 	Returns true if $x is equal to $y 	
                === 	Identical 	                $x === $y 	Returns true if $x is equal to $y, and they are of the same type 	
                != 	    Not equal 	                $x != $y 	Returns true if $x is not equal to $y 	
                <> 	    Not equal 	                $x <> $y 	Returns true if $x is not equal to $y 	
                !== 	Not identical 	            $x !== $y 	Returns true if $x is not equal to $y, or they are not of the same type 	
                > 	    Greater than 	            $x > $y 	Returns true if $x is greater than $y 	
                < 	    Less than 	                $x < $y 	Returns true if $x is less than $y 	
                >= 	    Greater than or equal to 	$x >= $y 	Returns true if $x is greater than or equal to $y 	
                <= 	    Less than or equal to 	    $x <= $y 	Returns true if $x is less than or equal to $y 	
                <=> 	Spaceship 	                $x <=> $y 	Returns an integer less than, equal to, or greater than zero, depending on if $x is less than, equal to, or greater than $y. Introduced in PHP 7.


        4. Increment/Decrement

                ++$x 	Pre-increment 	Increments $x by one, then returns $x 	
                $x++ 	Post-increment 	Returns $x, then increments $x by one 	
                --$x 	Pre-decrement 	Decrements $x by one, then returns $x 	
                $x-- 	Post-decrement 	Returns $x, then decrements $x by one


        5. Logical

                and 	And 	$x and $y 	True if both $x and $y are true 	
                or 	    Or 	    $x or $y 	True if either $x or $y is true 	
                xor 	Xor 	$x xor $y 	True if either $x or $y is true, but not both 	
                && 	    And 	$x && $y 	True if both $x and $y are true 	
                || 	    Or 	    $x || $y 	True if either $x or $y is true 	
                ! 	    Not 	!$x 	    True if $x is not true


        6. String

                . 	Concatenation 	            $txt1 . $txt2 	Concatenation of $txt1 and $txt2 	
                .= 	Concatenation assignment 	$txt1 .= $txt2 	Appends $txt2 to $txt1


        7. Array

                + 	    Union 	        $x + $y 	Union of $x and $y 	
                == 	    Equality 	    $x == $y 	Returns true if $x and $y have the same key/value pairs 	
                === 	Identity 	    $x === $y 	Returns true if $x and $y have the same key/value pairs in the same order and of the same types 	
                != 	    Inequality 	    $x != $y 	Returns true if $x is not equal to $y 	
                <> 	    Inequality 	    $x <> $y 	Returns true if $x is not equal to $y 	
                !== 	Non-identity 	$x !== $y 	Returns true if $x is not identical to $y


        8. Conditional assignment

                ?: 	    Ternary 	        $x = expr1 ? expr2 : expr3 	    Returns the value of $x. The value of $x is expr2 if expr1 = TRUE. The value of $x is expr3 
                ?? 	    Null coalescing 	$x = expr1 ?? expr2 	        Returns the value of $x. The value of $x is expr1 if expr1 exists, and is not NULL. If expr1 does not exist, or is NULL, the value of $x is expr2. Introduced in PHP 7



CONDITIONAL STATEMENTS: IF & ELSE & ELSEIF

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



FUNCTIONS

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


ARRAYS

    Types:
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



LOOPS

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