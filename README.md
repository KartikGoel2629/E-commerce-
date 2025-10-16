# FullStack_Ecommerce_App

# Table of contents
- [About](#About)
- [Working](#Working)
- [Features](#Features)
- [App_Overview](#App_Overview)
  * [Products_List_Page](#Products_List_Page)
  * [Product_Details_Page](#Product_Details_Page)
  * [Checkout_Page](#Checkout_Page)
  * [Payment_Confirmation_Page](#Payment_Confirmation_Page)
  * [Payment_successfull_Page](#Payment_successfull_Page)
  * [User_Orders_Page](#User_Orders_Page)
  * [Login_Page](#Login_Page)
  * [Register_Page](#Register_Page)
- [Installation_and_Setup](#Installation_and_Setup)
  * [Backend_Setup_(Django)](#Backend_Setup_(Django))
  * [Frontend_Setup_(React)](#Frontend_Setup(React))
  * [Stripe_Card_details](#Stripe_Card_details)

## About
This project is a full-stack e-commerce web application built using React (Frontend) and Django REST Framework (Backend).
It allows users to browse products, manage their cart, make test payments via Stripe API, and view their order history.
The application uses JWT (JSON Web Tokens) for user authentication, ensuring that all sensitive actions (like managing orders, payments, or user data) are protected with secure, token-based verification.
Users can register, log in, update their profiles, and view their order history through a dedicated dashboard.

## Working
### Frontend (React)
- The user interacts with the website through a clean React interface.
- When actions like login, registration, or checkout occur, React sends HTTP requests to the backend using Axios.

### Backend (Django REST Framework)
- The backend receives these requests and processes them.
- It checks authentication using JWT Tokens.
- Django handles business logic — like validating payments, managing user data, and updating orders.

### Database (MySQL/SQLite)
- All information such as users, product details, and order history is stored in the database.

### Payment System (Stripe API)
- When a user checks out, the Stripe API (in test mode) simulates the payment.
- Even random card details (provided they’re Stripe test numbers) will return a “Payment Successful” message.

### Authentication Flow (JWT)
- When a user logs in, Django creates a JWT token.
- The token is sent to the frontend and stored (e.g., in local storage).
- Every subsequent request includes this token in the header for verification.

## Features

- Browse and search for products
- View detailed product pages
- Add/remove items from cart
- Checkout and simulate payments with Stripe
- View past orders
- User authentication (login/register/update account)

## App_Overview
### Products_List_Page
This page displays all the available products on the website.
<p align="center">
  <img width="1357" height="746" alt="Kartik (6)" src="https://github.com/user-attachments/assets/70173382-0296-4c4f-94cd-9ce7d4d64f67" />
</p>

### Product_Details_Page
This page displays the details of the Product which user has selected from the products list page. Here, the user can see all the info of the Product such as product name, description, in stock or out of stock and pay with stripe button. 
<p align="center">
 <img width="1366" height="585" alt="Kartik (5)" src="https://github.com/user-attachments/assets/f6cb4b7a-be31-4dab-a162-39ab99721330" />
</p>

### Checkout_Page
This page displays the info of the product which user has selected for the purchase. The page Contains the product information and provides pay with stripe card
option. The user can also save their card for future payments. The user can also select or edit their address from the page.

<p align="center">
 <img width="1366" height="768" alt="ecommerce checkout page png (1158×634) (1)" src="https://github.com/user-attachments/assets/1ccd743b-c443-4a34-9943-a427f9bad9de" />

</p>

### Payment_Confirmation_Page
The page displays total amount info, the address selected by the user for delivery and the card number used for the purchase. The user can also select a different card and
address from the same page if something wents wrong.

<p align="center">
  <img width="1366" height="712" alt="Kartik (2)" src="https://github.com/user-attachments/assets/d9638667-3afb-47f2-93ce-67ff83ad4987" />
</p>

### Payment_Successfull_Page
The Page displays the confirmation of the product purchase. Also, provides info like which product is bought and how much amount was paid for it. Go to orders page is
also provided to see the order details.

<p align="center">
 <img width="1366" height="274" alt="Kartik (4)" src="https://github.com/user-attachments/assets/ce58b358-3f22-4db3-80be-a21578089ec8" />
</p>

### User_Orders_Page
The page displays the list of all the orders made by user, with the details like their name, card number used, date of purchase, address etc.

<p align="center">
  <img width="1366" height="407" alt="Kartik (8)" src="https://github.com/user-attachments/assets/de777877-b6a0-479e-b85d-145fcbe04618" />
</p>

### Login_Page
Requires an Account on the Website
<p align="center">
  <img src="https://github.com/YashMarmat/Pages-App-django/blob/master/templates/ecommerce%20%20sign%20in%20page.png?raw=true" width="100%">
</p>

### Register_Page
New users can make an account on the website.
<p align="center">
  <img src="https://github.com/YashMarmat/Pages-App-django/blob/master/templates/ecommerce%20%20sign%20up%20page.png?raw=true" width="100%">
</p>

## Installation and Setup
After downloading/cloning the repository code follow below steps:
* (Note: You must add your own Stripe Secret Key and Publishable Key in the Django settings file to enable payment functionality.)

### Backend Setup (Django)
```
cd backend
python -m venv env
env\Scripts\activate
pip install -r requirements.txt
python manage.py runserver
```

### Frontend Setup (React)
```
cd frontend
npm install
npm start
```

### Stripe Card details
- Card Number: 4242 4242 4242 4242
- CVC and Expiry date can be any random number
