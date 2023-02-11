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
Note: This image only shows the first lines of text, but more are displayed.

The first example demonstrates searching for "San Diego Padres," in the California-WhatToDo.txt file with and without highlights. The second example demonstrates the first couple lines of text searching for "San" in California-WhatToDo.txt. As you can see from the images, when color is on, it is much easier to instantly find the keywords searched for. See the sources list for sources used.

## Make grep List Files Containting the Search Item
Another useful feature of grep is that it can also list the file names of files matching the pattern. You can do this using -l, which prints file names containing that pattern. This is useful if you want to get a list of files containing the pattern, but you don't want to see the actual text lines of each file. The -r is necessary to recursively search a directory, since we are inputting a directory rather than a single file.
Code examples:
```
$ grep -l "the beach and" written_2/travel_guides/berlitz2/*.txt
$ grep -l -r "in California" written_2/ //example using -r with a directory
```

Here are the outputs of the examples:

![image](https://user-images.githubusercontent.com/122569404/218027664-99eabeaa-f9a0-479f-bff6-28b02bcab3b4.png)

![image](https://user-images.githubusercontent.com/122569404/218027174-26812376-e5cf-4c55-860f-eab08f8da9d7.png)

The 1st image demonstrates which text files in the berlitz2 folder have the words "the beach and". The 2nd image demonstrates which text files have the "in California" text in the written_2/ directory (using recursive searching). This is great for seeing which files have a particular pattern in a simple manner, without seeing the actual file text. See the sources list for sources used.

## Make grep find files that do not match the Search Item
In grep, you can also do a kind-of inverse search, finding all lines that do not match a given pattern. This could be useful if there are features in a line or file you know you don't want. You can do this through the -v token, which finds anything that does not match the pattern.

Code examples:
```
$ grep -v "a" written_2/travel_guides/berlitz2/California-WhatToDo.txt
$ grep -v "and" written_2/travel_guides/berlitz2/California-WhatToDo.txt | grep -v "to" | grep -v "has"
```

Here are the outputs of the examples:

![image](https://user-images.githubusercontent.com/122569404/218030142-210ae5ba-3cd2-4b99-a0bd-e7253a3853ae.png)
![image](https://user-images.githubusercontent.com/122569404/218030627-640870e8-361e-4b16-ab4d-bfe943d79a64.png)

In the 1st example, I am searching for all lines in California-WhatToDo.txt for any lines that do not have a "a" letter. In the 2nd example, I use -v as well as the pipe operator to search for all lines that do not have an "and", "to", or "has". Only lines missing these 3 strings are displayed. This command is useful if you want only want lines or files that do not have a specific feature. See the sources list for sources used.

## Make grep Display Line Numbers for Matches
Grep can also display line numbers for matches, so you know where in a file the pattern had matched. You can show line numbers using -n. This is useful to get the specific location(s) in the file(s) that the pattern had matched.

Code examples:
```
$ grep -n --color="always" "beaches" written_2/travel_guides/berlitz2/California-WhatToDo.txt
$ grep -r -n --color="always" "waterskiing," written_2/
```

Here are the outputs of the examples:

![image](https://user-images.githubusercontent.com/122569404/218032131-bfc00910-834d-44b6-984f-138c3515531b.png)
![image](https://user-images.githubusercontent.com/122569404/218032669-e6b57198-9048-45e4-a860-5a45b01e0f7e.png)


The 1st example is showing the line numbers of all lines in California-WhatToDo.txt with "beaches" in it (color was turned on to see it better). We can see that "beaches" is on lines 11, 12, and 15. The 2nd example is recursively searching through all files in the written_2/ directory for any files matching "waterskiing" and we can see the file and what line contains this pattern (color was turned on to see it better). This command is useful to know which line in a file had the pattern match. See the sources list for sources used.

## Sources
This [Source](https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/) was used in the research for the information above as well as the following grep help command:
```
$ grep --help
```

MLA Citation:

Moorthy, S. (2009, March 26). *15 practical GREP command examples in linux / unix.* The Geek Stuff. Retrieved February 9, 2023, from    https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/ 
