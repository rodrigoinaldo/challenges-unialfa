### Exercício 2

#### O programa funciona de modo simples, é criado um array que representa as tabelas de um arquivo Excel com uma estrutura simples, funciona como um vetor, o pirmeiro index do array principal é a linha o segundo indexe do arrary segundario é a coluna da tabela Excel, 
~~~php
$list = array(
    [ 'nome' , 'idade' ,'cargo' ],
    [ 'João' , 18 ,'Junior' ],
    [ 'Ellen' , 24 ,'estudante' ],
    [ 'Alex' , 30 ,'professor' ],
);
~~~
#### Em seguida criei o arquivo csv e armazenenei em uma váriavel $fp

~~~php
$fp = fopen('persons.csv', 'w');
~~~
#### Por ultimo inserimos os dados do array no csv 
~~~php
foreach($list as $campos){
    fputcsv($fp, $campos);
}
~~~

#### para evitar possivel estouro de memória fechamos o arquivo com flcose()
~~~php
fclose($fp);
~~~
