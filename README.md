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
```python
def rotate_word(text):
    return text[1:] + text[0]
```
> ## Outputs
```python
rotate_word("python")
```
```'ythonp'```
```python
rotate_word("logic")
```
```'ogicl'```
```
```python
rotate_word("Code")
```
```'odeC'```
```python
rotate_word("A")
```
```'A'```
>  ##  **B.** WORD USERNAME BUILDER PROBLEM
>  Create a function named make username() that accepts two strings: first name and last name. The
function must:
><br>1. Convert all letters to lowercase;
><br>2. Remove all spaces from the first name;
><br>3. Remove all spaces from the last name; and
><br>4. Join the processed first and last names using one period (.).
>> For this programming problem, we are tasked to combine two different texts together, with the conditions that the given texts are to be converted into lowercase, and they are joined together with one period. This could be done by using the function ***.lower()***, which converts the given text into lower case. The last condition that needs to be met is to convert the given text to have no spaces in between when merging it in the output. This problem can be solved by using the function ***.replace()***
>> <br><br>
>> ***.lower()*** - This is used to convert the given text from the input into lowercase.
>> <br><br>
>> ***.replace*** (" ", "") - The reasoning for why we use this function is so we replace every single blank space indicated by the ***" "*** with an empty string represented by ***""***.
> ## CODE
```python
def make_username(first_name, last_name):
    lower_first = first_name.lower() .replace(" ", "")
    lower_last = last_name.lower() .replace(" ", "")
    return lower_first + "." + lower_last
```
> ## Outputs
```python
make_username("Ada", "Lovelace")
```
```'ada.lovelace'```
```python
make_username("Alan", "Turing")
```
```'alan.turing'```
```python
make_username("Ana Maria", "De Leon")
```
```'anamaria.deleon'```
