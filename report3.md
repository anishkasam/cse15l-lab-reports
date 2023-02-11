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

#### Example #2:
