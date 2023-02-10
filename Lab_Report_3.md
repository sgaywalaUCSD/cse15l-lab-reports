# CSE15L Lab Report 3 Researching Commands
Siddharth Gaywala
CSE15L

***

## Make grep Highlight the word
A useful feature of grep is that it can highlight the parameter you are searching for. You can do this using --color=never, --color=always, or 
--color=auto to specify grep to not highlight the text, always highlight the text, or reference default settings. It is useful, because you might grep a keyword, but
if the text is already highlighted, that text will jump out at you and it is much easier to find the words you were looking for in a large paragraph.
Here is an example:
```
$ grep --color=always  "San Diego Padres," written_2/travel_guides/berlitz2/California-WhatToDo.txt
$ grep --color=never  "San Diego Padres," written_2/travel_guides/berlitz2/California-WhatToDo.txt
```


![image](https://user-images.githubusercontent.com/122569404/217982576-c8341236-af4f-4e65-bbeb-97c55cfa3643.png)

And here is another example:
```
$ grep --color=never  "San" written_2/travel_guides/berlitz2/California-WhatToDo.txt
$ grep --color=always  "San" written_2/travel_guides/berlitz2/California-WhatToDo.txt
```

![image](https://user-images.githubusercontent.com/122569404/217982844-96ccd20d-9ec6-463a-b758-930304761538.png)
![image](https://user-images.githubusercontent.com/122569404/217982875-cda00c4d-084b-4538-8f5b-abd4a550bd4e.png)

As you can see from the images, when color is on, it is much easier to instantly find the keywords searched for.

## Make grep Search a Directory Recursively
Another useful feature of grep is that it can search directories also, instead of just individual files. (combine with next one)

## Make grep List Files Containting the Search Item

## Make grep find files that do not match the Search Item
- make it so that it searches california for any files w/o and

## Make grep Have Some Tolerance For Mismatches

choose either less, find, or grep (1x)
find 4 interesting options/ways to use the command
for each, give 2 examples using it in written_2/ w/ code block and sentence on what its doing / why useful

cite source for each: https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/
