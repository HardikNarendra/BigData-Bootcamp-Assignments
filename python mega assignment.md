## Python mega Assignment

Q1. Why do we call Python as a general purpose and high-level programming language?<br>
Ans.<br>
```
 Python is a general purpose language because it can used in any kind of domains such as for Application development (Frontend, Backend) , cyber security, data analytics, data science ,ML ,AI, IOT and much more. It is called as high-level programming language because writing code in python is very user friendly and human readable and it can be written easily in a English-like language.
```

Q2. Why is Python called a dynamically typed language?<br>
Ans.<br>
```
 Python is called a dynamically typed language because in python we do not need to declare type of the variable at first, it is determined during the runtime by the interpretor.
```
Q3. List some pros and cons of Python programming language?<br>
Ans.<br>
```
     Pros are:
     1) Easy to learn and read.
     2) Its Portabilty, same code can be used on any kind of machine.
     3) Its Versatility,
     4) It is free and Open Source and has more number of  users than any other language.
     5) It has large number of inbuilt libraries which can directly be used according to the tasks needed to be performed.
     
     Cons are:
     1) Python is slow to use as it is dynamically typed and the code is read by interpretor line-by-line.
     2) Python is not good in making mobile application as it was earlier built for server-side programming so the client-side is rarely used.
     3) Python consumes a lot of memory space.
     4) Python can have runtime errors and is not easy to test.
```
Q4. In what all domains can we use Python?<br>
Ans.<br>
```
 Python can be used in many domains such as Web Development, Networking, ML,AI, Deep Learning,IOT automation,Graphic Designing,Big Data Analytics etc.
```

Q5. What are variable and how can we declare them?<br>
Ans.<br>
```
A variable is a name which refers or points to an object . Object is assigned to a variable and we can access that object by using variable name
we can decalre by typing.
var=100
```  
Q6. How can we take an input from the user in Python?<br>
Ans.<br> 
```
by using input() fuction
ex: a=input("Enter the value of a:")
```
Q7. What is the default datatype of the value that has been taken as an input using input() function?<br>
Ans.<br>
```
 String datatype.
```
Q8. What is type casting?<br>
Ans.<br>
```
 type casting is explicity converting the datatype according to our need (higher bit value to lower bit value.).
```
Q9. Can we take more than one input from the user using single input() function? If yes, how? If no, why?<br>
Ans.<br>
```
 Yes we can take more than one input using single input() function using using .split() function to split the values.
     ex:
    x,y=input("enter two numbers:").split(',')
```

Q10. What are keywords?<br>
Ans.<br>
``` 
Keywords are special words which are reserved in python to do that specific task which is designed for it, it cannot be used for any other purpose than that.
```

Q11. Can we use keywords as a variable? Support your answer with reason.<br>
Ans.<br> 
```
No we cannot use keywords for variable name because they they are reserved buit-in to perform a specific task , it has its unique functinality.
```

Q12. What is indentation? What's the use of indentaion in Python?<br>
Ans.<br>
```
We use indentation instead of curly braces with we use in other languages such as c,c++ etc. It is a white space at the beginning of the code line and is used to   indicate a block of code.
```

Q13. How can we throw some output in Python?<br>
Ans.<br>
``` 
we can use print() function to throw output.
```

Q14. What are operators in Python?<br>
Ans.<br>
```
 Operators are used to perform various kind of operations on values or certain variables. 
     Types of Operators in python are.
     1) Arithmetic operator.
     2) Logical Operator.
     3) Comparision Operator.
     4) Bitwise Operator.
     5) Assignment Operator. 
     6) Identity Operator.
     7) Membership Operator.
```
Q15. What is difference between / and // operators?<br>
Ans.<br>
```
 '/' Indicates integer division for ex. 5/2 gives 2 as answer.
     '//' Indicates floor division for ex. 5/2 gives 2.5 as answer.
```

Q16. Write a code that gives following as an output.<br>
```
iNeuroniNeuroniNeuroniNeuron 
```
Ans.<br>
```
    print("iNeuron"*4)
```

Q17. Write a code to take a number as an input from the user and check if the number is odd or even.<br>
Ans.<br>
```
    a=float(input("Enter a number:"))
    if a % 2 == 0:
        print('Even')
    else:
        print('Odd')
```
Q18. What are boolean operator?<br>
Ans.<br>
```
     Boolean operator are those which are used when we need to check if certain conditions are matched before proceding to the code.
     Boolean operators are: and, or, not.
```
Q19. What will the output of the following?<br>
```
1 or 0

0 and 0

True and False and True

1 or 0 or 0
```
Ans.<br>
```   
    1 or 0 will give '1' as output

    0 and 0 will give '0' as output

    True and False and True will give 'False' as output

    1 or 0 or 0 will give '1' as output
 ```   


Q20. What are conditional statements in Python?<br>
Ans.<br>
```
 Conditional statement are used to  control the flow of large programs in which certain conditions are required to be satisfied to execute certain code.
```

Q21. What is use of 'if', 'elif' and 'else' keywords?<br>
Ans.<br>
```
    'if' is used to check a condition in the code, if the 'if' condition is true then the code inside if block is executed , if the condition is false then 'elif'   
     condition is checked,if elif condition is true then the code inside elif block is executed, if the 'elif' condition is false then at last the code inside 'else'
     block is executed. 
```

Q22. Write a code to take the age of person as an input and if age >= 18 display "I can vote". If age is < 18 display "I can't vote".<br>
Ans.<br>
```
    age=int(input('Enter your age:'))
    if age >= 18:
        print('I can vote')
    else:
        print('I can't vote')
```

Q23. Write a code that displays the sum of all the even numbers from the given list.<br>
```
numbers = [12, 75, 150, 180, 145, 525, 50]
```
Ans.<br>
```
    numbers = [12, 75, 150, 180, 145, 525, 50]
    sum=0
    for i in numbers:
        if i % 2 == 0:
            sum = sum + i
        else:
            continue
    print(sum)
```
Q24. Write a code to take 3 numbers as an input from the user and display the greatest no as output.<br>
Ans.<br>
```
    a,b,c=input("Enter three numbers seperated by a comma").split(',')
    a=int(a)
    b=int(b)
    c=int(c)
    if a > b and a > c:
        print(f'{a} is greatest')
    elif b > c:
        print(f'{b} is greatest')
    else:
        print(f'{c} is greatest')
```
Q25. Write a program to display only those numbers from a list that satisfy the following conditions<br>

- The number must be divisible by five

- If the number is greater than 150, then skip it and move to the next number

- If the number is greater than 500, then stop the loop
```
numbers = [12, 75, 150, 180, 145, 525, 50]
```
Ans.<br>
```
    numbers = [12, 75, 150, 180, 145, 525, 50]
    for i in numbers:
        if i % 5 == 0:
            if i <= 150:
                print(i)
            elif i > 500:
                break 
            else:
                continue
```

Q26. What is a string? How can we declare string in Python?<br>
Ans. String is a datatype in python which stores the value of a variable in string/text format. We can declare them by using single quotation mark or double quotation
     marks. 
     ``` ex:
         first_name='Hardik'
         middle_name="Narendra'
     ```

Q27. How can we access the string using its index?<br>
Ans. we can use sqaure brackets to access string using its index.
```
    ex:
    first_name='Hardik'
    print(first_name[0])
```

Q28. Write a code to get the desired output of the following<br>
```
string = "Big Data iNeuron"
desired_output = "iNeuron"
```
Ans.
```
print(string[9:])
```

Q29. Write a code to get the desired output of the following<br>
```
string = "Big Data iNeuron"
desired_output = "norueNi"
```
Ans.
```
string = "Big Data iNeuron"
print(string[15:8:-1])
```
Q30. Resverse the string given in the above question.<br>
Ans.
```
print(string[::-1])
```

Q31. How can you delete entire string at once?<br>
Ans. using del keyword
```
del(string)
```

Q32. What is escape sequence?<br>
Ans.<br>
```
An escape sequence is a sequence of characters that, when used inside a character or string, does not represent itself but is converted into another character or series of characters that may be difficult or impossible to express directly, like newline (\n), tab (\t), and so on.
```
Q33. How can you print the below string?<br>
```
'iNeuron's Big Data Course'
```
Ans.
```
print("\'iNeuron's Big Data Course\'")
```

Q34. What is a list in Python?<br>
Ans.<br>
```
 List is used to store sequential elements of different datatypes in python. It is a collection of elements enclosed in square brackets"[]" and sperated by comma.
```
Q35. How can you create a list in Python?<br>
Ans. To create empty list<br>
```
a=[]
print(type(a))
```
To create list with data
```
a=[1,2,3,4]
print(a)
```

Q36. How can we access the elements in a list?<br>
Ans. we can access elements in list by using indexing.
```
list1=[1,2,3,4,5]
print(list1[1])
```

Q37. Write a code to access the word "iNeuron" from the given list.<br>
```
lst = [1,2,3,"Hi",[45,54, "iNeuron"], "Big Data"]
``` 
Ans.
```
lst = [1,2,3,"Hi",[45,54, "iNeuron"], "Big Data"]
print(lst[4][2])
```

Q38. Take a list as an input from the user and find the length of the list.<br>
Ans.
```
list1 = input("Enter number of elements seprated by comma: ").split(",")
print(len(list1))
```

Q39. Add the word "Big" in the 3rd index of the given list.<br>
```
lst = ["Welcome", "to", "Data", "course"]
```
Ans.
```
lst = ["Welcome", "to", "Data", "course"]
lst.insert(2,"Big")
print(lst)
```

Q40. What is a tuple? How is it different from list?<br>
Ans. tuple also stores sequential data of different types same as list. The main difference between list and tuple is , tuple are immutable i.e we cannot change value of a tuple  element while list are mutable.

Q41. How can you create a tuple in Python?<br>
Ans. by using () brackets.

Q42. Create a tuple and try to add your name in the tuple. Are you able to do it? Support your answer with reason.<br>
Ans. no we cannot add element in the already created tuple as tuples are immutable. if we want to change the element value we need to create a new tuple using only the changed elements from the original tuple.
```
s=(2,5,8)
s_append = s + (8, 16, 67)
print(s_append)
print(s)
```

Q43. Can two tuple be appended. If yes, write a code for it. If not, why?<br>
Ans. yes we can append two tuples.
```
t1=(1,5,8)
t2=(5,9,10)
t3=t1+t2
print(t3)
print(type(t3))
```

Q44. Take a tuple as an input and print the count of elements in it.<br>
Ans.
```
x=input("Enter the input elements seperated by comma").split(',')
t1=tuple(x)
print(len(t1))
```
Q45. What are sets in Python?<br>
Ans. Set is a unordered collection of elements which are mutable and has no duplicate values in it.

Q46. How can you create a set?<br>
Ans. we can create a set using set() function or we can use curly braces with data in it a= {1,2,3}, if {} is empty it will create empty dictionary.

Q47. Create a set and add "iNeuron" in your set.<br>
Ans.
```
a={'iNeuron'}
print(a)
print(type(a))
```

Q48. Try to add multiple values using add() function.<br>
Ans.
```
a={'iNeuron'}
a.add('is')
a.add('great')
print(a)
```

Q49. How is update() different from add()?<br>
Ans.  we can use add() to add single element into set while we can use update() to insert multiple elements into set.

Q50. What is clear() in sets?<br>
Ans. clear() function is used to clear all elements from a set.

Q51. What is frozen set?<br>
Ans. Frozen sets are set which are immutable, once created elements cannot be modified from a frozen set.

Q52. How is frozen set different from set?<br>
Ans.
1) Sets are mutable while frozen sets are immutable.
2) Sets are not hashable since they are mutable and not in order while frozen sets are hashable as they immutable elements are fixed and we can't add or remove elements.
3) Sets can’t be used as a dictionary key or as elements of another set,they can be used as a dictionary value whereas Frozensets are hashable, you can use the elements as a dictionary key or as an element from another set.

Q53. What is union() in sets? Explain via code.<br>
Ans. union returns all items from the original set and all items from the specified set.
```
set1={1,2,3,4,5}
set2={4,5,6,7}
print(set1 | set2)
```

Q54. What is intersection() in sets? Explain via code.<br>
Ans. intersection returns the similar elements between two sets.
```
set1={1,2,3,4,5}
set2={4,5,6,7}
print(set1 & set2)
```

Q55. What is dictionary in Python?<br>
Ans. Dictionary is a datastructure in python which is mutable and allows to store key-value pair.

Q56. How is dictionary different from all other data structures.<br>
Ans. Dictionary can be used in a variety of operations as it  consists of wide variety of methods and operations which other data structure does'nt have.The keys are always unique in a dictionary while the values may be same.

Q57. How can we delare a dictionary in Python?<br>
Ans. we can either declare it using the dict() function or we can type empty curly braces for creating empty dictionary.
```
a=dict()
b={}
c={'a':1,'b':2}
```

Q58. What will the output of the following?<br>
```
var = {}
print(type(var))
```
Ans. Output will be <class 'dict'>

Q59. How can we add an element in a dictionary?<br>
Ans. We can add elements by directly writing dict1['key_name']=value
```
dict1={}
dict1['name']='hardik'
dict1['age']=24
dict1['skills']=['hadoop','python','Sql']
dict1['address']={'country':'india','state':'daman','pincode':396210}
```

Q60. Create a dictionary and access all the values in that dictionary.<br>
Ans.
```
dict1={}
dict1['name']='hardik'
dict1['age']=24
dict1['skills']=['hadoop','python','Sql']
print(dict1.values())

```

Q61. Create a nested dictionary and access all the element in the inner dictionary.<br>
Ans.
```
dict1={}
dict1['name']='hardik'
dict1['address']={'country':'india','state':'daman','pincode':396210}
print(dict1['address']['country'])
print(dict1['address']['pincode'])

```

Q62. What is the use of get() function?<br>
Ans. get() function is used to access the elements from the dictionary
```
dict1={}
dict1['name']='hardik'
print(dict1.get('name'))
```

Q63. What is the use of items() function?<br>
Ans. It returns a list of all key-value pairs of dictionary.
```
dict1={}
dict1['name']='hardik'
dict1['age']=24
dict1['skills']=['hadoop','python','Sql']
dict1['address']={'country':'india','state':'daman','pincode':396210}
print(dict1.items())

```

Q64. What is the use of pop() function?<br>
Ans. it is used to remove desired key-value pair from the dictionary.
```
dict1={}
dict1['name']='hardik'
dict1['age']=24
dict1['skills']=['hadoop','python','Sql']
print(dict1.pop('name'))
```

Q65. What is the use of popitems() function?<br>
Ans. this function is used to remove the last inserted key-value pair from the dictionary and returns that value in the form of tuple.
```
dict1={}
dict1['name']='hardik'
dict1['age']=24
dict1['skills']=['hadoop','python','Sql']
print(dict1.popitem())
```

Q66. What is the use of keys() function?<br>
Ans. this function is used to get all the keys from the dictionary.
```
dict1={}
dict1['name']='hardik'
dict1['age']=24
dict1['skills']=['hadoop','python','Sql']
print(dict1.keys())
```

Q67. What is the use of values() function?<br>
Ans. this function is used to get all the values from the dictionary.
```
dict1={}
dict1['name']='hardik'
dict1['age']=24
dict1['skills']=['hadoop','python','Sql']
print(dict1.values())
```
Q68. What are loops in Python?<br>
Ans. Loops are used to iterate over a block of statement multiple time as required.

Q69. How many type of loop are there in Python?<br>
Ans. There are 2 types of loop i.e for loop and while loop.

Q70. What is the difference between for and while loops?<br>
Ans. For loop is used when we know how many times the loop is needed to be iterated, while loop is used when we don't know the exact number of iterations, we just need to run untill a condition is satisfied.

Q71. What is the use of continue statement?<br>
Ans. continue statement skips the execution of the current program block and forces the control to start the next iteration.

Q72. What is the use of break statement?<br>
Ans. break statement is used to bring the control out of the loop when certain external condition is satisfied

Q73. What is the use of pass statement?<br>
Ans. pass statement is null statement. it is used as a placeholder where in the program empty code is not allowed ,pass statement is used there.

Q74. What is the use of range() function?<br>
Ans. this function is used to get a sequence of numbers in a given range or to iterate loop over a sequence of numbers.

Q75. How can you loop over a dictionary?<br>
Ans.
```
dict1={}
dict1['name']='hardik'
dict1['age']=24
dict1['skills']=['hadoop','python','Sql']

for k,v in dict1.items():
    print("Key: ",k+"   " "Value: ",v)

```


### Coding problems
Q76. Write a Python program to find the factorial of a given number.<br>
Ans.
```
#factorial
def fact(n):
    if n<0:
        print("Factorial of negative number does'nt exist")
    elif n==1 or n==0:
        return 1
    else:
        return n*fact(n-1)
print(fact(5))
```


Q77. Write a Python program to calculate the simple interest. Formula to calculate simple interest is SI = (P*R*T)/100<br>
Ans.
```
#simple interest
def si(p,r,t):
    return (p*r*t)/100
print("Simple interest is:",si(10,8,2))
```

Q78. Write a Python program to calculate the compound interest. Formula of compound interest is A = P(1+ R/100)^t.<br>
Ans.
```

def ci(p,r,t):
    return p*(1+ r/100)**t
print("Compound interest is: ",ci(10,8,2))
```
Q79. Write a Python program to check if a number is prime or not.<br>
Ans.
```
from math import sqrt
n = 1
prime_flag = 0

if(n > 1):
	for i in range(2, int(sqrt(n)) + 1):
		if (n % i == 0):
			prime_flag = 1
			break
	if (prime_flag == 0):
		print("True")
	else:
		print("False")
else:
	print("False")

```
Q80. Write a Python program to check Armstrong Number.<br>
Ans.
```
#armstrong numnber
def armstrong(n):
    temp=n
    tot_dig=len(str(n))
    sum=0
    while n!=0:
        num = n % 10
        sum = sum + (num**tot_dig)
        n=n//10
    if sum == temp:
        print(f"{temp} is a armstrong number")
    else:
        print(f"{temp} is not a armstrong number ")
a=int(input("Please enter a number: "))
armstrong(a)
```

Q81. Write a Python program to find the n-th Fibonacci Number.<br>
Ans.
```
# nth fibonnaci number
def fibo(n):
    if n <= 1:
        return n
    else:
        return fibo(n-1)+fibo(n-2)
n=5
print(fibo(5))
```

Q82. Write a Python program to interchange the first and last element in a list.<br>
Ans.
```
#program to interchange first and last element in a list
list1 = [1,5,3,8,2,4,6,2,1,4,4]
list1[0] , list1[-1] =  list1[-1], list1[0]
print(list1)
```
output:
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/solution_code.py"
[4, 5, 3, 8, 2, 4, 6, 2, 1, 4, 1]
```
Q83. Write a Python program to swap two elements in a list.<br>
ans.
```
#program to swap two element in a list
list1 = [1,5,3,8,2,4,6,2,1,4,4]
list1[2] , list1[6] =  list1[6], list1[2]
print(list1)
```
output:
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/solution_code.py"
[1, 5, 6, 8, 2, 4, 3, 2, 1, 4, 4]
```

Q84. Write a Python program to find N largest element from a list.<br>
ans.
```
#find N largest element from a list
list1 = [1,5,3,8,2,4,6,2,1,10,12]
#nth largest 
n=3
set1=set(list1)
list1=list(set1)
print(list1[-n:])
```
Output:
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/solution_code.py"
[8, 10, 12]
```

Q85. Write a Python program to find cumulative sum of a list.<br>
Ans.
```
#cummulative sum
list1 = [10, 15, 20, 25, 30] 
c_sum=[]
c=0
for x in range(0,len(list1)):
    c = c + list1[x]
    c_sum.append(c)
print(c_sum)
```
Output:
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/solution_code.py"
[10, 25, 45, 70, 100]
```

Q86. Write a Python program to check if a string is palindrome or not.<br>
Ans.
```
#check if a string is palindrome or not
string1="harrah"
string2=string1[::-1]
if string1==string2:
    print("Its a palindrome")
else:
    print("Its not a palindrome")
```
Output:
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/solution_code.py"
Its a palindrom
```
Q87. Write a Python program to remove i'th element from a string.<br>
Ans.
```
#remove i'th element from a string
i=3
string="Hardik Narendra"
new_string=string.replace(string[i],"",1)
print(new_string)
```
Output:
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/solution_code.py"
Harik Narendra
```

Q88. Write a Python program to check if a substring is present in a given string.<br>
Ans.
```
#check if a substring is present in a given string
string1="Hardik Narendra Prajapati Narendra"
substring="Narendra"
if substring in string1:
    print(substring,"is a substring of string1")
else:
    print(substring,"is not a part of string1")
```
Output:
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/solution_code.py"
Narendra is a substring of string1
```
Q89. Write a Python program to find words which are greater than given length k.<br>
Ans.
```
#find words which are greater than given length k
string1="Hi how are you hardik , is everything fine"
k=3
words= string1.split()
for word in words:
    if len(word) > k:
        print(word)
```
Output:
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/solution_code.py"
hardik
everything
fine
```

Q90. Write a Python program to extract unquie dictionary values.<br>
Ans.
```
#extract unquie dictionary values
dict1={'name':'hardik','last_name':'prajapati','mid_name':'hardik'}
res=list(set(dict1.values()))
print(res)
```

Output:
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/solution_code.py"
['hardik', 'prajapati']
```

Q91. Write a Python program to merge two dictionary.<br>
Ans
```
#merge two dictionary
dict1 = {'a': 10, 'b': 8}
dict2 = {'d': 6, 'c': 4}
dict2.update(dict1)
print(dict2)
```
Output:
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/solution_code.py"
{'d': 6, 'c': 4, 'a': 10, 'b': 8}
```

Q92. Write a Python program to convert a list of tuples into dictionary.<br>
```
Input : [('Sachin', 10), ('MSD', 7), ('Kohli', 18), ('Rohit', 45)]
Output : {'Sachin': 10, 'MSD': 7, 'Kohli': 18, 'Rohit': 45}
```
Ans.
```
#convert a list of tuples into dictionary
Input = [('Sachin', 10), ('MSD', 7), ('Kohli', 18), ('Rohit', 45)]
print(dict(Input))
```
Output:
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/solution_code.py"
{'Sachin': 10, 'MSD': 7, 'Kohli': 18, 'Rohit': 45}
```

Q93. Write a Python program to create a list of tuples from given list having number and its cube in each tuple.<br>
```
Input: list = [9, 5, 6]
Output: [(9, 729), (5, 125), (6, 216)]
```
Ans.
```
#create a list of tuples from given list having number and its cube in each tuple
list1 = [9, 5, 6]
list2=[]
lambda_power = lambda x : x**3
for i in list1:
    t1=(i,lambda_power(i))
    list2.append(t1)
print(list2)
```
Output:
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/solution_code.py"
[(9, 729), (5, 125), (6, 216)]
```
Q94. Write a Python program to get all combinations of 2 tuples.<br>
```
Input : test_tuple1 = (7, 2), test_tuple2 = (7, 8)
Output : [(7, 7), (7, 8), (2, 7), (2, 8), (7, 7), (7, 2), (8, 7), (8, 2)]
```
Ans.
```
# get all combinations of 2 tuples
test_tuple1 = (7, 2)
test_tuple2 = (7, 8)
list1=[]
for i in range(len(test_tuple1)):
    for j in range(len(test_tuple2)):
        t1=(test_tuple1[i],test_tuple2[j])
        list1.append(t1)
for j in range(len(test_tuple2)):
    for i in range(len(test_tuple1)):
        t1=(test_tuple2[j],test_tuple1[i])
        list1.append(t1)        
print(list1)
```
Solution:
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/solution_code.py"
[(7, 7), (7, 8), (2, 7), (2, 8), (7, 7), (7, 2), (8, 7), (8, 2)]
```


Q95. Write a Python program to sort a list of tuples by second item.<br>
```
Input : [('for', 24), ('Geeks', 8), ('Geeks', 30)] 
Output : [('Geeks', 8), ('for', 24), ('Geeks', 30)]
```
Ans.
```
#sort a list of tuples by second item
Input = [('for', 24), ('Geeks', 8), ('Geeks', 30)] 
print(sorted(Input , key=lambda x : x[1]))
```
Output:
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/solution_code.py"
[('Geeks', 8), ('for', 24), ('Geeks', 30)]
```

Q96. Write a python program to print below pattern.<br>
```
* 
* * 
* * * 
* * * * 
* * * * * 
```
Ans.
```
#program to print below pattern.
for i in range(1,6):
    print("* "*i)
```
Output:
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/solution_code.py"
* 
* * 
* * *
* * * *
* * * * *
```
Q97. Write a python program to print below pattern.<br>
```
    *
   **
  ***
 ****
*****
```
Ans.
```
#print below pattern.
n=5
for i in range(1,n+1):
    print(" "*(n-i) + "*"*i)
    
```
Output:
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/solution_code.py"
     *
    **
   ***
  ****
 *****
```

Q98. Write a python program to print below pattern.<br>
```
    * 
   * * 
  * * * 
 * * * * 
* * * * * 
```
Ans.
```
rows = int(input("Enter number of rows: "))

k = 0

for i in range(1, rows+1):
    for space in range(1, (rows-i)+1):
        print(end="  ")
   
    while k!=(2*i-1):
        print("* ", end="")
        k += 1
   
    k = 0
    print()
```
Output:
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/solution_code.py"
Enter number of rows: 5
        * 
      * * *
    * * * * *
  * * * * * * *
* * * * * * * * *
```
Q99. Write a python program to print below pattern.<br>
```
1 
1 2 
1 2 3 
1 2 3 4 
1 2 3 4 5
```
Ans.
```
for i in range(5):
    for j in range(i+1):
        print(j+1,end=" ")
    print("\n")
```
Output:
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/solution_code.py"
1 
1 2
1 2 3
1 2 3 4
1 2 3 4 5
```

Q100. Write a python program to print below pattern.<br>
```
A 
B B 
C C C 
D D D D 
E E E E E 
```
Ans.
```
ascii=65
for i in range(1,6):
    for j in range(i):
        alphabet = chr(ascii)
        print(alphabet , end=" ")
    ascii += 1
    print("\n")
```
output:
```
PS C:\Users\Dell> & C:/Users/Dell/AppData/Local/Programs/Python/Python311/python.exe "c:/Users/Dell/OneDrive/Desktop/Ineuron Big Data Bootcamp/Python Assignment/solution_code.py"
A 
B B
C C C
D D D D
E E E E E

```