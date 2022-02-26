# Lab Report 4

* my repo: https://github.com/AndrewJia/markdown-parse
* reviwed repo: https://github.com/xis004/markdown-parse

## Snippet 1

![Snippet 1 Preview](./report4-images/previewSnippet1.png)

* intended output: ["`google.com", "google.com", "ucsd.edu"]

<br>
My result - failed

![My Result 1](./report4-images/s1MyRes.png)


Reviewed result - failed
![Reviewed Result 1](./report4-images/xi1.png)

How to fix
* My understanding of `s: brackets or parenthesis within two of them do not count toward formatting
* I think the fix could be done within 10 lines, but it migh take me ~20
* After finding a local variable (nextOpenBracket, nextCloseBracket, openParen, closeParen), check if it is between the first and second `, or third and fourth, etc. If it is, recalculate the bracket/parenthesis 

## Snippet 2

![Snippet 2 Preview](./report4-images/previewSnippet2.png)

* intended output: ["a.com", "a.com(())", "example.com"]

<br>
My result - failed

![My Result 2](./report4-images/s2MyRes.png)


Reviewed result - failed
![Reviewed Result 2](./report4-images/xi2.png)

How to fix
* I don't think this can be done within 10 lines.
* From my understanding, I don't fully understand how nested brackets work, so I'm just assuming this is complicated enough that it takes more than 10 lines.
* In addition, we check if there is a \ in front of a bracket. If there is, we have to ignore it

## Snippet 3

![Snippet 3 Preview](./report4-images/previewSnippet3.png)

* intended output: ["https://ucsd-cse15l-w22.github.io/"]

<br>
My result - failed

![My Result 3](./report4-images/s3MyRes.png)


Reviewed result - failed
![Reviewed Result 3](./report4-images/xi3.png)


How to fix
* I think this can be done within 10 lines.
* From my understanding, line breaks are allowed within the brackets as long as there aren't two in a row. Line breaks are allowed before and after the url, as long as there aren't two in a row.
* String trim should be able to trim off the line breaks from the input string (the string between the openParen and closeParen)
* One way to check the brackets is to simply do a for loop, iterating on each character. If it is a line break and the next character is a line break, the link is invalid.