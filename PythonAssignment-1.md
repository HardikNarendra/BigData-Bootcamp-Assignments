## Assignment Part-1
Q1. Why do we call Python as a general purpose and high-level programming language?<br>
Ans. Python is a general purpose language because it can used in any kind of domains such as for Application development (Frontend, Backend) , cyber security, data analytics, data science ,ML ,AI, IOT and much more. It is called as high-level programming language because writing code in python is very user friendly and human readable and it can be written easily in a English-like language.


Q2. Why is Python called a dynamically typed language?<br>
Ans. Python is called a dynamically typed language because in python we do not need to declare type of the variable at first, it is determined during the runtime by the interpretor.

Q3. List some pros and cons of Python programming language?<br>
Ans. Pros are:
     1) Easy to learn and read.
     1) Its Portabilty, same code can be used on any kind of machine.
     2) Its Versatility,
     3) It is free and Open Source and has more number of  users than any other language.
     4) It has large number of inbuilt libraries which can directly be used according to the tasks needed to be performed.<br>
     Cons are:
     1) Python is slow to use as it is dynamically typed and the code is read by interpretor line-by-line.
     2) Python is not good in making mobile application as it was earlier built for server-side programming so the client-side is rarely used.
     3) Python consumes a lot of memory space.
     4) Python can have runtime errors and is not easy to test.

Q4. In what all domains can we use Python?<br>
Ans. Python can be used in many domains such as Web Development, Networking, ML,AI, Deep Learning,IOT automation,Graphic Designing,Big Data Analytics etc.

Q5. What are variable and how can we declare them?<br>
Ans. A variable is a name which refers or points to an object . Object is assigned to a variable and we can access that object by using variable name
     we can decalre by typing.
     ```var=100  ```

Q6. How can we take an input from the user in Python?<br>
Ans. by using input() fuction
     ex: a=input("Enter the value of a:")

Q7. What is the default datatype of the value that has been taken as an input using input() function?<br>
Ans. String datatype.

Q8. What is type casting?<br>
Ans. type casting is explicity converting the datatype according to our need (higher bit value to lower bit value.).

Q9. Can we take more than one input from the user using single input() function? If yes, how? If no, why?<br>
Ans. Yes we can take more than one input using single input() function using using .split() function to split the values.<br>
     ex:
    ```x,y=input("enter two numbers:").split(',')```

Q10. What are keywords?<br>
Ans. Keywors are special words which are reserved in python to do that specific task which is designed for it, it cannot be used for any other purpose than that.

Q11. Can we use keywords as a variable? Support your answer with reason.<br>
Ans. No we cannot use keywords for variable name because they they are reserved buit-in to perform a specific task , it has its unique functinality.

Q12. What is indentation? What's the use of indentaion in Python?<br>
Ans. We use indentation instead of curly braces with we use in other languages such as c,c++ etc. It is a white space at the beginning of the code line and is used to   indicate a block of code.

Q13. How can we throw some output in Python?<br>
Ans. we can use print() function to throw output.

Q14. What are operators in Python?<br>
Ans. Operators are used to perform various kind of operations on values or certain variables. <br>
     Types of Operators in python are.
     1) Arithmetic operator.
     2) Logical Operator.
     3) Comparision Operator.
     4) Bitwise Operator.
     5) Assignment Operator. 
     6) Identity Operator.
     7) Membership Operator.

Q15. What is difference between / and // operators?<br>
Ans. '/' Indicates integer division for ex. 5/2 gives 2 as answer.
     '//' Indicates floor division for ex. 5/2 gives 2.5 as answer.

Q16. Write a code that gives following as an output.<br>
```
iNeuroniNeuroniNeuroniNeuron
```
Ans.
```    print("iNeuron"*4)```


Q17. Write a code to take a number as an input from the user and check if the number is odd or even.<br>
Ans.
```
   a=float(input("Enter a number:"))
    if a % 2 == 0:
        print('Even')
    else:
        print('Odd') 
```


Q18. What are boolean operator?<br>
Ans. Boolean operator are those which are used when we need to check if certain conditions are matched before proceding to the code.
     Boolean operators are: and, or, not.

Q19. What will the output of the following?<br>
```
1 or 0

0 and 0

True and False and True

1 or 0 or 0
```
Ans. 
```
    1 or 0 will give '1' as output

    0 and 0 will give '0' as output

    True and False and True will give 'False' as output

    1 or 0 or 0 will give '1' as output
```    

Q20. What are conditional statements in Python?<br>
Ans. Conditional statement are used to  control the flow of large programs in which certain conditions are required to be satisfied to execute certain code.

Q21. What is use of 'if', 'elif' and 'else' keywords?<br>
Ans. 'if' is used to check a condition in the code, if the 'if' condition is true then the code inside if block is executed , if the condition is false then              'elif'condition is checked,if elif condition is true then the code inside elif block is executed, if the 'elif' condition is false then at last the code           inside 'else' block is executed. 

Q22. Write a code to take the age of person as an input and if age >= 18 display "I can vote". If age is < 18 display "I can't vote".<br>
Ans.
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
Ans.
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
Ans.
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

Q25. Write a program to display only those numbers from a list that satisfy the following conditions

- The number must be divisible by five

- If the number is greater than 150, then skip it and move to the next number

- If the number is greater than 500, then stop the loop<br>
```
numbers = [12, 75, 150, 180, 145, 525, 50]
```
Ans.
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
