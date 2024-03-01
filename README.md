# Simple-Calc
Simple python calculator
def add(num1, num2):
  """Adds two numbers and returns the sum."""
  return num1 + num2

def subtract(num1, num2):
  """Subtracts two numbers and returns the difference."""
  return num1 - num2

def multiply(num1, num2):
  """Multiplies two numbers and returns the product."""
  return num1 * num2

def divide(num1, num2):
  """Divides two numbers and returns the quotient. Handles division by zero."""
  if num2 == 0:
    return "Error: Cannot divide by zero."
  else:
    return num1 / num2

while True:
  # Get user input for operation
  print("Select operation:")
  print("1. Add")
  print("2. Subtract")
  print("3. Multiply")
  print("4. Divide")
  print("5. Exit")

  choice = input("Enter choice(1/2/3/4/5): ")

  # Get numbers
  if choice in ('1', '2', '3', '4'):
    try:
      num1 = float(input("Enter first number: "))
      num2 = float(input("Enter second number: "))
    except ValueError:
      print("Invalid input. Please enter numbers only.")
      continue

  # Perform operation based on choice
  if choice == '1':
    result = add(num1, num2)
    print(num1, "+", num2, "=", result)
  elif choice == '2':
    result = subtract(num1, num2)
    print(num1, "-", num2, "=", result)
  elif choice == '3':
    result = multiply(num1, num2)
    print(num1, "*", num2, "=", result)
  elif choice == '4':
    result = divide(num1, num2)
    print(num1, "/", num2, "=", result)
  elif choice == '5':
    print("Exiting calculator.")
    break
  else:
    print("Invalid input.")

