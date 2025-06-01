# EX 6D BRUTE FORCE ALGORITHM

## DATE : 20-05-25

## AIM :

To create a python program using brute force method of searching for the given substring in the main string.

## Algorithm :

1.Take two inputs: the main string and the substring to search for.

2.Create a regex pattern using the substring.

3.Search for the first match of the pattern in the main string.

4.If a match is found.Print the starting index of the match.

5.Continue searching for the next match, starting just after the current match.

6.Repeat step 4 until no more matches are found.

## Program:

```
/*
 Developed by: Vishinu H
 Register Number: 212223220124
*/

def match(string,sub):
    l = len(string)
    ls = len(sub)
    ########### Add your code here #######
    i = j = 0
    found = False
    while i <= l - ls:
        j = 0
        while j < ls and string[i + j] == sub[j]:
            j += 1
        if j == ls:
            print("Found at index", i)
            found = True
        i += 1
    
    if not found:
        print("Not Found")

str1=input()
str2=input()

```

## Output :

![image](https://github.com/user-attachments/assets/75c27e26-c4dc-456e-971d-5c5ae641cb61)


## Result :

Thus the above program was executed successfully for searching the substring at respective index.
