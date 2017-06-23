### Using functions in dictionaries

Dictionaries can store all types of data, which makes them useful for many things.

You can store custom or inbuilt functions and methods within a dictionary. There are plenty of times when this comes in handy, for example when, in another programming language, you would use a **CASE** statement.

Have a look at the bit of code below. It's an example of a menu system, where different functions are run depending on whether the user types in the values 1, 2 or 3.

~~~python
def option1():
    print('You chose 1')

def option2():
    print('You chose 2')

def option3():
    print('You chose 3')

choice = input():

if choice == '1':
    option1()
elif choice == '2':
    option2()
elif choice == '3':
    option3()
~~~

Rather than chaining `if` and `elif` conditionals together, you can use a dictionary of functions. For instance:

~~~python
options = {'1': option1, '2': option2, '3': option3}
~~~

This now has the possible user inputs as the keys, and the functions to be called as the values. With an additional line, the user's choice can be prompted for and the appropriate function can be called.

~~~python
options[input('Choose 1, 2 or 3 ')]()
~~~

So the completed code looks like this:

~~~python
def option1():
    print('You chose 1')


def option2():
    print('You chose 2')


def option3():
    print('You chose 3')


options = {'1': option1, '2': option2, '3': option3}

options[input('Choose 1, 2 or 3 ')]()
~~~
