####Resolução desafio 02 Exercicio 1

*Primeiramente fiz a configuração da conecção com o banco
*Alterando o campo senha pra =>"" (vazia).
*Alterei a porta 9999 para 3306.
*Criamos o banco de dados com nome desafio2 e criamos a tabela challenge

*No index havia erro de sintax na Variavel sql
*Faltava um (;) na linha onde preparava o sql para a variavel $consulta
*Removi a linha   $consulta->bindParam(":login", $login);