[URL](http://natas1.natas.labs.overthewire.org)
username: natas1
password: g9D9cREhslqBKtcA2uocGHPfMZVzeFK6

Indicated by the hint, password should be hidden by similar way as Level 0 does.
![[Level1_website.png]]

When trying to right click in the white box, a window will pop out saying that "right click has been disabled".
![[Level1_popup.png]]

One easy solution is that you can right click outside the white box and you can inspect the website.
![[Level1_rc.png]]

Another solution is to use Linux command "curl -u"
![[curl.png]]
Password is obtained after curl result is returned
![[CurlResult.png]]
Password can also be found by inspecting the page
![[Level1_InsepctResult.png]]
