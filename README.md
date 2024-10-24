# Email Slicer function
def email_slicer(email):
    try:
        # Split the email into username and domain
        username, domain = email.split('@')
        return username, domain
    except ValueError:
        return "Invalid email format. Please enter a valid email."

# Get email input from the user
email = input("Enter your email address: ")

# Call the email slicer function and get the result
result = email_slicer(email)

# Output the result
if isinstance(result, tuple):
    print(f"Username: {result[0]}")
    print(f"Domain: {result[1]}")
else:
    print(result)
