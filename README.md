# Basic Calculator Program
# This program performs basic arithmetic operations on two numbers

def calculator():
    print("\nWelcome to the Basic Calculator!")
    print("Available operations: + (addition), - (subtraction), * (multiplication), / (division)\n")
    
    try:
        # Get user input
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))
        operation = input("Enter operation (+, -, *, /): ").strip()
        
        # Perform calculation
        if operation == '+':
            result = num1 + num2
            print(f"\nResult: {num1} {operation} {num2} = {result}")
        elif operation == '-':
            result = num1 - num2
            print(f"\nResult: {num1} {operation} {num2} = {result}")
        elif operation == '*':
            result = num1 * num2
            print(f"\nResult: {num1} {operation} {num2} = {result}")
        elif operation == '/':
            if num2 == 0:
                print("\nError: Cannot divide by zero!")
            else:
                result = num1 / num2
                print(f"\nResult: {num1} {operation} {num2} = {result}")
        else:
            print("\nError: Invalid operation entered! Please use +, -, *, or /")
    
    except ValueError:
        print("\nError: Please enter valid numbers!")

# Run the calculator
if __name__ == "__main__":
    calculator()
