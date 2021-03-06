## Exam statistics

If you have done the *Battleship exercise*, this one will follow the same structure. We will go step by step, giving solutions in case you get stucked. At the end you can look to the solution file `Exam.py`.

####Ready? The computing starts here:

- This are the grades of some students:
```
grades = [100, 100, 90, 40, 80, 100, 85, 70, 90, 65, 90, 85, 50.5]
```
We are going to make a function to print them.
 + Define a function called `print_grades()` with one argument, a list called grades.
 + nside the function, iterate through grades and print each item on its own line.
 + After your function, call `print_grades()` with the grades list as the parameter.

**Solution 1**
````python
>>> grades = [100, 100, 90, 40, 80, 100, 85, 70, 90, 65, 90, 85, 50.5]
>>>
>>> def print_grades(grades):
...     for grade in grades:
...         print grade
...
...
>>> print_grades(grades)
100
100
90
40
80
100
85
70
90
65
90
85
50.5
>>>
```
- The next step in the creation of our grade statistics program involves computing the mean (average) of the grades.
 + Define a function `grades_sum()` that does the following.
 + Takes in a list of scores, scores
 + Computes the sum of the scores
 + Returns the computed sum
 + Call the newly created `grades_sum()` function with the list of grades and print the result.

**Solution 2**
```python
>>> grades = [100, 100, 90, 40, 80, 100, 85, 70, 90, 65, 90, 85, 50.5]
>>>
>>>
>>>
>>> def grades_sum (scores):
...     total = sum (scores)
...     return total
...
>>>
>>> print grades_sum(grades)
1045.5
>>>
>>>
```
Note:You can also use a for loop.


- Define a function `grades_average()`, below the grades_sum() function that does the following:

 + Has one argument, grades, a list
 + Calls `grades_sum` with grades
 + Computes the average of the grades by dividing that sum by float(len(grades)).
 + Returns the average.
 + Call the newly created `grades_average()` function with the list of grades and print the result.

**Solution 3**
```python
>>> def grades_average(grades):
...     tot =grades_sum(grades)
...     ave=tot/float(len(grades))
...     return ave
...
>>> print grades_average(grades)
80.4230769231
```
- We're going to use the average for computing the variance. The variance allows us to see how widespread the grades were from the average.
 + Define a new function called `grades_variance()` that accepts one argument, scores, a list.
 + First, create a variable average and store the result of calling `grades_average(scores)`.
 + Next, create another variable variance and set it to zero. We will use this as a rolling sum.
for each score in scores: Compute its squared difference: (average - score) ** 2 and add that to variance.
 + Divide the total variance by the number of scores.
 + Then, return that result.
 + Finally, after your function code, print `grades_variance(grades)`.

**Solution 4**
```python
>>> def grades_variance(scores):
...     average=grades_average(scores)
...     variance=0
...     for score in scores:
...         add=(average-score)**2
...         variance += add
...     var_tot=variance/len(scores)
...     return var_tot
...
>>> print grades_variance(grades)
334.071005917
```
- The standard deviation is the square root of the variance. You can calculate the square root by raising the number to the one-half power.

 + Define a function `grades_std_deviation(variance)`.
return the result of variance ** 0.5
 + After the function, create a new variable called variance and store the result of calling `grades_variance(grades)`.
 + Finally print the result of calling `grades_std_deviation(variance)`.

**Solution 5**
```python
>>> def grades_std_deviation(variance):
...     return variance**0.5
...
>>> variance=grades_variance(grades)
334.071005917
>>> print grades_std_deviation(variance)
18.2776094147
```


