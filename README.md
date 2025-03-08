This file contains a simple password requirement system designed in Python asking users to input a password while having password requirements 




password = input("Enter a password:")
if len(password) < 8:
    print("Password MUST be at least 8 characters long")
numCount = 0
symbolCount = 0
specialSymbols = ['!','&','@','*','$']

for char in password:
    if char.isdigit():
        numCount += 1
    elif char in specialSymbols:
        symbolCount += 1
if len(password) >= 8:
    if numCount == 0:
        print("Password must have at least one number")
if symbolCount == 0:
    print("Password must have at least one special character from ! @ & * $")
if numCount > 0 and symbolCount > 0:
    print("Password meets all requirements")
    
