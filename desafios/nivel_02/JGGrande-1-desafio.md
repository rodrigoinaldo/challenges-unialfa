# Desafio 1

### comecei o desafio arrumando alguns erros basicos que encontrei por primeiro.

* Coloquei um ponto e vírgula que estava faltando na linha 7;
* Removi o s de "sqls" na linha 7 para se referir a variavel da "sql" da linha 4;
* Removi a linha 8 pois não tinha nessecidade de parametros, estava apenas gerando erro.
* Removido var_dump da linha 13.

### Indo para o connection.php
* Foi alterado o valor da variavel $senha da linha 4 para "root"
* Foi criado um banco de dados com o nome de "chalange-lavel-2-nv-1".
* Foi inserido os dados de script.sql dentro no novo banco de dados.
* O valor da varialvel $banco da linha 5 foi alterado para "chalange-lavel-2-nv-1" 
* Foi alterado o atributo port= da linha 8 de port=9999 para port=8889 

### Voltando para o index.php
* Foi colocado os dados retornados da query dentro de uma variavel $dados 
* A variavel $dados foi estruturada em uma mini estrutura html  da seguinte forma:  
*               <p><?=$dados->id?></p>
*               <h2><?=$dados->name?></h2>
*               <h3><?=$dados->log?></h3>
 *              <h4><?=$dados->datetime?></h4>
