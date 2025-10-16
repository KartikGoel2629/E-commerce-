# FullStack_Ecommerce_App
A demo full-stack e-commerce application built using React and Django REST Framework, featuring JWT-based authentication and Stripe test-mode payments.
Users can register, browse products, add them to a cart, and simulate secure checkouts.

# Table of contents
- [About_this](#About_this)
- [App_Overview](#App_Overview)
  * [Products_List_Page](#Products_List_Page)
  * [Product_Details_Page](#Product_Details_Page)
  * [Checkout_Page](#Checkout_Page)
  * [Payment_Confirmation_Page](#Payment_Confirmation_Page)
  * [Payment_successfull_Page](#Payment_successfull_Page)
  * [User_Orders_Page](#User_Orders_Page)
  * [Login_Page](#Login_Page)
  * [Register_Page](#Register_Page)
- [Installation](#Installation)
  * [Backend](#backend)
  * [Frontend](#frontend)

## About_this
An Ecommerce website where users can purchase products by using their stripe card.  Users are allowed to visit our website and free to look any product details. User needs to create an account on our website to proceed with the payment section. If a user want they can also delete their account anytime (NOTE: With the deletion of a user account all their info like Account details, Address details, Card details will be deleted as well)

The website also provides the flexibility to create a new stripe card if they do not have one, the user can also pay with other user stripe card (if they provide the right email address linked with the card and other card details like Card Number, Exp Month, Exp Year and CVC). The user can also detete their stripe card if they like (Caution: With the deletion of their stripe card their account related to that card will also be deleted as well). 

## App_Overview
### Products_List_Page
This page displays all the available products on the website.
<p align="center">
  <img width="1357" height="746" alt="Kartik (6)" src="https://github.com/user-attachments/assets/70173382-0296-4c4f-94cd-9ce7d4d64f67" />
</p>

### Product_Details_Page
This page displays the details of the Product which user has selected from the products list page. Here, the user can see all the info of the Product such as product name, description, in stock or out of stock and pay with stripe button. For Admins, the website provides two more functionalities such as Updating the product and secondly deleting the product.
<p align="center">
  <img width="1366" height="657" alt="Kartik (5)" src="https://github.com/user-attachments/assets/73f515a9-795d-4651-bc99-077a610a349a" />
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
<p align="center">
  <img src="https://github.com/YashMarmat/Pages-App-django/blob/master/templates/ecommerce%20%20sign%20up%20page.png?raw=true" width="100%">
</p>

### Other_Functionalities
-JWT Authentication: The website uses JSON Web Tokens (JWT) to verify user identity and manage authentication securely.
-Secure Transactions: Strong backend security checks are implemented during card creation and payment processing.
-Request Validation: Every request (except Product List and Product Details pages) is authenticated using the JWT token to ensure user safety and data protection.

## Installation and Setup
after downloading/cloning the repository code follow below steps:
* (Note: You must add your own Stripe Secret Key and Publishable Key in the Django settings file to enable payment functionality.)

### To Run
install `pygame` pacakge
```
pip install pygame
```
then run the 'main.py' file
```
python main.py
```



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

