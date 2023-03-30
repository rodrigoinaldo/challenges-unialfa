#### Respostas


* O problema era a variável $sqls que não existia
* Faltava um; na linha 7 do "index.php"
* Foi preciso apagar a linha 8 do "index.php" por que não tem informações de login para retornar do banco. 
* Faltava informações de configuração para acessar o banco de dados (port, senha, nome do banco)