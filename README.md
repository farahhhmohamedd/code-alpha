def fibonacci_recursive(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci_recursive(n-1) + fibonacci_recursive(n-2)

def get_user_input():
    while True:
        try:
            num_terms = int(input("Enter the number of terms for the Fibonacci series: "))
            if num_terms <= 0:
                raise ValueError("The number must be a positive integer.")
            return num_terms
        except ValueError as e:
            print(f"Invalid input: {e}. Please try again.")

if __name__ == "__main__":
    num_terms = get_user_input()
    
    print(f"Fibonacci series up to {num_terms} terms:")
    for i in range(num_terms):
        print(fibonacci_recursive(i))
