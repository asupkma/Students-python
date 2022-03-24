# Students-python
Some task about python
The task
```
1. Напишите функцию pin(), которая:

- будет просить пользователя вводить пин код, пока пользователь не введет 1234;

- если пользователь ввел 1234, то возвращает это значение;

Каждый раз при вводе пользователем цифр, данная функция должна:

- посчитать количество введённых символов и вывести это количество на печать (с помощью цикла FOR);

- вывести на печать тип введенных пользователем данных (integer, float или string);

- в случае, если пользователь ввел 123456789 – вывести на печать “You entered too many numbers”, в случае, если пользователь введет число НЕ равное 1234 – вывести на печать “Please enter the pin code one more time”, в случае, если пользователь введет 1234 – вывести на печать “You entered right pin code”.

 

2. Напишите функцию checking(), которая:

- будет принимать в качестве аргумента возвращаемое значение функции pin();

- в случае, если возвращаемое значение функции pin() будет 1234 – выведет на печать “Your code is too simple!”

 

3. Напишите код вызова функции, который демонстрирует работоспособность функций pin() и checking().
```
# Answer
```
def pin(out):                                                                          # Declare the function
    x = 1                                                                              # Set count of symbols
    while True:                                                                        # Loop continuously
        inp = raw_input('Enter PIN\n')                                                 # Get the input
        for x in range(len(inp)):                                                      # Count to the lenght of the input
            x = x+1                                                                    # Increase by one
        print(x)                                                                       # Print the count symbols in input
        if inp.isdigit():                                                              # If it is integer
            print('It is Integer\n')                                                   # Print it
            if inp == '1234':                                                          # If input is right we a searching for
                print('You entered right pin code\n')                                  # Print you are winner
                break                                                                  # Break the loop
            elif inp == '123456789':                                                   # If input one of
                print('You entered too many numbers\n')                                # Print that way
            else:                                                                      # Else because it all aboove was digits only
                print('Please enter the pin code one more time\n')                     # Wrong digits. print try again
        elif inp.replace('.','',1).isdigit() and inp.count('.') < 2:                   # Check is it float (. removed and final is digit and . iside input but only one)
            print('Its Float\n')                                                       # Print its float
        else:                                                                          # Nothing else... neither integer nor float. May be string
            print ('It is Neither Integer Nor Float! Something else. May be string\n') # Print it
    return inp                                                                         # Return input from 

def checking(bbb):                                                                     # Declare function with some variable
    if bbb == '1234':                                                                  # If it is what we are searching for
        print('Your code is too simple\n')                                               # Print it
    return                                                                             # Just return

y = pin('')                                                                            # Call the pin function to variable
checking(y)                                                                            # Call the function with variable nested function
```

