# FullStack_Ecommerce_App
A demo full-stack e-commerce application built using React and Django REST Framework, featuring JWT-based authentication and Stripe test-mode payments.
Users can register, browse products, add them to a cart, and simulate secure checkouts.
<p id ="top" align="center">
  <img src="https://github.com/YashMarmat/Pages-App-django/blob/master/templates/ecommerce%20%20products%20list%20page.png?raw=true" width="100%">
</p>

Checkout the site in action here <a href="https://condescending-goldstine-79a4ed.netlify.app/">Deployed App</a> (short note below)

(Note: The website can take upto 30 seconds (hosted on Heroku free tier services), as the project has no clients, its just for learning, please refer the source
code to run locally).

# Table of contents
- [About_this](#About_this)
- [App_Overview](#App_Overview)
  * [Products_List_Page](#Products_List_Page)
  * [Product_Details_Page](#Product_Details_Page)
  * [Checkout_Page](#Checkout_Page)
  * [Payment_Confirmation_Page](#Payment_Confirmation_Page)
  * [Payment_successfull_Page](#Payment_successfull_Page)
  * [Orders_Page_For_User](#Orders_Page_For_User)
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
  <img src="https://github.com/YashMarmat/Pages-App-django/blob/master/templates/ecommerce%20%20products%20list%20page.png?raw=true" width="100%">
</p>

### Product_Details_Page
This page displays the details of the Product which user has selected from the products list page. Here, the user can see all the info of the Product such as product name, description, in stock or out of stock and pay with stripe button. For Admins, the website provides two more functionalities such as Updating the product and secondly deleting the product.
<p align="center">
  <img src="https://github.com/YashMarmat/Pages-App-django/blob/master/templates/ecommerce%20%20product%20details%20page.png?raw=true" width="100%">
</p>

### Checkout_Page
This page displays the info of the product which user has selected for the purchase. The page Contains the product information and provides pay with stripe card
option. The user can also save their card for future payments. The user can also select or edit their address from the page.

<p align="center">
  <img src="https://github.com/YashMarmat/Pages-App-django/blob/master/templates/ecommerce%20%20checkout%20page.png?raw=true" width="100%">
</p>

### Payment_Confirmation_Page
The page displays total amount info, the address selected by the user for delivery and the card number used for the purchase. The user can also select a different card and
address from the same page if something wents wrong.

<p align="center">
  <img src="https://github.com/YashMarmat/Pages-App-django/blob/master/templates/ecommerce%20%20payment%20confirmation%20page.png?raw=true" width="100%">
</p>

### Payment_Successfull_Page
The Page displays the confirmation of the product purchase. Also, provides info like which product is bought and how much amount was paid for it. Go to orders page is
also provided to see the order details.

<p align="center">
  <img src="https://github.com/YashMarmat/Pages-App-django/blob/master/templates/ecommerce%20%20payment%20successfull%20page.png?raw=true" width="100%">
</p>

### Orders_Page_For_User
The page displays the list of all the orders made by user, with the details like their name, card number used, date of purchase, address etc.

<p align="center">
  <img src="https://github.com/YashMarmat/Pages-App-django/blob/master/templates/ecommerce%20%20orders%20page%20for%20normal%20user.png?raw=true" width="100%">
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
- Used JSON web tokens to achieve the authentication checks in the website.
- Strict Security Checking behind the scenes during the Card Creation and Payment Process.
- JSON Token gets checked for every single request made on the website (except products list and product details page)

## Installation
after downloading/cloning the repository code follow below steps:
* (NOTE: your need to mention your own stripe secret api key and publishable key in django to run the project)

### Backend
* (for both linux and windows)
1) Move in backend folder through terminal and run following commands,

`python3 -m venv env` (for windows --> `python -m venv env`) 

`source env/bin/activate` (for windows --> `env\scripts\activate`)

`pip install -r requirements.txt` (same for both)

`python manage.py runserver` (same for both)

### Frontend
* (for both linux and windows)
2) Move in frontend folder through terminal and run follwing commands

`npm i`

`npm start`

## All set ! Happy coding :)

<p><a href="#top">Back to Top</a></p>

