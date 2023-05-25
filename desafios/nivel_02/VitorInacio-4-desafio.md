### Desafio usando SESSION

### form.php
* No form.php eu fiz uma verificação, caso tenha algum valor via POST, vai verificar se a senha ou o login estão corretos, e aí sim vai criar uma SESSION 

~~~ php
    if ($_POST) {
        $login = $_POST["login"] ?? NULL;
        $senha = $_POST["senha"] ?? NULL;

        if (($login != "cavalo") && ($senha != "cavalo")){
            echo "<script>alert('Acesso negado, usuario ou senha incorreto')</script>";
        };

        $_SESSION["usuario"] = array(
            "login" => $login,
            "senha" => $senha
        );
    }
~~~

* E aqui eu fiz o formulário

~~~ php
    <h1>Efetuar login</h1>
    <form method="POST">
        <label for="login">Login:</label>
        <input for="text" name="login" id="login" required placeholder="Por favor, preencha este campo">

        <br>

        <label for="senha">Senha:</label>
        <input type="password" name="senha" id="senha" required placeholder="Por favor, preencha esse campo">

        <br>

        <button type="submit">Efetuar Login</button>
    </form>
~~~

### index.php

* Primeiramente, eu startei a sessão

~~~ php
    <?php
        session_start()
    ?>
~~~

* Depois dentro do body, eu fiz uma verificação, caso não tenha nenhuma sessão, ele vai requerir o form.php, caso tenha, ele só vai imprimir o que está dentro 

~~~ php
    <?php
        if (!isset($_SESSION["usuario"])) {
            require "form.php";
        }else {
            print_r ($_SESSION);
        }
    ?>
~~~