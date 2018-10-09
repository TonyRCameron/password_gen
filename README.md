# password_gen
#A simple password generator

"""
Generate a password
Strong passwords have a mix of lowercase letters, uppercase, numbers and
symbols
Extra:
Ask for strong or weak password. Weak picks 1 or 2 words from a list
"""
import random
import string

#Generate a list with all possible characters then take from list

def pass_gen():
    password = None
    characters = []
    weak = ['this', 'is', 'weak', 'password']
    strength = input('Generate strong or weak password? : ').lower()

    if strength == 'weak':
        password = "".join(random.sample(weak, 2))
        print(password)

    if strength == 'strong':
        num = int(input('How many characters long? : '))

        characters = string.digits, string.ascii_letters, string.punctuation
        characters = "".join(characters)
        password = random.sample(characters, num)
        print("".join(password))

pass_gen()
