##Natas Level 1

[URL](http://natas1.natas.labs.overthewire.org) <br>
username: natas1 <br>

Indicated by the hint, password should be hidden by similar way as Level 0 does. <br>
![Level1_website.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level1/Level1_website.png) <br>

When trying to right click in the white box, a window will pop out saying that "right click has been disabled". <br>
![[Level1_popup.png]](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level1/Level1_popup.png) <br>

One easy solution is that you can right click outside the white box and you can inspect the website. <br>
![Level1_rc.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level1/Level1_rc.png) <br>

Another solution is to use Linux command "curl -u" <br>
![curl.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level1/curl.png) <br>

Password is obtained after curl result is returned <br>
![CurlResult.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level1/CurlResult.png) <br>

Password can also be found by inspecting the page <br>
![Level1_InsepctResult.png](https://github.com/Johnchauyu/NatasOverTheWire-writeup/blob/main/Screenshots/Level1/Level1_InsepctResult.png) <br>
