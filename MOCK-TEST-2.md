# MOCK-TEST-2

## 1) Write an SQL query to find the second-highest salary from an "Employees" table.
   5 points <br>
Ans.
```
#query to find second highest salary from employees table
SELECT * FROM (SELECT * FROM employees ORDER BY salary DESC LIMIT 2) 
AS emp ORDER BY salary LIMIT 1; 
```


## 2) Write a MapReduce program to calculate the word count of a given input text file.<br>
Ans.<br>
<br>
mapper.py<br>
```
# for reading and writing data
import sys
  
# reading entire line from STDIN (standard input)
for line in sys.stdin:
    # to remove leading and trailing whitespace
    line = line.strip()
    # split the line into words
    words = line.split()
      
    # looping over the words array and printing the word
    for word in words:
        # Reduce step, i.e. the input for reducer.py
        print('%s\t%s' % (word, 1))
```

reducer.py<br>
```
from operator import itemgetter
import sys
  
current_word = None
current_count = 0
word = None
  
# read the entire line from STDIN
for line in sys.stdin:
    # remove leading and trailing whitespace
    line = line.strip()
    # slpiting the data on the basis of tab we have provided in mapper.py
    word, count = line.split('\t', 1)
    # convert count (currently a string) to int
    try:
        count = int(count)
    except ValueError:
        # count was not a number, so silently
        # ignore/discard this line
        continue
  
    # this IF-switch only works because Hadoop sorts map output
    # by key (here: word) before it is passed to the reducer
    if current_word == word:
        current_count += count
    else:
        if current_word:
            # write result to STDOUT
            print('%s\t%s' % (current_word, current_count))
        current_count = count
        current_word = word

if current_word == word:
    print('%s\t%s' % (current_word, current_count))
```
Command to execute the code<br>
```
hadoop jar hadoop-streaming-2.4.0.jar -files mapper.py,reducer.py -mapper mapper.py -reducer reducer.py -input /test/demo.txt -output /output
```

## 3) Write a Spark program to count the number of occurrences of each word in a given text file.<br>
Ans.<br> 
Note for this program i have shared a seperate jupyter notebook link.
https://github.com/HardikNarendra/BigData-Bootcamp-Assignments/blob/main/MOCK-TEST-2-Spark-wordcount.ipynb





