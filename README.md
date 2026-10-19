import re

password = input("Enter password: ")

length = len(password) >= 8
upper = bool(re.search(r"[A-Z]", password))
lower = bool(re.search(r"[a-z]", password))
digit = bool(re.search(r"\d", password))
special = bool(re.search(r"[^A-Za-z0-9]", password))

score = sum([length, upper, lower, digit, special])

print("Strong password" if score >= 5 else "Weak password")# password-strength-checker
