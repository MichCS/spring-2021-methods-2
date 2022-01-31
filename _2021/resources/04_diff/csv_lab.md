## Problem 0
- We can open and read text files in python like so:
  ```
  f = open("file_name")
  s = f.read()
  ```
- Notice that the file name should be a string.
- In order to make opening the file easy, make sure the file is in the same directory as your python program file.
- It is a good idea to close a file when you're done with it, which you can do like so:
  - `f.close()`
- There is a file called **nyc_pop.csv** that you can find in the same place as these instructions. Download it and put it in the same directory as this file.
- Write code that will open **nyc_pop.csv** and the read its contents into a string.


## Problem 1
- You should notice that the file contains population data for the boroughs of NYC from 1790 - 2010. It is formatted such that each line represents one year, and contains a series of numbers separated by `,`. This is a common way of representing data in plain text, since it is easily accessible in programming.
- The file type is called **comma separated value** or **csv**.
- Often, the first line of a csv file will contain the headers that describe what each value represents.
- Write a function that will take a string representing the text of a file that looks similar to nyc_pop.csv and returns a list that contains only the headers.
  ```
  print( get_headers(text) )
  # Should print
  ['Year', 'Manhattan', 'Brooklyn', 'Queens', 'Bronx', 'Staten Island']
  ```

## Problem 2
- Write a function that will take a string representing the text of file that looks similar to nyc_pop.csv and returns a list of lists.
- Each sublist should represent a line from the file.
- Each element in a sublist should represent one value.
  ```
  print(get_data(text))
  # Should print:
  [['1790', '33131', '4549', '6159', '1781', '3827'], ['1800', '60515', '5740', '6642', '1755', '4563'], ...
  # There will be more sublists after that.
  ```

## Problem 3
- Write a function that will take a list of lists similar to one returned by your solution to problem 2, where every element is a string, and change each element in each sublist to a number.
- Note that this function modifies the parameter list, it does not return a new list.
- You can assume that the parameter only contains lists of number strings.
  ```
  number_convert(data)
  print(data)
  # Should print
  # [[1790.0, 33131.0, 4549.0, 6159.0, 1781.0, 3827.0 ], [1800.0, 60515.0, 5740.0, 6642.0, 1755.0, 4563.0], ...
  # There will be more sublists after that.
  ```

## Problem 4
- Write a function that takes a list similar to the one returned by the function in problem 3, and returns the total of the values in a given row.
  ```
  print( row_total(1790, pop_data) )
  # Should print 49447.0
  ```

## Problem 5
- Write a function that takes a list similar to the one returned by the function in problem 3, and returns a list containing the values in a given column.
  ```
  print(get_column('Bronx', pop_headers, pop_data))
  # Should print
  [1781.0, 1755.0, 2267.0, 2782.0, 3023.0, 5346.0, 8032.0, 23593.0, 37393.0, 51980.0, ...
  # With more data after that
  ```

## Problem 6
Use code, including the functions from problems 1-5 to answer the following questions. Your code should print out the answer.
- How many people lived in NYC in 2010?
- How many people lived in Brooklyn in 1970?
- What was the change in total population from 1900 to 2000?
- What percentage of the total NYC population did Queens account for in 2010?
- Come up with your own question that can be answered using the population data.