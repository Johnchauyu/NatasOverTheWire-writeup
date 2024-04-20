## Natas Level 6

[URL](http://natas6.natas.labs.overthewire.org) <br>
username: natas6 <br>

There is one obvious input field once accessed the web page. <br>
![Level6.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level6/Level6.png) <br>

After clicking that 'View sourcecode' button, the below code are shown. <br>
![Level6_SourceCode.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level6/Level6_SourceCode.png) <br>
```
<html>
<head>
<!-- This stuff in the header has nothing to do with the level -->
<link rel="stylesheet" type="text/css" href="http://natas.labs.overthewire.org/css/level.css">
<link rel="stylesheet" href="http://natas.labs.overthewire.org/css/jquery-ui.css" />
<link rel="stylesheet" href="http://natas.labs.overthewire.org/css/wechall.css" />
<script src="http://natas.labs.overthewire.org/js/jquery-1.9.1.js"></script>
<script src="http://natas.labs.overthewire.org/js/jquery-ui.js"></script>
<script src=http://natas.labs.overthewire.org/js/wechall-data.js></script><script src="http://natas.labs.overthewire.org/js/wechall.js"></script>
<script>var wechallinfo = { "level": "natas6", "pass": "<censored>" };</script></head>
<body>
<h1>natas6</h1>
<div id="content">

<?

include "includes/secret.inc";

    if(array_key_exists("submit", $_POST)) {
        if($secret == $_POST['secret']) {
        print "Access granted. The password for natas7 is <censored>";
    } else {
        print "Wrong secret";
    }
    }
?>

<form method=post>
Input secret: <input name=secret><br>
<input type=submit name=submit>
</form>

<div id="viewsource"><a href="index-source.html">View sourcecode</a></div>
</div>
</body>
</html>
```

We only need to pay attention to this part of the code as it is responsible to handle our input. <br>
```
<?

include "includes/secret.inc";

    if(array_key_exists("submit", $_POST)) {
        if($secret == $_POST['secret']) {
        print "Access granted. The password for natas7 is <censored>";
    } else {
        print "Wrong secret";
	}
    }
?>
```
In order to print out the password for the next level, the value of the variable: secret that we submitted through the HTTP POST request has to be same as the defined value of another variable: secret. <br>
And by inputting 'testing' in the field, it can be sure that the inputted value determines the value of variable: secret in the HTTP POST request. <br>
![Level6_secret.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level6/Level6_secret.png) <br>

Then I visited the link provided in `include "includes/secret.inc";`. Found that it is an empty page and the value of secret, `FOEIUWGHFEEUHOFUOIU`, is hidden in the HTML code. <br>
![Level6_secretpage.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level6/Level6_secretpage.png) <br>

Input the found value of variable: secret into the input field and the password for next level is revealed. <br>
![Level6_accessgranted.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level6/Level6_accessgranted.png) <br>
