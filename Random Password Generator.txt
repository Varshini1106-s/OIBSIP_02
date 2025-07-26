import random
import string

def generate_password(length, use_letters, use_digits, use_symbols):
    character_set = ''
    
    if use_letters:
        character_set += string.ascii_letters  # A-Z + a-z
    if use_digits:
        character_set += string.digits         # 0-9
    if use_symbols:
        character_set += string.punctuation    # !@#$%^&*()

    if not character_set:
        print("You must select at least one character type.")
        return None

    password = ''.join(random.choice(character_set) for _ in range(length))
    return password

def get_user_input():
    try:
        length = int(input("Enter desired password length (e.g. 8, 12): "))
        if length <= 0:
            print("Length must be a positive number.")
            return None

        use_letters = input("Include letters? (y/n): ").lower() == 'y'
        use_digits = input("Include digits? (y/n): ").lower() == 'y'
        use_symbols = input("Include symbols? (y/n): ").lower() == 'y'

        return length, use_letters, use_digits, use_symbols

    except ValueError:
        print("Invalid input. Please enter a number for password length.")
        return None

def main():
    print("🔐 Random Password Generator")
    user_input = get_user_input()
    
    if user_input:
        length, use_letters, use_digits, use_symbols = user_input
        password = generate_password(length, use_letters, use_digits, use_symbols)
        if password:
            print(f"\nYour generated password is: {password}")

if __name_ == "__main__":
    main()
