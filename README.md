start, end = input().split()
start = int(start)
end = int(end)

if start >= end:
    print("Ошибка: начало диапазона должно быть меньше конца")
else:
    fib1, fib2 = 0, 1
    fibonacci_numbers = []
    
    while fib1 <= end:
        if fib1 >= start:
            fibonacci_numbers.append(fib1)
        fib1, fib2 = fib2, fib1 + fib2
    
    if fibonacci_numbers:
        print(" ".join(map(str, fibonacci_numbers)))
    else:
        print("В заданном диапазоне нет чисел Фибоначчи")
