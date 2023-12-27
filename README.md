![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E) ![PHP](https://img.shields.io/badge/php-%23777BB4.svg?style=for-the-badge&logo=php&logoColor=white) 

## 📝 Project Ninja Guerreiro

📜**This repository consists of the source code of a form made in HTML/CSS using PHP as its back-end together with the MySQL Database.**

## Table of Contents

  * [Introduction](#Introduction)
  * [Registering users with HTML and PHP](#sign-up)
    + [HTML](#HTML)
    + [PHP](#PHP)

## Introduction

adadada

## Registering users with HTML and PHP

Typically, a web page has a landing page, but we decided to begin with the sign-up system since it will help determine a database setup.

This system is composed of **four inputs from HTML**. The connection with the database will be made using **PHP**.

Using **HTML**, we can define the building blocks of the signup system. It is worth noting that this can be done using **Bootstrap**, but it is always good to **practice the basics of HTML**.

To simplify the process, only **HTML** will be used for the landing page instead of **extensive CSS coding**. However, it is still important to consider certain factors to avoid any potential issues during the development process.

### HTML

```
<div class="sign" id="signup">
	<!-- It's important to mention that one the attribute "name=''" is used on the PHP file -->
	<form method="POST" action="exemple.php"> <!-- The method POST creates a request for the action -->
		<input type="text" id="username" class="user-name" name="username" placeholder="username">
		<input type="email" id="email" class="e-mail" name="email" placeholder="email">
		<input type="password" id="password" class="pass-word" name="password" placeholder="password">
		<input type="password" id="corfirmpassword" class="confirm_password" name="confirm-password" placeholder="confirm password">
		<button id="sign-button">Register!</button> <!-- Send the form -->
	</form>
</div>
```
Notice that each ID or CLASS will not be used yet, so you do not have to follow or copy this code. Try to build your example. Furthermore, pay attention to the name attribute definition. Choose a name that matches the input action, as it will make the next part easier to understand. Now, let's start with the PHP file.

### PHP

```
<?php
    include "./env.php";
    new DB_Connection();
?>
```

