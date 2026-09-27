import math

# ==========================================
# Exercise 1: Calculate the area of a circle
# ==========================================
radius = float(input("Enter circle radius? "))
# Using 3.14 to match the expected output (10 -> 314.0)
area = 3.14 * (radius ** 2)
print(f"Circle area = {area}")

# ==========================================
# Exercise 2: Convert Celsius into Fahrenheit
# ==========================================
c = float(input("Enter the temperature in Celsius? "))
f = c * 9/5 + 32
print(f"{c} (C) = {f} (F)")

# ==========================================
# Exercise 3: Check whether a number is prime
# ==========================================
n_prime = int(input("Enter a number? "))
if n_prime < 2:
    print(f"{n_prime} is a NOT prime number")
else:
    is_prime = True
    for i in range(2, int(math.sqrt(n_prime)) + 1):
        if n_prime % i == 0:
            is_prime = False
            break
            
    if is_prime:
        print(f"{n_prime} is a prime number")
    else:
        print(f"{n_prime} is a NOT prime number")

# ==========================================
# Exercise 4: Check whether a number is perfect
# ==========================================
n_perfect = int(input("Enter a number? "))
if n_perfect <= 0:
    print(f"{n_perfect} is a NOT perfect number")
else:
    divisors_sum = sum(i for i in range(1, n_perfect) if n_perfect % i == 0)
    if divisors_sum == n_perfect:
        print(f"{n_perfect} is a perfect number")
    else:
        print(f"{n_perfect} is a NOT perfect number")

# ==========================================
# Exercise 5: Find favorite color in a list
# ==========================================
color_list = ["Black", "Yellow", "Blue", "Red", "White"]
color = input("What is your favorite color? ")
if color in color_list:
    index = color_list.index(color)
    print(f"Your color is at index {index} in my list")
else:
    print("Sorry, I could not find your color")

# ==========================================
# Exercise 6: Create sequences using range()
# ==========================================
range1 = list(range(7))
range2 = list(range(1, 11, 3))
range3 = list(range(5, 0, -1))
range4 = list(range(6, -3, -2))

print("range1 |", ", ".join(map(str, range1)))
print("range2 |", ", ".join(map(str, range2)))
print("range3 |", ", ".join(map(str, range3)))
print("range4 |", ", ".join(map(str, range4)))

# ==========================================
# Exercise 7: Function to remove dollar sign
# ==========================================
def remove_dollar_sign(s):
    return s.replace("$", "")

# ==========================================
# Exercise 8: Function to extract even items
# ==========================================
def extract_even(l):
    return [num for num in l if num % 2 == 0]

# ==========================================
# Exercise 9: Function to calculate factorial
# ==========================================
def calculate_factorial(n):
    if n == 0 or n == 1:
        return 1
    fact = 1
    for i in range(2, n + 1):
        fact *= i
    return fact

# ==========================================
# Exercise 10: Function to get all divisors
# ==========================================
def get_all_divisors(n):
    if n <= 0:
        return []
    return [i for i in range(1, n + 1) if n % i == 0]

# ==========================================
# Exercise 11: Function to compute distance
# ==========================================
def compute_distance(x1, y1, x2, y2):
    return math.sqrt((x2 - x1)**2 + (y2 - y1)**2)

# ==========================================
# Exercise 12: Function to print m x n pattern
# ==========================================
def print_pattern(m, n):
    for _ in range(m):
        print("* " * n)
