#Explicação da resolução dos erros:

* Inicialmente, faltava um ponto e vírgula na linha 7, que continha o seguinte código "$consulta = $pdo->prepare($sqls)"

* Também foi notado que para o projeto funcionar, foi necessário comentar a linha 8, que continha o código "$consulta->bindParam(":login", $login);"

* Foi preciso alterar a configuração de conexão com o banco de dados para $usuario = root, $senha = root e $banco = (nome do meu banco)