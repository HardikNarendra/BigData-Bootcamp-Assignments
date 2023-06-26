## Python OOP Assignment
Q1. What is the purpose of Python's OOP?<br>
Ans. Thepurpose of oops in python is to encapsulate or hide the working of data with the methods from the other parts of the code by using encapsulation,polymorphism and inheritance.<br>

Q2. Where does an inheritance search look for an attribute?<br>
Ans. it first looks in the instance object then it looks for the class from where that instance object was created from and then in all higher superclasses.<br>

Q3. How do you distinguish between a class object and an instance object?<br>
Ans. Class objects represent the class itself while instance object object represent individual intances of the class. Class objects have class level attributes and methods that are shared among all the instances of class while instance objects have their own set of attributes and methods that are independent of other.<br>

Q4. What makes the first argument in a class’s method function special?<br>
Ans. The first argument in a class method is self.It is special beacause it represents instance of a given class,if it was not there than the instance would not be able to have its own attributes and methods. Self actually holds the reference address or points to the objects created from a class.<br>

Q5. What is the purpose of the init method?<br>
Ans.init method is used for initialization of the object's attribute.<br>

Q6. What is the process for creating a class instance?<br>
Ans. The steps for creating a class instance are:-<br>
Step1) define a class by using the class keyword and add the attributes as required.<br>
step2)  call the class using class name and pass in whatever arguments its __init__ method accepts.<br>

Q7. What is the process for creating a class?<br>
Ans. we can simply type:<br>
```
class abc:
    def __init__(self,name):
        self.name=name
```

Q8. How would you define the superclasses of a class?<br>
Ans. we can define by typing<br>
```
class A:
    pass
class B(A):
    pass
class C(B):
    pass
x=C()
print(isinstance(x, A))
```

Q9. What is the relationship between classes and modules?<br>
Ans. Modules are collections of methods and constants. They cannot generate instances. Classes may generate instances (objects), and have per-instance state (instance variables).<br>

Modules may be mixed in to classes and other modules. The mixed in module’s constants and methods blend into that class’s own, augmenting the class’s functionality. Classes, however, cannot be mixed in to anything.<br>

A class may inherit from another class, but not from a module.<br>

A module may not inherit from anything.<br>

Q10. How do you make instances and classes?<br>
Ans.<br>
```
class Employee:
   'Common base class for all employees'
   empCount = 0

   def __init__(self, name, salary):
      self.name = name
      self.salary = salary
      Employee.empCount += 1
   
   def displayCount(self):
     print "Total Employee %d" % Employee.empCount

   def displayEmployee(self):
      print "Name : ", self.name,  ", Salary: ", self.salary

"first object of Employee class"
emp1 = Employee("Hardik", 2000)
"second object of Employee class"
emp2 = Employee("Narendra", 5000)
emp1.displayEmployee()
emp2.displayEmployee()
print "Total Employee %d" % Employee.empCount
```

Q11. Where and how should be class attributes created?<br>
Ans. Class attributes will be shared by all instances,they are defined in the class body parts usually at the top.<br>
```
class sampleclass:
    count = 0     # class attribute
  
    def increase(self):
        sampleclass.count += 1
  
```
Q12. Where and how are instance attributes created?<br>
Ans. instance attribute are defined inside a constructer using the self parameter.<br>
```
class Student:
    def __init__(self, name, age): 
        self.name = name
        self.age = age
```

Q13. What does the term "self" in a Python class mean?<br>
Ans. The self parameter is a reference to the current instance of the class, and is used to access variables that belongs to the class.<br>

Q14. How does a Python class handle operator overloading?<br>
Ans. To perform operator overloading, Python provides some special function or magic function that is automatically invoked when it is associated with that particular operator. For example, when we use + operator, the magic method __add__ is automatically invoked in which the operation for + operator is defined. <br>

Q15. When do you consider allowing operator overloading of your classes?<br>
Ans. When one or both operands are of a user-defined class or structure type, operator overloading makes it easier to specify user-defined implementation for such operations. This makes user-defined types more similar to the basic primitive data types in terms of behaviour.<br>

Q16. What is the most popular form of operator overloading?<br>
Ans.The most frequent instance is the adding up operator '+', where it can be used for the usual addition and also for combining two different strings.<br>

Q17. What are the two most important concepts to grasp in order to comprehend Python OOP code?<br>
Ans. Inheritance and Polymorphism.<br>

Q18. Describe three applications for exception processing.<br>
Ans.Exception handling allows for the program to anticipate and recover from errors, thus making the program more robust and resistant to unexpected conditions. By catching and handling exceptions, the program can continue to execute and provide a more stable user experience.<br>
-a try block that encloses the code section which might throw an exception,<br>
-one or more catch blocks that handle the exception and.<br>
-a finally block which gets executed after the try block was successfully executed or a thrown exception was handled.<br>

Q19. What happens if you don't do something extra to treat an exception?<br>
Ans. When an exception occurred, if you don't handle it, the program terminates abruptly and the code past the line that caused the exception will not get executed.<br>

Q20. What are your options for recovering from an exception in your script?<br>
Ans.Try and except statements are used to catch and handle exceptions in Python. Statements that can raise exceptions are kept inside the try clause and the statements that handle the exception are written inside except clause<br>

Q21. Describe two methods for triggering exceptions in your script.<br>
Ans. Try – This method catches the exceptions raised by the program. <br>
     Raise – Triggers an exception manually using custom exceptions.<br>

Q22. Identify two methods for specifying actions to be executed at termination time, regardless of  
whether or not an exception exists.<br>
Ans. Finally-Finally block always executes irrespective of an exception being thrown or not. The final keyword allows you to create a block of code that follows a       try-catch block<br>
    Raise-The raise statement specifies an argument which initializes the exception object. Here, a comma follows the exception name, and argument or tuple of the argument that follows the comma.<br>

Q23. What is the purpose of the try statement?<br>
Ans. Try method catches the exceptions raised by the program.<br>

Q24. What are the two most popular try statement variations?<br>
Ans. try/except/else and try/except/finally<br>

Q25. What is the purpose of the raise statement?<br>
Ans. The raise statement specifies an argument which initializes the exception object. Here, a comma follows the exception name, and argument or tuple of the argument that follows the comma.<br>

Q26. What does the assert statement do, and what other statement is it like?<br>
Ans.
-Assertions are statements that assert or state a fact confidently in your program. For example, while writing a division function, you're confident the divisor shouldn't be zero, you assert divisor is not equal to zero.<br>
-Assertions are simply boolean expressions that check if the conditions return true or not. If it is true, the program does nothing and moves to the next line of code. However, if it's false, the program stops and throws an error.<br>
-It is also a debugging tool as it halts the program as soon as an error occurs and displays it.<br>
```
def avg(marks):
    assert len(marks) != 0
    return sum(marks)/len(marks)

mark1 = []
print("Average of mark1:",avg(mark1))
```

Q27. What is the purpose of the with/as argument, and what other statement is it like?<br>
Ans.The with statement replaces a try-catch block with a concise shorthand. More importantly, it ensures closing resources right after processing them. A common example of using the with statement is reading or writing to a file.<br>

Q28. What are *args, **kwargs?<br>
Ans.  <br>
-The args stands for arguments that are passed to the function.<br>
```
def Person(*args):
    print(args)

Person('Sean', 'Male', 38, 'London', 9375821987)

```
- kwargs stands for keyword arguments which are passed along with the values into the function.<br>
```
# Print values of function Person along with its associated keywords
def Person(**kwargs):
    for key, value in kwargs.items():
        print("{} -> {}".format(key, value))    # OR print(f'{key} -> {value}')

Person(Name = 'Sean', Sex = 'Male', Age = 38, City = 'London', Mobile = 9375821987)

```

Q29. How can I pass optional or keyword parameters from one function to another?<br>
Ans.To pass optional or keyword parameters from one function to another, collect the arguments using the * and ** specifiers in the function’s parameter list,Through this, you will get the positional arguments as a tuple and the keyword arguments as a dictionary. Pass these arguments when calling another function by using * and ** <br>
```
def f(a, *args, **kwargs):
   ...
   kwargs['width'] = '14.3c'
   ...
   g(a, *args, **kwargs)
```
Q30. What are Lambda Functions?<br>
Ans. A lambda function is a small anonymous function. A lambda function can take any number of arguments, but can only have one expression.<br>
Syntax:<br>
```
lambda arguments : expression
```
The expression is executed and the result is returned.<br>

Q31. Explain Inheritance in Python with an example?<br>
Ans.  It is a mechanism that allows you to create a hierarchy of classes that share a set of properties and methods by deriving a class from another class. Inheritance is the capability of one class to derive or inherit the properties from another class. <br>
Example:<br>
```
class Person(object):

    # Constructor
    def __init__(self, name, id):
	self.name = name
	self.id = id

    # To check if this person is an employee
    def Display(self):
	print(self.name, self.id)

emp = Person("Hardik", 12) # An Object/instance of Person
emp.Display()

```

Q32. Suppose class C inherits from classes A and B as class C(A,B).Classes A and B both have their own versions of method func(). If we call func() from an object of 
class C, which version gets invoked?<br>
Ans. the function from class C will get invoked first.<br>

Q33. Which methods/functions do we use to determine the type of instance and inheritance?<br>
Ans. isinstance()<br>

Q34.Explain the use of the 'nonlocal' keyword in Python.<br>
Ans.The nonlocal keyword is used to work with variables inside nested functions, where the variable should not belong to the inner function.<br>
```
def myfunc1():
  x = "John"
  def myfunc2():
    nonlocal x
    x = "hello"
  myfunc2() 
  return x

print(myfunc1())
```
Q35. What is the global keyword?<br>
Ans.A global keyword is a keyword that allows a user to modify a variable outside the current scope. It is used to create global variables in Python from a non-global scope, i.e. inside a function. Global keyword is used inside a function only when we want to do assignments or when we want to change a variable.<br>
