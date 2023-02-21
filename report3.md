# Lab Report 3

## Researching Commands

### grep -l

Source: [geeksforgeeks](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)

#### Example #1:

Input:  
```
grep -rl "Jamaica" written_2/
```

Output:
```
written_2//non-fiction/OUP/Castro/chB.txt
written_2//travel_guides/berlitz1/HistoryJamaica.txt
written_2//travel_guides/berlitz1/HandRJamaica.txt
written_2//travel_guides/berlitz1/WhatToIsrael.txt
written_2//travel_guides/berlitz1/IntroJamaica.txt
written_2//travel_guides/berlitz1/HistoryFWI.txt
written_2//travel_guides/berlitz1/WhatToJamaica.txt
written_2//travel_guides/berlitz2/Boston-WhereToGo.txt
written_2//travel_guides/berlitz2/Bahamas-WhatToDo.txt
written_2//travel_guides/berlitz2/Cuba-WhereToGo.txt
written_2//travel_guides/berlitz2/Bahamas-History.txt
```

This command recursively searches the directory for the phrase "Jamaica". It iterates through all the files and returns all of the file that contain "Jamaica". This command is useful because you may need to know which files contain a certain term. 

#### Example #2:

Input:
```
grep -rl "plantains" written_2/
```

Output:
```
written_2//travel_guides/berlitz1/IntroFWI.txt
written_2//travel_guides/berlitz1/WhatToJamaica.txt
written_2//travel_guides/berlitz2/PuertoRico-WhereToGo.txt
```

This command recursively searches the directory for the phrase "plantains". It iterates through all the files and returns all of the file that contain "plantains". This command is useful because you may need to know which files contain a certain term.

### grep -n

Source: [geeksforgeeks](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)

#### Example #1:

Input:
```
grep -nr "plantains" written_2/
```

Output:
```
written_2//travel_guides/berlitz1/IntroFWI.txt:90:        red pimentos, and plantains.
written_2//travel_guides/berlitz1/WhatToJamaica.txt:425:        of coffee, bananas, plantains, and sugar cane. The well-informed guides
written_2//travel_guides/berlitz2/PuertoRico-WhereToGo.txt:110:From the caves it’s a short drive to Lares, the island’s center of coffee production. The sweet brew made from Puerto Rican beans is considered one of the finest in the world, though production is small. Coffee plants, usually interspersed with other crops such as bananas or plantains, can be seen growing on the high hillsides; it is a crop that enjoys good drainage and lots of humidity, which the large banana leaves help to conserve.
```

This command recursively searches the given directory for the phrase "plantains". It iterates through all of the files and returns the file, the line number where the phrase is, and the line itself. This command is useful if you want to not only find the files where the phrase occurs, but also where in the file that phrase occurs.

#### Example #2:

Input: 
```
grep -nr "coffee beans" written_2/
```

Output:
```
written_2//travel_guides/berlitz1/WhatToJamaica.txt:774:        being roasted and ground; you can also buy supplies of coffee beans to
written_2//travel_guides/berlitz2/Cuba-WhereToGo.txt:182:A tortuous side road 12 km (7 miles) east along the coast ascends the mountains to La Gran Piedra (Big Stone), where you can climb on foot for a bird’s-eye view of eastern Cuba. About 2 km (about a mile) beyond, a passable dirt track leads to Museo La Isabelica, a 19th-century coffee-plantation finca (country house) with a workshop, original furniture, and a concrete garden where coffee beans were once laid out to dry.
```

This command recursively searches the given directory for the phrase "coffee beans". It iterates through all of the files and returns the file, the line number where the phrase is, and the line itself. This command is useful if you want to not only find the files where the phrase occurs, but also where in the file that phrase occurs.

### grep -c

Source: [geeksforgeeks](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)

#### Example #1:

Input:
```
grep -rc "the" written_2/
```

Output (*Trimmed*):
```
written_2//non-fiction/OUP/Berk/ch2.txt:183
written_2//non-fiction/OUP/Berk/ch1.txt:153
written_2//non-fiction/OUP/Berk/CH4.txt:189
written_2//non-fiction/OUP/Berk/ch7.txt:125
written_2//non-fiction/OUP/Abernathy/ch2.txt:63
written_2//non-fiction/OUP/Abernathy/ch3.txt:50
...
```

This command searches each file and returns the number of occurrences of the specified phrase in that file. It iterates through every single file and shows the number of times "the" appears in the file. This command is useful since you can find the frequency of a phrase in a file. For example, you can find which file has the most information on a certain topic by finding the number of occurrences of a certain term. Some files may mention the term in passing and only have 1 or 2 occurrences of a word, while other files may go in depth on the term and have a lot of occurrences. The number of occurrences can tell you which file has the most information on the term you're searching for.

#### Example #2:

Input:
```
grep -rc "Fidel Castro" written_2/
```

Output (*Trimmed*):
```
...
written_2//travel_guides/berlitz2/Athens-WhatToDo.txt:0
written_2//travel_guides/berlitz2/Nepal-WhatToDo.txt:0
written_2//travel_guides/berlitz2/Bermuda-WhereToGo.txt:0
written_2//travel_guides/berlitz2/Paris-WhatToDo.txt:0
written_2//travel_guides/berlitz2/Cuba-History.txt:1
written_2//travel_guides/berlitz2/Vallarta-WhereToGo.txt:0
written_2//travel_guides/berlitz2/Bahamas-History.txt:1
written_2//travel_guides/berlitz2/Beijing-WhatToDo.txt:0
written_2//travel_guides/berlitz2/Cancun-WhereToGo.txt:0
```

This command searches each file and returns the number of occurrences of the specified phrase in that file. It iterates through every single file and shows the number of times "Fidel Castro" appears in the file. This command is useful since you can find the frequency of a phrase in a file. For example, you can find which file has the most information on a certain topic by finding the number of occurrences of a certain term. Some files may mention the term in passing and only have 1 or 2 occurrences of a word, while other files may go in depth on the term and have a lot of occurrences. The number of occurrences can tell you which file has the most information on the term you're searching for.

### grep -L

Source: [man7](https://man7.org/linux/man-pages/man1/grep.1.html)

#### Example #1:

Input:
```
grep -rL "history" written_2/
```

Output (*Trimmed*):
```
written_2//non-fiction/OUP/Berk/CH4.txt
written_2//non-fiction/OUP/Berk/ch7.txt
written_2//non-fiction/OUP/Abernathy/ch3.txt
written_2//non-fiction/OUP/Abernathy/ch7.txt
written_2//non-fiction/OUP/Abernathy/ch8.txt
written_2//non-fiction/OUP/Abernathy/ch9.txt
written_2//non-fiction/OUP/Abernathy/ch14.txt
written_2//non-fiction/OUP/Rybczynski/ch2.txt
written_2//non-fiction/OUP/Rybczynski/ch1.txt
...
```

This command searches each file for the phrase "history" and if the file doesn't contain the phrase, the command outputs the file. This command is useful to find files where certain phrases are ommitted. For example, if you have a directory of a bunch of attendance logs, and each file contains the names of the students present for a certain date. You would want to know which dates a student wasn't present in class. 

#### Example #2:

Input:
```
grep -rL "United States" written_2/
```

Output (*Trimmed*):
```
written_2//non-fiction/OUP/Berk/ch2.txt
written_2//non-fiction/OUP/Abernathy/ch6.txt
written_2//non-fiction/OUP/Abernathy/ch14.txt
written_2//non-fiction/OUP/Rybczynski/ch2.txt
written_2//non-fiction/OUP/Rybczynski/ch1.txt
written_2//non-fiction/OUP/Kauffman/ch1.txt
written_2//non-fiction/OUP/Kauffman/ch4.txt
written_2//non-fiction/OUP/Kauffman/ch5.txt
written_2//non-fiction/OUP/Kauffman/ch7.txt
...
```

This command searches each file for the phrase "United States" and if the file doesn't contain the phrase, the command outputs the file. This command is useful to find files where certain phrases are ommitted. For example, if you have a directory of a bunch of attendance logs, and each file contains the names of the students present for a certain date. You would want to know which dates a student wasn't present in class. 
