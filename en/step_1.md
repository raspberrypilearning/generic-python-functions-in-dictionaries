### Using functions in dictionaries

Dictionaries can be used to store all types of data, which can lead to some interesting uses.

You can store custom or inbuilt functions and methods within a dictionary. There are plenty of examples when this might be useful, put one particular example is when you might use a **CASE** statement in another programming language.

Have a look at this bit of code. It's an example of a menu system, where different functions are run depending on whether the user types in the values 1, 2 or 3.

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

This now has the possible user's input as the key, and the function to be called as the value. Now with an additional line, the user's choice can be prompted for and the appropriate function can be called.

~~~python
options[input('Choose 1, 2 or 3 ')]()
~~~

So the completed code now looks like this:

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
