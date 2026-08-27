## <center> __University of Santo Tomas – Faculty of Engineering Electronics Engineering Department__ </center>
## <center> __ECE 2112: Advanced Computer Programming and Algorithms__ </center>
# <center> __EXPERIMENT 1: INTRODUCTION TO PYTHON PROGRAMMING__ </center> 
#### Emmanuelle D.G. Miran| 2ECE-C
## **I.** Intended Learning Outcomes
1. Use basic Python functions, operators, and string operations;
2. Manipulate strings using indexing, slicing, and built-in string methods;
3. Apply sequence unpacking to manipulate the elements of a list; and
4. Construct simple Python functions that return a specified result.

## **II.** Programming Problems
>  ##  **A.** WORD ROTATION PROBLEM

> Create a function named rotate word() that accepts a non-empty string. Move the first character of the string to the end while keeping all remaining characters in their original order. Preserve the capitalization of every character.
>> For this programming problem, we would need to be able to identify the whole text given and identify which position they are in. With that in mind, we shall identify each and every letter by using ***string indexing***. We also use something called ***string slicing***, which is used to extract a specific part of a word depending on the value you use in the [ ]. Python uses a 0-based indexing system, so the letters will be identified by [0] as the first letter in the given text.
>> 
>> In this specific problem, the functions that we used are the following.
>> 
>> ***String Indexing:*** [1:] - This is used to identify every single letter in the word, starting from the second letter.
>> 
>> ***String Slicing:*** [0] - This is used to extract the first letter of the given word in the function.
> ## CODE
def rotate_word(text):
    return text[1:] + text[0]
