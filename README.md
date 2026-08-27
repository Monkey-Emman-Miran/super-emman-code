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
>  ##  **C.** BOOKEND SWAP PROBLEM
> Create a function named swap bookends() that accepts a list containing at least two elements. Unpack the list into three variables:

><br><br> **first – the first element;**
><br><br> **middle – a list containing everything between the first and last elements; and**
><br><br> **last – the last element.**
><br><br> Using these variables, return a new list in which the first and last elements have exchanged positions. The elements in the middle must remain in their original order. Do not modify the input list
>> For this problem, we are asked to take the given input text and rearrange it in the order of ***Last -> Middle -> First*** because we only asked to swap the first and last input element, as the middle element remains in place. To solve this problem, we can use something called ***sequence unpacking***, which allows us to assign an order or sequence to the given elements.
>> <br><br>An easy way to visualize this is by using this example.
>> <br><br> 1, *2, 3 = [cat, dog, monkey, rat,]
>> <br><br> In this example, the elements inputted on the right-hand side of the ***=*** will be assigned a digit from the right-hand side.
>> <br><br> 1 = cat
>> <br><br> 2 = dog, monkey
>> <br><br> 3 = rat
>> <br><br> By assigning the input text a position, we can easily just swap the first and last elements in the return function. For sequence unpacking so that we would be able to assign multiple texts into one element, we will use an * as shown above to group them together.

> ## CODE
```python
def swap_bookends(items):
    first, *middle, last = items
    return [last] + middle + [first]
```
> ## Outputs
```python
swap_bookends([1, 2, 3, 4, 5, 6])
```
 ```[6, 2, 3, 4, 5, 1]```
```python
swap_bookends(["red", "green", "blue"])
```
```['blue', 'green', 'red']```
```python
swap_bookends([8, 3])
```
```[3, 8]```

To view and test the code:
- Download ```'ECE2112_PA.ipynb'``` that is located in this repository
- Open via any Interactive Python Notebook (e.g., Google Colab or Jupyter Notebook)
- Upload and run the file

**README File Version History:**

```August 27, 2026``` - Initial README.md and .ipynb file was uploaded.
