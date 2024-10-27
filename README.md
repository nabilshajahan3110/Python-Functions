
# PYTHON FUNCTIONS

# 1.What does the len() function do in Python? Write a code example using len() to find the length of a list.

# A. The len() function is used to determine the length or number of items in a collection such as string, tuple, sets, dictionaries or lists. It returns an integer representing the length of the given object

l1 = list(range(1,7))
print(l1,type(l1),len(l1))


![DF 1](https://github.com/user-attachments/assets/4278b5cb-4811-4c18-80a0-76ed9f3d18ec)


# 2.Write a Python function greet(name) that takes a person's name as input and prints "Hello, [name]!".

def greet(name):
    print(f"Hello, {name}!")

name = str(input("Enter the name: "))

greet(name)


![DF 2](https://github.com/user-attachments/assets/5dfa48ec-6c05-4590-b333-d1aeccfd79ad)


# 3.Write a Python function find_maximum(numbers) that takes a list of integers and returns the maximum value
#   without using the built-in max() function. Use a loop to iterate through the list and compare values.

def find_maximum(numbers):
    if not numbers:  # Check if the list is empty
        return None

    max_value = numbers[0]
    for number in numbers:
        if number > max_value:
            max_value = number
    return max_value

numbers = [3, 5, 2, 10, 1]
print(find_maximum(numbers))


![DF 3](https://github.com/user-attachments/assets/3072064f-d5da-42e5-94ec-c5b6860dbc75)


# 4.Explain the difference between local and global variables in a Python function. Write a program where a global variable and a local variable have the same name and show how Python differentiates between them.

# A. Python Global variables are those which are not defined inside any function and have a global scope. They are defined outside any function and are accessible throughout the program.

# Python local variables are defined inside a function and their scope is limited inside that function alone. They are only accessible inside the function.


# Local variable
def l():
    s = "My name is Nabil"
    print(s)

l()


![PF 4 A](https://github.com/user-attachments/assets/0227d2e0-8863-4512-bfad-b18bf1861173)


# Local variable called outside
l()
print(s)


![PF 4 B](https://github.com/user-attachments/assets/e2ddb53e-f143-431a-9d60-eb833cba3e32)


# Global variable
def g():
    print("Inside Function",s)

s = "My name is Nabil"
g()
print("Outside Function",s)


![PF 4 C](https://github.com/user-attachments/assets/268143af-0b66-4966-806a-0214ea49aab1)


# 5.Create a function calculate_area(length, width=5) that calculates the area of a rectangle. If only the length is provided, the function should assume the width is 5. Show how the function behaves when called with and without provided, the function should assume the width is 5. Show how the function behaves when called with and without the width argument.

def area_of_rectangle(length, width=5):
    area = length * width
    return(area)

Area_with_Width = area_of_rectangle(15,3)
print(f"The area of rectangle with length and width is {Area_with_Width} square units.")

Area_with_Default_Width = area_of_rectangle(15)
print(f"The area of rectangle with length and default width is {Area_with_Default_Width} square units.")



![PF 5](https://github.com/user-attachments/assets/4c847adc-1fcc-42bf-909e-b0331a6f2bc6)

