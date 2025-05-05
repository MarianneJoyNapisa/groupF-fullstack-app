# node-mysql-signup-verification-api

NodeJS + MySQL - Boilerplate API with Email Sign Up, Verification, Authentication & Forgot Password

How to run:

1. Open XAMPP
2. CMD

- npm install
- set NODE_OPTIONS=--openssl-legacy-provider && npm start

3. ethereal.email
user: gerry.jast@ethereal.email
pass: NEbEME1KxudWwJxcgr

4. Postman/Thunder Client

# Register

POST : http://localhost:4000/accounts/register

body/raw/jason
{
    "title": "Mr",
    "firstName": "Hello",
    "lastName": "Ph",
    "email": "helloPh@example.com",
    "password": "my-super-secret-password",
    "confirmPassword": "my-super-secret-password",
    "acceptTerms": true
}

# Verify Email

POST : http://localhost:4000/accounts/verify-email

{
    "token": "REPLACE THIS WITH YOUR TOKEN"
}


# Authenticate

POST : http://localhost:4000/accounts/authenticate

{
    "email": "helloPh@example.com",
    "password": "my-super-secret-password"
}

# List Accounts

GET : http://localhost:4000/accounts

Authorization/Bearer Token/Token(From authenticate)

# Update Account

PUT : http://localhost:4000/accounts/3

Authorization/Bearer Token/Token(From authenticate)

body/raw/json

{
    "status": "inactive"
}



