![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E) ![PHP](https://img.shields.io/badge/php-%23777BB4.svg?style=for-the-badge&logo=php&logoColor=white) 

## 📝 Project Ninja Guerreiro

📜**This repository consists of the source code of a form made in HTML/CSS using PHP as its back-end together with the MySQL Database.**

## Table of Contents

  * [Introduction](#Introduction)
  * [Registering users with HTML and PHP](#sign-up)
    + [HTML](#HTML)
    + *[HTML](#HTML_SIGN)
    + [PHP](#PHP)

## Introduction

adadada

## Registering users with HTML and PHP

Typically, a web page has a landing page, but we decided to begin with the sign-up system since it will help determine a database setup.

This system is composed of **four inputs from HTML**. The connection with the database will be made using **PHP**.

Using **HTML**, we can define the building blocks of the signup system. It is worth noting that this can be done using **Bootstrap**, but it is always good to **practice the basics of HTML**.

To simplify the process, only **HTML** will be used for the landing page instead of **extensive CSS coding**. However, it is still important to consider certain factors to avoid any potential issues during the development process.


---
### HTML
### HTML SIGNUP
Typically, a web page has a landing page, but we decided to begin with the sign-up system since it will help determine a database setup.

This system is composed of four inputs from HTML. The connection with the database will be made using PHP.

Using HTML, we can define the building blocks of the signup system. It is worth noting that this can be done using Bootstrap, but it is always good to practice the basics of HTML.

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
Notice that each ID or CLASS will not be used yet, so you do not have to follow or copy this code. Try to build your example. Furthermore, pay attention to the name attribute definition. Choose a name that matches the input action, as it will make the next part easier to understand. Now, let's advantage and also build the login code.

---
**HTML LOGIN**

Using the same system that will be made in PHP, we can also start building the login code in HTML. Follow the code, and pay attention to the name attribute.

### HTML

```
<div class="login" id="login">
	<form method="POST" action="example.php">

		<input type="email" id="email" class="e-mail" name="email2" placeholder="email">
		<!-- For those who didn't notice I changed the name attribute name-->

		<input type="password" id="password" class="pass-word" name="password2" placeholder="password"><!--here as well-->

		<button id="log-button">logar</button><!--You actually do have to change or specify if a button id is related to the log in or sign-up, you can choose a same id for both-->

	</form>
</div>
```
Finally, let's dive into PHP, starting with the connection.

### PHP

***Com os inputs criados podemos fazer nossa primeira requisição no PHP, mas antes de tudo isso temos que fazer a conexão com o Banco de Dados.***

***Primeiro temos que criar um novo arquivo .php, contendo as seguintes informações, DB_HOST, DB_USER, DB_PASSWORD e DB_DATABASE.***

***Segue exemplo:***

```
<?php

// Classe criada para declarar as variáveis privadas ou públicas.
class DB_Connection{
    private $host = "******"; // DB_HOST
    private $user = "******"; // DB_USER
    private $pswd = "******"; // DB_PASSWORD
    private $db = "******"; // DB_DATABASE

// Quando criada a classe, criamos também a função a ser executada.
    public function __construct(){  
				// Nesta linha criamos a variável $conn, para se referir a instância criada apartir do new, outra coisa a se observar é o $this que se trata de uma pseudo-variável que se refere a um objeto.
        $conn = new mysqli($this->host, $this->user, $this->pswd, $this->db);

				// Aqui ocorre uma condição, SE $conn for igual a connect_error, ou ocorrer um erro do mesmo, ele mata o código("die()") e apresenta o erro.
        if($conn->connect_error){
            die("Erro na conexão!");
        }
				// Caso o código passe por todas as etapas sem apresentar erro, ele escreve na tela a mensagem "Conexão Estabelecida!".
        echo "Conexão Estabelecida!";
    }
}

?> 
```
..

