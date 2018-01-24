# EShop
Introduction:
This project consists of RESTful services that implement a checkout counter for an online retail store that scans products and generates itemized bill.

It provides services for see products and place orders. Products can be configured with rate and category (A,B or C). Sales tax is applied based on the category of the product:

Category A - 10%
Category B - 20%
Category C- 0%
Bill details the products, quantity, total cost,sales tax and the total value of the bill.

REST endpoints
Client can add products to cart and orders using the REST endpoints. Below is overview of REST end points:

Products
GET /items - fetches list of all product data.
POST /addToCart/{uid}/{pid} - add product to users cart using user ID and oriduct ID.
GET /viewCart/{uid} - see the cart product and total price and taxes.
DELETE /removeFromCart/{uid}/{pid} - delete product from users cart using product ID.
POST /checkout/{uid} - After the bill payment cart will be empty.

These REST end points are secured using basic authentication mechanism. Code uses in-memory repository with list of users to authenticate. (eg. Username:abc@123.com, Password:epass)

About Implementation
This application has been using Jersy jars as it provides a wide variety of features that aid development and maintainence.

This program and instructions have been tested on following versions on Windows laptop.

Tomcat 7
Java version: 1.7
