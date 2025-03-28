# python-assignment-1
def calculator():
    try:
        # Prompt user to enter the first number and convert to float
        num1 = float(input("Enter the first number (10): "))
        # Prompt user to enter the second number and convert to float
        num2 = float(input("Enter the second number (5): "))
        # Prompt user to enter a mathematical operation
        operation = input("Enter the operation (+, -, *, /): ")
        
        # Perform the corresponding mathematical operation
        if operation == '+':
            result = num1 + num2  # Addition
            print(f"{num1} + {num2} = {result} (10 + 5 = 15)")
        elif operation == '-':
            result = num1 - num2  # Subtraction
            print(f"{num1} - {num2} = {result} (10 - 5 = 5)")
        elif operation == '*':
            result = num1 * num2  # Multiplication
            print(f"{num1} * {num2} = {result} (10 * 5 = 50)")
        elif operation == '/':
            if num2 != 0:  # Check to prevent division by zero
                result = num1 / num2  # Division
                print(f"{num1} / {num2} = {result} (10 / 5 = 2.0)")
            else:
                print("Error: Division by zero is not allowed.")
        else:
            print("Invalid operation. Please enter +, -, *, or /.")
    except ValueError:
        # Handle the case where the user inputs a non-numeric value
        print("Error: Please enter valid numbers (10, 5).")

# Call the calculator function to execute the program
calculator()
