import random
import string

def generate_password(length):
    """Generate a complex password without special characters."""
    characters = string.ascii_letters + string.digits
    
    password = [
        random.choice(string.ascii_uppercase),  # At least one uppercase letter
        random.choice(string.ascii_lowercase),  # At least one lowercase letter
        random.choice(string.digits)            # At least one digit
    ]
    
    password += random.choices(characters, k=length - 3)
    random.shuffle(password)  # Shuffle to ensure randomness
    return ''.join(password)

def generate_multiple_passwords(count, length):
    """Generate a list of complex passwords with the specified count and length."""
    return [generate_password(length) for _ in range(count)]


passwords_12 = generate_multiple_passwords(1000, 12)
passwords_8 = generate_multiple_passwords(1000, 8)


print("12-character complex passwords:")
for pwd in passwords_12:
    print(pwd)


print("\n8-character complex passwords:")
for pwd in passwords_8:
    print(pwd)
