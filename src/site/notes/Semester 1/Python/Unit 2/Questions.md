---
{"dg-publish":true,"permalink":"/semester-1/python/unit-2/questions/"}
---


# Unit 2 Questions and Answers

---

## Question Bank

                                      Question Bank 2

Topic: Collections & Functions


True or False Questions

1.True or False? A list in Python is an immutable linear data structure.


2.True or False? A list traversal is a means of accessing one-by-one, the elements of a list.


3.True or False? Lists and tuples are denoted by the use of square brackets.


4.True or False? Lists and tuples must each contain at least one element.


5.True or False? Lists are denoted by use of parentheses and tuples are denoted by the use of

square brackets.


6.True or False? In List append and extend operations are same.


7.True of False? The tuple element can be nmodified,if th element is list.


8.True or False? Some string methods alter the string they are called on, while others return a

new altered version of the string.


9.True or False? The find method returns the number of occurrences of a character or substring

within a given string.


10.True or False? String method isdigit returns true if the string applied to contains only digits.


11.True or False? Only files that are written to need to be opened first.


12.True or False? When calling the built-in open function, a second argument of 'r' or 'w' must

always be given.
13..True or False? calling the built-in open function, a second argument of 'r' must always be

given when opening a file for reading.


14.. True or False? calling the built-in open function, a second argument of 'w' must always be

given when opening a fi le for writing.


15.True or False? There is more chance of an I/O error when opening a file for reading.


16.True or False? The readline method reads every character from a text fi le up to and

including the next newline character '\n'.


17.True or False? It is especially important to close a file that is open for writing


Questions

   18. What is meant by data structures?

   19. What is tuple ? What is the difference between list and tuple?

   20. What is docstring?

   21. What is a function? Mention the type of function and use.

   22. What are Python's dictionaries?

   23. Indicate the reasons for IOError (exception) may occur when opening a file.

   24. What would be the range of index values for a list of 10 elements?

   25. Mention the list operations does not need to be provided an index value?

   26. What is the process of accessing each element of a list, one-by-one?

   27. List out the chractersics of lists in Python?

   28. Write down the proper way to denote an empty list in Python?

   29. What is the correct way to access the fourth element of a list named lst?

   30. Indicate the use of Square brackets are used with lists in Python?

   31. Which of the following is not a valid list in Python?
    (a) [85, 'sunny', ‘June 5’]

    (b) [10; 20; 30]

    (c) ['one', 'two', 'three']

    (d) all of the above

    32. For lst = [10, 20, 30, 40, 50], what value is accessed by list[3]?

    33. What should the value of k be for lst[k] to access the tenth element of list lst?

    34. For lst = [10, 20, 30, 40, 50], what value is the value of lst after del lst[3] is performed?

    35. For lst = [10, 20, 30, 40, 50], what value is the value of lst after lst.append(0) is

    performed?

    36. For lst = [10, 20, 30, 40, 50], what is the resulting value of lst[2:4]?

    37. For some list lst, what will be the result of the execution of the (a)instruction lst.insert(1,

    3)?

    38. Write the proper notation for a tuple of only one element?

    39. Mention the operations cannot be used with tuples?

    40. For nested list lst = [ [10, 20, 30], [40, 50, 60] ], Write the correct form of assessing the

    element with the value 40?

    41.Which of the following lists are syntactically correct in Python?

    (a) [1, 2, 3, 'four'] (b) [1, 2, [3, 4]] (c) [[1, 2, 3]['four'\|1, 2, 3]['four']]

    42.For lst [4, 2, 9, 1], what is the result of each of the following list operations?

    (a) lst[1] (b) lst.insert(2, 3) (c) del lst[3] (d) lst.append(3)

    43. For fruit 5 ['apple', 'banana', 'pear', 'cherry'], use a list operation to change the list to

['apple', 'banana', 'cherry'] .

    44. For a list of integers, lst, give the code to retrieve the maximum value of the second half

of the list.

     45. For variable product_code containing a string of letters and digits,
    (a) Give an if statement that outputs “Verified” if product_code contains both a “Z” and a “9”,

and outputs “Failed” otherwise.

    (b) Give a Python instruction that prints out just the last three characters in product_code.

    46. Write the valid operations possible on tuples (for tuples t1 and t2)?

    47. For str15 'Hello World', answer the following,

    (a) Give an instruction that prints the fourth character of the string.

    (b) Give an instruction that fi nds the index location of the fi rst occurrence of the letter 'o' in

the string.

    48. Identify suitable string functions to recognize the following string type:

    i) char in 'ABCDEFGHIJKLMNOPQRSTUVWXYZ' or \

    ii) char in 'abcdefghijklmnopqrstuvwxyz' or \

    iii) char in '0123456789' 44.

    49. Which of the results below does s.strip('-')return for the string s 5 '---ERROR---'.

    (a) '---ERROR’

    (b) 'ERROR---'

    (c) 'ERROR'

    50. Indicate which of the following s.replace('c','e')returns for s 5 'abcabc'.

    (a) 'abeabc'

    (b) 'abeabe'

    51. Indicate following that are syntactically correct for creating a set.

    (a) set([1, 2, 3])

    (b) set((1, 2, 3))

    (c) {1, 2, 3} 47.

    52. For set s containing values 1, 2, 3, and set t containing 3, 4, 5, which of the following are

the correct results for each given set operation?

    (a) s | t➝{3}
    (b) s & t➝{1, 2, 3, 4, 5}

    (c) s 2 t➝{1, 2}

    (d) s ^ t➝{1, 2, 4, 5}



    Fill in the Blanks

    53. In List The size can be __________to grow in increase or decrease of elements.

    54. In tuple, elements are enclosed in _____symbol.

    55. The ______ is immutable collection type in Python.

    56. A ______ is a mutable data type with nonduplicate, unordered values, providing the

usual mathematical set operations in Python.

    57. A dictionary type in Python is an associative data structure that is accessed by a

_______________ rather than an index value.

    58. __________ string function returns copy of str with all leading and trailing characters

that appear in string removed.

    59. In Python, when a fi le is opened, a _____________is created that provides methods for

accessing the file.



Programming exercise

60. For a list of integers named nums,

(a) Write a while lo op that adds up all the values in nums.

(b) Write a for loop that adds up all the values in nums in which the loop variable is assigned

each value in the list.

(c) Write a for loop that adds up all the elements in nums in which the loop variable is assigned

to the Index value of each element in the list.

(d) Write a for loop that displays the elements in nums backward.
(e) Write a for loop that displays every other element in nums, starting with the first element.

61. For a nested list lst that contains sublists of integers of the form [n1, n2, n3]

(a) Give a Python instruction that determines the length of the list.

(b) Give Python code that determines how many total integer values there are in list lst.

(c) Give Python code that totals all the values in list lst.

(d) Given an assignment statement that assigns the third integer of the fourth element (sublist)

of lst to the value 12.

62. Examine the following lines of Python code:

lst1 = [1, 2, 3, 4]

lst2 = [1, 2, 3, 4] l

st1 == lst2

What will be the output?

63. Write a Python program that prompts the user for a list of integers, stores in another list only

those values between 1–100, and displays the resulting list.

64. Write a Python program that prompts the user for a list of integers, stores in another list only

those values that are in tuple valid_values, and displays the resulting list.

65. Write a Python program that prompts the user for a list of integers and stores them in a list.

For all values that are greater than 100, the string 'over' should be stored instead. The program

should display the resulting list.

66. Write a Python program that prompts the user to enter a list of fi rst names and stores them

in a list. The program should display how many times the letter 'a' appears within the list.

67. Write a Python program that prompts the user to enter a list of words and stores in a list only

those words whose fi rst letter occurs again within the word (for example, 'Baboon'). The

program should display the resulting list.

68. Write a Python program that prompts the user to enter types of fruit, and how many pounds

of fruit there are for each type. The program should then display the information in the form fruit
, weight listed in al- phabetical order, one fruit type per line as shown below, Apple, 6 lbs.

Banana, 11 lbs.etc.

69. Write a Python program that prompts the user to enter integer values for each of two lists. It

then should displays whether the lists are of the same length, whether the elements in each list

sum to the same value,and whether there are any values that occur in both lists.

70. For set s containing values 1, 2, 3 and set w of type frozenset containing values 'a','b','c',

which of the following are valid set operations and why?

(a) 'a' in s

(b) 'a' in w

(c) len(s) 1 len(w)

(d) s.add(4)

 (e) w.add('d')

71. For dictionary d 5 {'apples':0.66,'pears':1.25,'bananas':0.49}, which of the following correctly

updates the price of bananas and justify with reason.

(a) d[2] 5 0.52

(b) d[0.49] 5 0.52

(c) d['bananas'] 5 0.52

72. Create a dictionary ‘ODD’ of odd numbers between 1 and 10, where the key is the decimal

number and the value is the corresponding number in words. Perform the following operations

on this dictionary:

(a) Display the keys,values and items.

(b) Find the length of the dictionary

(c) Check if 7 is present or not

(d) Retrieve the value corresponding to the key 9

(e) Delete the item from the dictionary corresponding to the key 9
73. Write a program to count the number of times a vowels appears in a given string and store it

in dictionary.

74. Write a Program to perform union and intersection for the given sets:

Input: S1={‘India’,’No 1 show’,’is’ ‘a’, ‘Raisng Singing Star’} S2={‘Raising Sining Star’,’No 1

show’,’is’, ‘telecasting’,’in’, ‘SatrPlus’,’Channel’}

output: S1 U S2={‘India’,’No 1 show’,’is’ ‘a’, ‘Raisng Singing Star’,‘Raising Sining Star’,,’is’,’No 1

show’, ‘telecasting’,’in’, ‘SatrPlus’,’Channel’} S1 Intersection(S2)={‘is’,’Raising Singing Star’,’No

1 show’}

75. Write a program Update set1 by adding items from set2, except common items. Input :set1

= {10, 20, 30, 40, 50} set2 = {30, 40, 50, 60, 70} Expected output:{70, 10, 20, 60}


---

## Solved Questions & Answers

True or False Questions

1.True or False? A list in Python is an immutable linear data structure.

Answer: False

2.True or False? A list traversal is a means of accessing one-by-one, the elements of a list.

Answer: True

3.True or False? Lists and tuples are denoted by the use of square brackets.

Answer: False

4.True or False? Lists and tuples must each contain at least one element.

Answer: False

5.True or False? Lists are denoted by use of parentheses and tuples are denoted by the use

of square brackets.

Answer: False

6.True or False? In List append and extend operations are same.

Answer:False

7.True of False? The tuple element can be nmodified,if th element is list.

Answer:True

8.True or False? Some string methods alter the string they are called on, while others return

a new altered version of the string.

Answer:True

9.True or False? The find method returns the number of occurrences of a character or

substring within a given string.

Answer:True

10.True or False? String method isdigit returns true if the string applied to contains only

digits. Answer:True

11.True or False? Only files that are written to need to be opened fi rst. Answer:True

12..True or False? When calling the built-in open function, a second argument of 'r' or 'w'

must always be given.
Answer:True

13..True or False? Calling the built-in open function, a second argument of 'r' must always

be given when opening a file for reading.

Answer:True

14.. True or False? Calling the built-in open function, a second argument of 'w' must always

be given when opening a file for writing.

Answer:False

15.True or False? There is more chance of an I/O error when opening a file for reading.

Answer:True

16.True or False?The readline method reads every character from a text file up to and

including the next newline character '\n'.

Answer:True

17.True or False? It is especially important to close a file that is open for writing.

Answer:True



Questions:

   18. What is meant by data structures?

       Specialized format for organizing and retrieval of data in an efficient way

   19. What is tuple ? What is the difference between list and tuple?

       A tuple is another sequence data type that is similar to the list. A tuple consists of a number of
       values separated by commas. The main differences between lists and tuples are: Lists are
       enclosed in brackets ( [ ] ) and their elements and size can be changed, while tuples are
       enclosed in parentheses ( ( ) ) and cannot be updated.

   20. What is docstring?

       Doc string is short for documentation string. It is a string that occurs as the first
       statement in a module, function, class, or method definition. It is used to explain in
       brief, what a function does.

   21. What is a function? Mention the type of function and use.
   A Function can be called as a section of a program that is written once and can be executed
   whenever required in the program, thus making code reusability.
   There are two types of Functions.
    a) Built-in Functions: Functions that are predefined. We have used many predefined
   functions in Python.
    b) User- Defined: Functions that are created according to the requirements

22. What are Python's dictionaries?
    Dictionary is mutable associative data structure with key value pair. A dictionary key
    can be almost any Python type, but are usually numbers or strings. Values, on the
    other hand, can be any arbitrary Python object.

23. .Indicate the reasons for IOError (exception) may occur when opening a file.

   Answer:open() function when trying to open a file that does not exist. It is also raised

   for operating system-related errors.print statement fails will also raise IOError.

24. What would be the range of index values for a list of 10 elements?

    Answer:for i in range(10): print(i)

25. Mention the list operations does not need to be provided an index value?

   Answer:remove(),clear()

26. What is the process of accessing each element of a list, one-by-one?

   Answer:List Traversal

27. List out the chractersics of lists in Python?

   Answer: mutable, hashable, has zero or more elements, slicing can be done.

28. Write down the proper way to denote an empty list in Python?

   Answer:listname=[]

29. What is the correct way to access the fourth element of a list named lst?

   Answer:lst[3]

30. Indicate the use of Square brackets are used with lists in Python ?

   Answer:square brackets used to create and access elements of a list.



31. Which of the following is not a valid list in Python?

   (a) [85, 'sunny', ‘June 5’] (b) [10; 20; 30] (c) ['one', 'two', 'three'] (d) all of the above

   Answer:(b)
32. For lst = [10, 20, 30, 40, 50], what value is accessed by list[3]?

    Answer:40

33. What should the value of k be for lst[k] to access the tenth element of list lst?

    Answer:k=9

34. For lst = [10, 20, 30, 40, 50], what value is the value of lst after del lst[3] is

    performed?

    Answer:lst=[‘10,20,30,50]

35. For lst = [10, 20, 30, 40, 50], what value is the value of lst after lst.append(0) is

    performed?

     Answer:lst=[10,20,30,40,50,0]

36. For lst = [10, 20, 30, 40, 50], what is the resulting value of lst[2:4]?

     Answer:lst=[30,40]

37. For some list lst, what will be the result of the execution of the

    (a)instruction lst.insert(1, 3)?

    Answer:lst=[10,3,20,30,40,50]

38. Write the proper notation for a tuple of only one element?

    Answer:tu1=(1,)

39. Mention the operations cannot be used with tuples?

    Answer:slicing,update elemets in tuple

40. For nested list lst = [ [10, 20, 30], [40, 50, 60] ], Write the correct form of assessing

    the element with the value 40?

    Answer:lst[1][1]

41. Which of the following lists are syntactically correct in Python?

    (a) [1, 2, 3, 'four'] (b) [1, 2, [3, 4]] (c) [[1, 2, 3]['four'\|1, 2, 3]['four']]

    Answer:all are correct

42.For lst [4, 2, 9, 1], what is the result of each of the following list operations?

(a) lst[1] (b) lst.insert(2, 3) (c) del lst[3] (d) lst.append(3)

    Answer:(a)2 (b)lst=[4,2,3,9,1] (c) lst=[4,2,3,1] (d) lst=[4,2,3,1,3]
Fill in the blanks

53. In List The size can be __________to grow in increase or decrease of elements.

Answer: shrinked

54. In tuple,elements are enclosed in _____symbol.

Answer:parenthesis

55. The ______ is immutable collection type in Python.

Answer: tuple

56. A ______ is a mutable data type with nonduplicate, unordered values, providing the

usual mathematical set operations in Python.

Answer: set

57. A dictionary type in Python is an associative data structure that is accessed by a

_______________ rather than an index value.

Answer: keyvalue

58. __________ string function returns copy of str with all leading and trailing characters that

appear in string removed.

Answer: strip function

59. In Python, when a file is opened, a _____________is created that provides methods for

accessing the file.

Answer: file object

Programming exercise

63. For a list of integers named nums,

(a) Write a while loop that adds up all the values in nums.

(b) Write a for loop that adds up all the values in nums in which the loop variable is assigned

each value in the list.

(c) Write a for loop that adds up all the elements in nums in which the loop variable is

assigned to the Index value of each element in the list.

(d) Write a for loop that displays the elements in nums backwards.
(e) Write a for loop that displays every other element in nums, starting with the fi rst

element. Answer:(a) nums = int(input())

while nums != 0:

         total_sum += nums

(b) for ele in nums:

         total=total+ele

(c) for i in range(len(nums)):

         print (nums[i])

(d) for i in range (len-1(nums):

         print nums[::-i] or print nums[-i]

64. For a nested list lst that contains sublists of integers of the form [n1, n2, n3],

(a) Give a Python instruction that determines the length of the list.

(b) Give Python code that determines how many total integer values there are in list lst.

(c) Give Python code that totals all the values in list lst.

(d) Given an assignment statement that assigns the third integer of the fourth element

(sublist) of lst to the value 12.

Answer:(a) >>>len(lst)

(b)>>>for ele in lst:

                   if ele>=0:

                   total=total+ele

(c) for ele in lst:

         total-total+ele

(d) lst[3][3]=12

65. Examine the following lines of Python code:

lst1 = [1, 2, 3, 4]

lst2 = [1, 2, 3, 4]

lst1 == lst2

What will be the output?
Answer: print the value True as each element in a lst is eqaul to lst2



65. Write a Python program that prompts the user for a list of integers, stores in another list

only those values between 1–100, and displays the resulting list.

Answer:int_lst=[] max_length= int(input("enter the length of the list: "))

while len(int_lst>maxlenght:

        item=int(input(“append an intger to the list”))

        if item in range(1,101):

                 int_lst.append(item)

        else :

                 print(“not in range 1-100”)

                 break print(int_lst)

66. Write a Python program that prompts the user for a list of integers, stores in another list

only those values that are in tuple valid_values, and displays the resulting list.

Answer:

int_lst=[]

valid_values = [12, 30, 51, 12, 199]

max_length= int(input("enter the length of the list: "))

while len(int_lst>maxlenght:

        item=int(input(“append an intger to the list”))

        if item in valid_values:

                 int_lst.append(item)

        else :

                 print(“not in valid_values”)

                 break print(int_lst)

68. Write a Python program that prompts the user to enter types of fruit, and how many

pounds of fruit there are for each type. The program should then display the information in
the form fruit , weight listed in al- phabetical order, one fruit type per line as shown below,

Apple, 6 lbs. Banana, 11 lbs.etc.

Hint:fruits = ['banana', 'apple', 'orange', 'pear', 'grape'] print 'You have...' for f in fruits: if f ==

'tomato': print 'A tomato is not a fruit!' # (It actually is.) break print 'A', f else: print 'A fine

selection of fruits!'

69. Write a Python program that prompts the user to enter integer values for each of two

lists. It then should displays whether the lists are of the same length, whether the elements

in each list sum to the same value,and whether there are any values that occur in both lists.

Answer:

# Python program to check

# if two lists have at-least

# one element common

# using traversal of list

result = False

# traverse in the 1st list

for x in list1:

# traverse in the 2nd list

for y in list2:

# if one common if x == y: result = True return result return result # driver code a = [1, 2, 3,

4, 5] b = [5, 6, 7, 8, 9] print(common_data(a, b)) a = [1, 2, 3, 4, 5] b = [6, 7, 8, 9]

print(common_data(a, b))

73.Write a program to count the number of times a vowels appears in a given string and

store it in dictionary.

Answer: steps-Use str.count() to count vowels in a string

1. a_string = "Abcde"

2. lowercase = a_string. lower() Convert to lowercase.

3. vowel_counts = {}

4. for vowel in "aeiou":
5. count= lowercase.count(vowel)Count vowels.

6. vowel_counts[vowel] =count. Add to dictionary

7. print(vowel_counts)


