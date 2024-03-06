# my_homewk
# 1. Basics of Lambda: Create a lambda function that multiplies any number by 10.

    x = int(input("input a number")) result = lambda x: x*10 print(result(x))

# 2. Using Map: Given a list of integers, use map() to double each number in the

# list.

    list_nums = (2,4,6,8) double = map(lambda x: x*2, list_nums) print(list(double))

# 3. Using Filter: Given a list of numbers, use filter() to extract all the even numbers.

    even_numbers = list(filter(lambda x:x % 2 == 0, range(20))) print(even_numbers)

4. Using Reduce: Use reduce() to find the product of all numbers in a given list.

        from functools import reduce

        def add(x,y): c = x * y result = f"{x} * {y} = {c}" return (c) c = reduce(add, [3,6,8]) print(c)

#6. Combining Map & Filter: Given a list of numbers, first filter out the even

numbers and then square them using map().

    test = list( map(lambda x: x ** 2, filter(lambda x: x % 2, range(1,10))) ) print(test)

Write a python function to create a simple Calculator.

    def add(x, y): return x + y
    
    def subtract(x, y): return x - y
    
    def multiply(x, y): return x * y
    
    def divide(x, y): return x / y
    
    print("Select operation.") print("1.Add") print("2.Subtract") print("3.Multiply") print("4.Divide")
    
    while True: choice = input("Enter choice(1/2/3/4): ")
    
    if choice in ('1', '2', '3', '4'):
        try:
            num1 = float(input("Enter first number: "))
            num2 = float(input("Enter second number: "))
        except ValueError:
            print("Invalid input. Please enter a number.")
            continue

    if choice == '1':
        print(num1, "+", num2, "=", add(num1, num2))

    elif choice == '2':
        print(num1, "-", num2, "=", subtract(num1, num2))

    elif choice == '3':
        print(num1, "*", num2, "=", multiply(num1, num2))

    elif choice == '4':
        print(num1, "/", num2, "=", divide(num1, num2))

    next_calculation = input("Let's do next calculation? (yes/no): ")
Write a python function to find max of two numbers.
        
        def max_of_two_num(n,m): if n>m: return n else: return m n,m = 4,6 print(m)

Write a python function to sum all numbers from given list. def sum(numbers): total = 0 for x in numbers: total += x return total print(sum((8, 2, 3, 0, 7)))
10.Write a python function to multiply all numbers from given list.

    def mul_list(list): product = 1 for i in list: product = product * i return product

    list1 = [2, 3, 4, 5] print(mul_list(list1))

11.You are given a program that takes all 3 passengers ages as inputs and inserts them in a list. Complete the program so that if it finds a value less than 16, it breaks the loop and outputs "Too young! ". If the age requirement is satisfied, the program outputs "Get ready!".

    ages = [] i = 0 while i<3: age= int(input()) ages.append(age) i+=1

    for i in ages:
    if i<16:
        print("Too young!")
    else:
        print("Get ready")
