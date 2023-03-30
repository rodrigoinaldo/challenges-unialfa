#### Itens feitos

* O problema era a varável $sqls que não existia, tive que mudar para $sql
* Faltava um ; na "$consulta = $pdo->prepare($sql)"
* Tive que criar um banco de dados
* Esse código "$consulta->bindParam(":login", $login);" era completamente inútil nessa situação, tive que apagar ele
* No connection.php, tive que mudar a senha para root
* Ainda no connection.php, eu tive que colocar o nome do banco de dados que eu criei na variável $banco