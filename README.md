#Python Project 1
#Roll no. :09
import math
def add(n1, n2):
    return n1 + n2
def subtract(n1, n2):
    return n1 - n2

def multiply(n1, n2):
    return n1 * n2

def divide(n1, n2):
    if n2 != 0:
        return n1 / n2
    else:
        return "Division by zero is not possible."
def sqrt(num):
     if ( num>=0):
        return math.sqrt(num)
     else:
        return "Sorry . Square root of a negative number"

def display_menu():
    print("Select operation:")
    print("1. Additon")
    print("2. Subtraction")
    print("3. Multiplication")
    print("4. Division")
    print("5.Square root ")
    print("6. Exit")


def calculator():
    while True:
        display_menu()

        
        choice = input("Enter choice (1/2/3/4/5/6): ")

        if choice == '6':
            print("Exiting")
            break

        
        if choice not in ('1', '2', '3', '4','5'):
            print("Invalid input! Please try again.")
            continue

        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))

        
        if choice == '1':
            print(f"{num1} + {num2} = {add(num1, num2)}")
        elif choice == '2':
            print(f"{num1} - {num2} = {subtract(num1, num2)}")
        elif choice == '3':
            print(f"{num1} * {num2} = {multiply(num1, num2)}")
        elif choice == '4':
            print(f"{num1} / {num2} = {divide(num1, num2)}")
        elif choice =='5' :
            print(f"The square root of { num1} is {sqrt(num1)} and the square root of { num2} is { sqrt(num2)}")
calculator()
