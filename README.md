# Python Tutorial for Beginners

In this tutorial, we will introduce Python from a beginner's perspective. 

This tutorial will culminate in creating an ***expenses tracker app***.

## Setup

### Installing Python

#### Installing Python for Windows

- Open up PowerShell and type ```python3```. 
    - Microsoft Store should open up. 
- Install Python 3.12
- Close PowerShell and Re-open it
- Type ```python3 --version``` and you should get something like: ```Python 3.12.3```

#### Installing Python for Mac

- Open up Terminal
- Run ```/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"``` to install Homebrew
- Close and Re-open Terminal
- Type ```brew install python```
- Type ```python3 --version``` and you should get something like: ```Python 3.12.3```

### Installing VS Code

VS Code is the development environment where we will write all of our code.

It is extremely helpful!

You can find the link [here](https://code.visualstudio.com/download)

### Installing Git

Git is a version control system that we can use to save versions of our code.

Git is used regularly in the field.

Download and install Git by following the instructions [here](https://learn.microsoft.com/en-us/devops/develop/git/install-and-set-up-git)

Once installed, try typing ```git --version``` in either PowerShell (Windows) or Terminal (Mac). You should get a version showing up.

### Sign up for a GitHub

GitHub is essentially a platform that carries all of your code with the versions that you've written, taken from your local machine and stored in the cloud. It's a great platform for teams to work together.

You can sign up for a GitHub account [here](https://github.com/)

### Link GitHub to Git

In PowerShell (Windows) or Terminal (Mac), run the following commands:

- ```git config --global user.email "your email"```
- ```git config --global user.name "your name"```

Replace "your email" with the email you used to sign up for GitHub and replace "your name" with your name.

Run through the sign-in process and once complete, your GitHub should be linked to Git.

### Clone down the first repository

I have set up some files for you to begin your Python journey. In order to retrieve these files from my Github account, we need to use the ```clone``` command. 

- Open up PowerShell (Windows) or Terminal (Mac) and navigate to the Desktop.
    -  Example: When I first open up PowerShell, I find myself in ```C:\Users\marti>```. To get to my Desktop, I just type ```cd Desktop``` and hit Enter.
- While in the Desktop, type the command ```git clone https://github.com/codewithmarty/python-codealong.git```
- When the command is completed, type ```ls``` and you should see a folder called "python-tutorial-with-marty" appear in your Desktop.
- Open up VS Code, click on Open Folder and open this folder that you've now added to your Desktop.
- Click on the file called "follow_along.py" to follow along in these lessons.

***The Setup is now complete***

## Lesson 1: Primitive Data Types

What is a data type?

It is exactly what you think it is...a type of data that Python understands.

Python has a number of data types and we cannot cover ALL of them in this tutorial.

However, we will focus on the following ones:

- Strings
- Numbers (Integers / Floats)
- Booleans
- Lists
- Dictionaries

Strings, Numbers and Booleans are ***primitive*** data types. This is another fancy word for simple. 

Lists and Dictionaries are NOT ***primitive***. 

### Strings 

A string is basically text that is surrounded by quotes.

For example, ```"shoes"``` is considered a string in Python. So is ```"32"```. Even though 32 is a number, because it is surrounded in quotes, it is treated like a string (or text).

I can save a string to a variable so that my strings can be used later in my program.

Example:
- Type ```favorite_color = "blue"``` in the follow_along file.
    - This saves ```"blue"``` to a variable called ```favorite_color```. This means whenever you call ```favorite_color``` in your code, the value is ```"blue"```.
    - Try calling it using a ```print``` statement:
        - Type the code ```print(favorite_color)```.
        - Hit the "play button" in VS Code and you should see ```"blue"``` in your terminal.

### Numbers

Numbers can be described as integers or floats. An integer is a whole number, while a float (or floating point) is a fancy term for a decimal.

For example, ```35``` is an integer in Python and I can save it to a variable. Let's say my age is 35. I can then say ```age = 35``` and if I want to save my age and use it later in the program, I can call it by the variable name, ```age```. 

Run the code ```print(age)``` and you should see 35 appear in your terminal.

A neat task could be I want to increase my age by 5. I can do that by running ```age = age + 5```. I have taken the old ```age``` variable and reset it to itself + 5. 

Run ```print(age)``` again. Now, I'm 40!

On the other hand, ```168.5``` is clearly not an integer. This is called a floating point number (or float for short) because the decimal value is "floating" around in memory.

Type ```height = 168.5``` in the file. Now you've saved my height to a variable!

### Booleans

Booleans are data types that are true or false statements.

For example, ```True``` is true and ```False``` is false because they just are!

Type ```is_happy = True``` in the file. You've now created a variable called ```is_happy``` that is storing a true value. A coder can interpret that to mean I am indeed happy! However, if I said ```is_happy = False```, this means I am not happy.

Keep ```is_happy = True``` in your code and also type ```print(is_happy)``` one line below it. 

Run the code by hitting the play button. You should see ```True``` appear in the terminal.

You can also use Booleans with numbers. For example, we have a variable called ```age``` that is set to 40. If I wrote: ```print(age > 51)``` what would you expect the output to be? Would it be a true statement or a false statement?

I know my age is 40, so is 40 > 51 a true statement? No! It's false. When you run the code ```print(age > 51)``` you should expect to see a false statement.

#### Our variables so far:

The following should be a list of all of our variables so far.

```python 
favorite_color = "blue"
age = 35 
age = age + 5
height = 168.5
is_happy = True
```

Now, type the following code:

```print(f"My favorite color is {color}, my age is {age} and my answer to whether or not I am happy is {is_happy}")```

Run it using the play button. What do you see appear in the terminal?

You should see ```"My favorite color is blue, my age is 40 and my answer to whether or not I am happy is True"```.

When you use ```f""``` you are using something called a ***formatted string***. You can embed variable names inside the string using ```{}``` and you'll get a beautiful string in the end. 

Congrats! You just finished the first lesson.

### Exercise 1
``` 
Navigate to exercise1.py

Part 1. Create 4 variables that hold: 
1. a string
2. a number
3. a float
4. a boolean

Part 2. Print a sentence using these four variables and a formatted string. 

Run your code.
```

## Lesson 2: Built-in Data Types

In lesson 1, we talked about primitive or basic data types.

We covered:
- strings
- integers
- floats
- booleans

In this lesson, we talk about more complex data structures, namely:
- lists
- dictionaries

Lists and dictionaries can be considered "containers" because they are basically boxes that hold data.

### Lists

A list is square brackets with a bunch of stuff inside.

Example:
- ```favorite_colors = ["blue", "pink", "green"]``` is a list of all of my favorite colors. Notice how we also have commas that separate the colors.
- ```favorite_foods = ["pizza", "sandwich"]``` is a list of all of my favorite foods.

So far, the examples above are lists of strings, but I can have lists of numbers as well.

Example:
- ```ages = [34, 32, 67, 60, 67]``` is a list of ages for people in my family.

I can also mix and match the primitive data types. For example:
- ```michael = [21, "blue", True]``` is a list that describes Michael.

### Dictionaries

There is one small problem with lists.

Let's look at the example: ```michael = [21, "blue", True]```

If you were to come back to your code in a week, I bet you wouldn't be able to remember what information this ```michael``` list actually held.

The first element, ```21``` could mean how many years Michael has been married or ```"blue"``` could mean his friend's favorite color. 

Is there a better way to describe Michael in code?

What if we wrote:

```python 
person = {
    "name": "michael",
    "age": 21,
    "favorite_color": "blue",
    "is_happy": True
}
```
Would you be able to understand what the variable ```person``` was actually holding?

```person``` is called a dictionary because it has key-value pairs and defines all of the characteristics that make Michael, Michael.

#### Accessing Information From Dictionaries

I can extract Michael's name, age, favorite color and whether or not he is happy very quickly.

- Getting Michael's name: ```person["name"]```. This will output "michael".
- Getting Michael's age: ```person["age"]```. This will output 21.
- Getting Michael's favorite color: ```person["favorite_color"]```. This will output "blue".
- Getting Michael's happy state: ```person["is_happy"]```. This will output True.

I can make a print statement to access all of the information about Michael. Here's how my print statement might look:

```print(f"My name is {person["name"]} and my age is {person["age"]}. My favorite color is {person["favorite_color"]}. To answer if I am happy, I will say {person["is_happy"]}.")```

The output should read: ```My name is michael and my age is 21. My favorite color is blue. To answer if I am happy, I will say True```.

### Exercise 2
``` 
Navigate to exercise2.py

Part 1. 
Create a list of your favorite singers and save it to a variable called favorite_singers.

Part 2. 
Create a list of information that describes you. Include:
- hair color
- favorite song
- age
- name

Part 3.
Convert the list from Part 2 to a dictionary.

Part 4.
Print a formatted string from the information you wrote in Part 3.

Run your code.
```

## Lesson 3: Lists of Dictionaries and For Looping

### Lists of Dictionaries

In the last lesson, we described lists and dictionaries as two separate things. However, we can combine them.

Let's say we have two persons, ```person1``` and ```person2```. These two variables can be represented as dictionaries:

```python 
person1 = {
    "name": "selam",
    "age": 18,
    "favorite_color": "pink",
    "is_happy": True
}
 
person2 = {
    "name": "martin",
    "age": 59,
    "favorite_color": "green",
    "is_happy": False
}
```

However, they can also be combined into a single list:

```python

    people = [
        {
            "name": "selam",
            "age": 18,
            "favorite_color": "pink",
            "is_happy": True
        },
        {
            "name": "martin",
            "age": 59,
            "favorite_color": "green",
            "is_happy": False
        },
    ]

```

The above variable ```people``` is KIND OF how a ***database*** looks like when you retrieve the data.

Here's a question: If I accessed Michael's information using notation like ```person["name"]```, how would I access Martin's name?

Would I just do ```people["name"]```? That can't be right because people represents two people so what about Selam's name?

We will investigate this in the next section.

### For Looping

I can access elements in a list very easily using something called a ```for``` loop.

Create a variable called ```favorite_shows = ["Love is Blind", "Boy Meets World", "Seinfeld"]```

Try writing the following code below your favorite shows:

```python
for show in favorite_shows:
    print(show)
```

What happens? The ```show``` variable becomes EACH of your favorite shows in your ```favorite_shows``` list. This is called a for loop. It loops **for** as many shows as you have in your list. It won't go more, it won't go less.

I can get even fancier with my code. I can replace it with a formatted string:

```python
for show in favorite_shows:
    print(f"My favorite show is {show}.")
```

The output to this code should be:

```
My favorite show is Love is Blind.
My favorite show is Boy Meets World.
My favorite show is Seinfeld.
```

Coming back to the ```people``` variable, this is how I would loop over each person (Selam and Martin) and print their information:

```python
for person in persons:
    print(f"My name is {person["name"]} and my age is {person["age"]}. My favorite color is {person["favorite_color"]}. To answer if I am happy, I will say {person["is_happy"]}.")
```

The ```person``` variable inside the loop now represents EACH dictionary of martin and selam.

The output to this code should be:

```
My name is selam and my age is 18. My favorite color is pink. To answer if I am happy, I will say True.
My name is martin and my age is 59. My favorite color is green. To answer if I am happy, I will say False.
```

### Exercise 3
``` 
Navigate to exercise3.py

Part 1. 
Create a dictionary and assign it to a variable called expense1. The keys for the expense should be name, amount and date.

Part 2.
Create another dictionary and assign it to a variable called expense2. Again, have a name, amount and date.

Part 3.
Create a list called expenses and put expense1 and expense2 inside of the expenses list.

Part 4.
Loop over your expenses list and print out each expense. Each expense should look something like:
"My expense is buying milk. It cost me $20. I bought it on 08-24-2023"
```

## Lesson 4: Adding Elements to Lists

Guess what. Lists can grow in length. They can also shrink. Let's just focus on growing them in this lesson.

How do you grow lists? 

Let's go back to our people list:

```python

    people = [
        {
            "name": "selam",
            "age": 18,
            "favorite_color": "pink",
            "is_happy": True
        },
        {
            "name": "martin",
            "age": 59,
            "favorite_color": "green",
            "is_happy": False
        },
    ]

```

Say I want to add another person that has the following information:

```python
    person3 = {
        "name": "dylan",
        "age": 24,
        "favorite_color": "magenta",
        "is_happy": True
    }
```

I can add Dylan to the people list by just using the following code:

```people.append(person3)```

I have now appended Dylan and his information to the ```people``` list.

Now, if I run the following for loop:

```python
for person in persons:
    print(f"My name is {person["name"]} and my age is {person["age"]}. My favorite color is {person["favorite_color"]}. To answer if I am happy, I will say {person["is_happy"]}.")
```

The output to this code should be:

```
My name is selam and my age is 18. My favorite color is pink. To answer if I am happy, I will say True.
My name is martin and my age is 59. My favorite color is green. To answer if I am happy, I will say False.
My name is dylan and my age is 24. My favorite color is magenta. To answer if I am happy, I will say True.
```

### Exercise 3 Continued
``` 
Head back to exercise3.py

Part 5. 
Append a new expense called expense3 to your expenses list.

Part 6.
Loop over your expenses list again and print out each expense. Each expense should look something like:
"My expense is buying milk. It cost me $20. I bought it on 08-24-2023" Your new expense should appear at the bottom.
```

## Lesson 5: Asking for Input

So far, our code has just been us (as developers) writing out what we want to see.

- However, what if we want to make our app more interactive?

- What if we want the user (not us) to tell us information about themselves? 

- How can we prompt the user?

We can use this thing called ```input```.

Type ```input("What is your favorite color? ")```.

What happens?

You should see the question pop up on your terminal and the program is waiting for an answer before it closes. Once you enter the answer, the program will close.

This is one way to make the experience interactive for the end user.

You can also save whatever the end user types to variables and do something with that information.

Example:
```python

name = input("What is your first name ")
age = int(input("What is your age? "))
favorite_color = input("What is your favorite color? ")

print(f"Your name is {name} and your age is {age}. Your favorite color is {favorite_color}.")

```

Here, we've printed the information back to the end user.

What's cool is you can now take that information and append it to the people's array.

Example:
```python

name = input("What is your first name ")
age = int(input("What is your age? "))
favorite_color = input("What is your favorite color? ")

person4 = {
    "name": name,
    "age": age,
    "favorite_color": favorite_color,
    "is_happy": True
}

people.append(person4)

for person in persons:
    print(f"My name is {person["name"]} and my age is {person["age"]}. My favorite color is {person["favorite_color"]}. To answer if I am happy, I will say {person["is_happy"]}.")

```

In fact, this is KIND OF how sign up works. You input your information into a nice form, your information gets registered to some database and you're all logged in.



