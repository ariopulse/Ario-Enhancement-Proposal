# ACEP-Python
Ario coding style for Python programming is fully compatible with [<u>PEP8</u>](https://www.python.org/dev/peps/pep-0008/).

Here is ACEP-Python 1:

<h2 style="color:rgba(50,84,108,255)">Naming</h2>

- For functions name use lower_snake_case
- For variables name use lower_snake_case
- For classes name use CamelCase 
- For class methods name use lower_snake_case
- For constants name use UPPER_SNAKE_NAME
- For your modules name use lower_snake_case
- For your packages name use lowercase

Note that if you use a name that originally has uppercase letter, use original form.

Name of variables, functions, classes and ... should be meaningful and understandable related to the function of that module.

Don't be afraid of names length and don't use abbreviations unless necessary.

```python
# Acceptable naming:
    first_name = 'Cyrus'
    new_IP_address = '192.168.1.1'
    average_of_student_scores = 15.53
	
    def print_some_text(text):
        print(text)

    class StudentsInfo(object):
        def best_score(self):
            best_score = 100
            return best_score
	
    BUFFER_SIZE = 255
	
    # mypackage
	
    # my_module
```

<h2 style="color:rgba(50,84,108,255)">White Space</h2>

It's recommended to use white spaces around operands and operators
Don't add any white space in blank new lines
briefly, white spaces are just to improve your code readability, but don't exaggerate!

Use a single space after commas (e.g., `a, b, c`).

Don't use spaces around the `=` operator when assigning default values to function arguments (e.g., `def foo(arg=42)`).

Use a single space after `#` to start a comment on the same line.

```python
# Acceptable using of whitespace:
    var = 10
    var = 2+8
    formula = (x+y) * (x**5)
    name = 'Sorena'

    score_list = [10, 20, 12]
    slice_list = old_list[1:]

    new_set = (x, y)

    if x>5:
        pass
    if x>5 and z<20:
        pass

    for i in range(0, 10):
        pass

    while c==2 or c>25:
        pass

# Unacceptable using of whitespace:
    var=10
    var = 2 + 8
    formula = (x + y) * (x ** 5)

    score_list = [10 , 20, 12]
    score_list = [ 10,20,12 ]
    slice_list = old_list[ 1: ]
    slice_list = old_list[1 : ]

    new_set = (x,y)
    new_set = ( x,y )
    new_set = ( x , y )
    if x > 5:
        pass
    if x>5and z<20:
        pass

    for i in range(0,10):
        pass

    while c == 2 or c > 25:
        pass
```

<h2 style="color:rgba(50,84,108,255)">New Line</h2>

- End of a Python code should have one new line
- Between imports and functions and classes should have two new lines
- Between imports and raw codes should have one or two new lines
- Between classes should have two new lines
- Between each method or each function in a class should have one new line
- Between classes or functions and main body should have two new lines
- Between each functions should have two new lines
- In the body of methods and functions or in the main body one new line should be used to separate block of related codes
- Between init docstring and should have one new line(if code starts with imports or raw codes) or two new lines(if code starts with functions or classes)   

```python
# Acceptable Newline:
    import sys
    import re
    # newline between imports and other codes
    class ClassOne(object):
        def simple_function(self):
            num_of_vars = 4
            sum_of_vars = (a+b+c+d)
            average = sum_of_vars/num_of_vars
            # new line to separate related blocks of code
            return average
        # newline between functions or methods	
        def print_some_text(self):
            print('hello world!')
    # newline between classes
    # newline between classes
    class ClassTwo(object):
        def __init(self, name, enter_time):
            self.name = name
            self.enter_time = enter_time
        # newline between functions or methods	
        def just_pass(self):
            pass
        # newline between functions or methods
        def say_greeting(self):
            greeting = 'hi' + self.namename
            greeting = greeting + 'How are you?'
            # newline to separate related blocks of code
            enter_time_message = 'youe enterd at' + str(self.enter_time)
            enter_time_message - enter_time + 'So, you\'re on time'
            # newline to separate related blocks of code
            final_message = greeting + enter_time_message
            return final_message
    # newline between started functions or classes and main body
    # newline between started functions or classes and main body
    student = ClassOne()
    studen.print_some_text()
    print('class 1 is tested')
    # newline to separate related blocks of code
    person = ClassTow('Kassandra', 9)
    print(person.say_greeting())
    print('class 2 is tested')
    # newline for end of the code		
```

<h2 style="color:rgba(50,84,108,255)">Importing</h2>

- Import each different module in separate lines
- Import from a module in one line
- Don't use *(importing everything from a module) unless necessary  
- If you want to assign a name to a module, you should use meaningful and understandable names related to the function of that module.

```python
# Acceptable importing:
	import sys
	import re
	from PyQt5 import QtCore, QtWidgets
	import fibo as fibonacci
	
# Unacceptable importing
	import sys, re
	from PyQt5 import QtCore
	from PyQt5 import QtEidgets
	from kivy import *
	import fibo as fb
```

<h2 style="color:rgba(50,84,108,255)">Indentation & Line Length </h2>

- Use 4 spaces for indentation, instead of using a tab (you can set your IDE tab to 4 spaces)

  

- The length of each <u>code</u> line should not exceed <u>79</u> characters. 
- The length of each <u>comment</u> line should not exceed <u>72</u> characters.
- Increasing the line length should follow the following examples

```python
# Acceptable indentation:
	if x>5:
		print('x is grater than 5')
	
# Unacceptable indentation
	if x>5:
		    print('x is grater than 5')
	
# Acceptable line length: 
	#vuse 4 space for indentation
	total = (num_one
			 + num_two
			 - num_three)

	long_string = ''' this is a very long
					  string and should
					  write in multilines'''
    
    long_list = [
    	1, 2, 3
    	4, 4, 6
    	]
	
# Unacceptable line length
	total = (num_one +
			 num_two -
			 num_three)
	long_string = 'this is a very long string and should write in multilines'
```

<h2 style="color:rgba(50,84,108,255)">Comments & DocStrings </h2>

- Comments are used to increase the understandability of the code and they generally explain why a statement has been used in the program.

  

- Docstrings are used to declare what does a python code or classes or methods or functions do
- Every Python <u>3</u> code should start with utf-8 coding style and a docstring with following format:
```python
# -*- coding: utf-8 -*-
"""
NAME: Code Name

VERSION: xx.xx.xx

PURPOSE: The Main Propose of This Code (say it in just one line)

DESCRIPTION: A complete description  of what does this code do

AUTHOR: Name of the author with <author@email.com>

DATE: Date of start this code (dd-month name(in short)-yyyy)

REQUIREMENT: Python version of this code
             lib1
             lib2

LICENSE: What kind of license does this code use?

desired URL(any URLs you want to be seen)
"""
```
- Every class should have a docstring with following format:
```python
"""
What does this class for?

...

Attributes
----------
attr1: (type)
    what is attr1 ?
attr2: (type)
    what is attr2 ?	
.
.
.
Methods
-------
methode1
    short description
methode2
    short description
.
.
.
"""
```
- Every method(<u>init method of classes does not need docstring</u>), and function should have a docstring with following format:
```python
"""What does this function or method do?
    Parameters
    ----------
    arg1: (type)(necessary or optional)
        what is arg1?
    arg2: (type)(necessary or optional)
        what is arg2?
    .
    .
    .
    Raises
    ------
    Raise(or Error) 1 Name:
        In which situation raise 1 happens?
    Raise(or Error) 2 Name:
        In which situation raise 2 happens?
    .
    .
    .
    Returns
    -------
    (type) what dose this function return and how?

# Use block of comments if you need to describe more 
# for example about the function algorithm
"""
```
- Use "(double quote) for docstrings

- docstring begins with a capital letter and ends with a period

- You can access docstrings in output terminal with __doc__ or __help__ method

  

- Try to write in “Strunk & White” English
- Between # and the first letter should have a single whitespace
- Comments should start with Capital letter
- In multiline comments, each line started with __#__
- In multiline comments, each paragraph should be separated by a newline with  __#__
- Use comments smartly to improve your code readability don't use tons of comments everywhere
- you can reduce comments by smart naming the variables

```python
# Acceptable starting docstring:
    """
    NAME: Advance Price Scraper
    
    VERSION: 1.0.0
    
    PURPOSE: Scrape Car Online Shops to Extract Car Price
    
    DESCRIPTION: This code use web scraping technique to extract car 
    			 online shops data and can guess a car price
    			 from other websites data
	
	AUTHOR: Saeed Hosseini <saeed144.73@gmail.com>
	
	DATE: 26-Apr-2021
	
	REQUIREMENT: Python 3.9.7
				 Beautiful Soup 4.9
				 Selenium 5.1.3
	
	LICENSE: MIT
	
	https://ariopulse.com
	https://github.com/S144S
    """
# Acceptable use of docstring:
	class Animal:
    """
    A class used to represent an Animal

    ...

    Attributes
    ----------
    says_str: (str)(necessary)
        a formatted string to print out what the animal says
    name: (str)(necessary)
        the name of the animal
    sound: (str)(necessary)
        the sound that the animal makes
    num_legs: (int)(optional)
        the number of legs the animal has (default 4)

    Methods
    -------
    says(sound=None)
        Prints the animals name and what sound it makes
    """

    says_str = "A {name} says {sound}"

    def __init__(self, name, sound, num_legs=4):
        self.name = name
        self.sound = sound
        self.num_legs = num_legs

    def says(self, sound=None):
        """Prints what the animals name is and what sound it makes.

        If the argument `sound` isn't passed in, the default Animal
        sound is used.

        Parameters
        ----------
        sound: (str)(optional)
            The sound the animal makes (default is None)

        Raises
        ------
        NotImplementedError
            If no sound is set for the animal or passed in as a
            parameter.
        
        Returns
        -------
        Nothing
        """
        if self.sound is None and sound is None:
            raise NotImplementedError("Silent Animals are not supported!")

        out_sound = self.sound if sound is None else sound
        print(self.says_str.format(name=self.name, sound=out_sound))

        
# Acceptable use of comments:
    
    # Calculate the solution to a quadratic equation using the quadratic
    # formula.
    #
    # There are always two solutions to a quadratic equation, x_1 and x_2.
    x_1 = (- b+(b**2-4*a*c)**(1/2)) / (2*a)
    x_2 = (- b-(b**2-4*a*c)**(1/2)) / (2*a)
	# Unacceptable indentation
	x = 'NiKola Tesla' # Scientist name
	# (better choice -> scientis_name = 'NiKola Tesla')
```

<h2 style="color:rgba(50,84,108,255)">Refrences </h2>

[1]	[PEP 8](https://www.python.org/dev/peps/pep-0008/)

[2]	[Barry's GNU Mailman style guide](http://barry.warsaw.us/software/STYLEGUIDE.txt)

[3]	[Wikipedia](http://www.wikipedia.com)

[4]	[Typeshed repo](https://github.com/python/typeshed)

