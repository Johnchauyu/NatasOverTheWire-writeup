[URL](http://natas4.natas.labs.overthewire.org/)
username: natas4
password: tKOcJIbzM4lTs8hbCmzn5Zr4434fGZQm

Showed "Access disallowed" after accessing the website.
![[Level4.png]]

Inspected the source code of the page and no findings. 
Therefore, I clicked the "Refresh page" button and found that the text in the white box changes.
![[Level4_refreshpage.png]]
- Found that the file path shown in the browser changed
- There is a new link included in the text inside the white box

The change in file link indicate that the "Refresh page" button is not actually refreshing the page but bring me to a new page.
Right after I am brought to another page, the original page (http://natas4.natas.labs.overthewire.org/) that I am browsing showed up in the text inside white box.

The changes in the text make me suspect that it is detecting the [referer](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referer) in my HTTP request. And I verified my suspect in the network tab of the browser.
![[Level4_networktab.png]]

The hidden password can be found by "curl" command with the modified referer header.
![[Level4_curl.png]]

It can also be done by BurpSuite.
![[Level4_burp.png]]