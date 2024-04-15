# Sale website with Alepay payment method

```
Create your Alepay account on "https://alepay-merchant.nganluong.vn/vi/dashboard/login".
Get your checksumkey and add it to checkSumKey at line 13 in common\models\SignatureHash.php
Get your tokenkey and add it to tokenKey at line 21 in frontend\models\Order.php

Frontend    :    Site where customers purchase merchant's products.
                 . Sign up with email and there will be file.eml in frontend\runtime\mail
                 . Enter the link in that file to verify email /* Read Yii2 tutorial on Youtube to know how to get the correct link */
                 . Customers should enter correct form of email, phone number to get access to payment methods.

Backend     :    Site where merchants up their products.   
                 . Log in with account signed up in Frontend

Phpmyadmin  :    Manage your database.

Prometheus  :    Get your system metrics and export them to Grafana.

Grafana     :    Visualize your system metrics. 
```

## Introduction
Using ```docker-compose up --build``` to up this project onto your Docker.
Then open alepay-backend terminal to run ```php yii migrate``` to create table in your database.
<p align="center">
  <img src="demo/yii migrate.jpg" width=800><br/>
  <img src="demo/applying.jpg" width=800><br/>
  <img src="demo/5 migrations .jpg" width=800><br/><br/>
</p>

## Login to phpmyadmin to control your data server.
<p align="center">
  <img src="demo/phpmyadmin.jpg" width=800><br/><br/>
</p>

## Sign up account in ```localhost:20080```
<p align="center">
  <img src="demo/1.jpg" width=800><br/>
  After sign up, you will see this notfication<br/>
  <img src="demo/thanks for registration.jpg" width=600><br/>
  In phpmyadmin, User table: status equals 9 if email is not confirmed.<br/>
  <img src="demo/user in db.jpg" width=600><br/>
</p>

## Confirm email
<p align="center">
  Open /app/frontend/runtime/mail in Docker Desktop.<br/>
  <img src="demo/mail.jpg" width=800><br/>
  Enter confirm link onto browser.<br/>
  <img src="demo/paste link.jpg" width=800><br/>
  <img src="demo/mail confirmed.jpg" width=800><br/>
  User status equals 10 after email is confirmed.<br/>
  <img src="demo/user in db _ 10.jpg" width=800><br/>
</p>

## Login ```localhost:21080``` and push merchant's product onto cart.
<p align="center">
  Click on 'Tạo sản phẩm mới' to push new product,<br/>
  <img src="demo/product.jpg" width=800><br/>
  Upload product's image.<br/>
  <img src="demo/create_product.jpg" width=800><br/>
  Edit your product.<br/>
  <img src="demo/edit_product.jpg" width=800><br/>
  <img src="demo/view_product.jpg" width=800><br/>
  <img src="demo/list_product.jpg" width=800><br/>
</p>

## Customer purchase product on site ```localhost:20080```
<p align="center">
  <img src="demo/list_product_frontend.jpg" width=800><br/>
  <img src="demo/cart.jpg" width=800><br/>
  <img src="demo/confirm_order.jpg" width=800><br/>
  <img src="demo/confirm_order_2.jpg" width=800><br/>
  <img src="demo/payment.jpg" width=800><br/>
</p>

<p align="center">
  <img src="demo/spanish_output.jpg" width=800><br/>
  <i>Spanish</i>
</p>

<p align="center">
  <img src="demo/russian_output.jpg" width=800><br/>
  <i>Russian</i>
</p>

