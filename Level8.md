[URL](http://natas8.natas.labs.overthewire.org)
username: natas8
password: a6bZCNYwdKqN5cGP11ZdtPg0iImQQhAB

This level is similar to level 6. There is the "View source code" button again.
![[level8.png]]

Below is the source code shown. And only the coloured part in the middle matters.
![[level8_sourcecode.png]]

The code below defined the value for variable "encodedSecret".
And provided a function "encodeSecret" to modify the parameter that is passed to the function.

Whenever we send any value in the "Input secret: " field in the first page, the submitted value will be sent to the function "encodeSecret" and compare its modified value with the predefined variable "encodedSecret".
Only if the modified value equals the predefined variable "encodedSecret", the password for the next level will show.

The goal is to craft the value that turn out to have the same value of parameter "encodedSecret" after being passed to function "encodeSecret".
```
<?      

$encodedSecret = "3d3d516343746d4d6d6c315669563362";      

function encodeSecret($secret) {       return bin2hex(strrev(base64_encode($secret)));   
}      

if(array_key_exists("submit", $_POST)) {       if(encodeSecret($_POST['secret']) == $encodedSecret{
		print "Access granted. The password for natas9 is <censored>";       } else {       
		print "Wrong secret";       
	}   
}   
?>
```

Function "encodeSecret" handle the input value like below:
Input value --> Base 64 encode --> Reverse the string --> Convert to hexadecimal

In order to let function "encodeSecret" return value of variable "encodedSecret", I reverse the order of how the function "encodeSecret" handle the parameter passed in with following code.
Input value --> Convert to binary --> Reverse the string --> Base 64 decode
```
<?php
 
$input = "3d3d516343746d4d6d6c315669563362";

$first_operation = hex2bin($input);
$second_operation = strrev($first_operation);
$third_operatoin = base64_decode($second_operation);

echo $third_operatoin;

?>
```

By input the following result into the "Input secret" field, the key for next level is shown.
![[level8_decodeResult.png]]
![[level8_success.png]]
