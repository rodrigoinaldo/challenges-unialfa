###Criando arquivo Excel pelo php

* Primeiro criei um arquivo .php, logo apos criei um arquivo, utilizando a funcao FOPEN

* atraves do foreach, percorremos o array, escrevendo as linhas csv


~~~php
<?php

// Cabeçalho do csv
$headers = ['Produto', 'Preço'];

$dados = [
    [
        'produto' => 'Notebook',
        'preco' => 3587,
    ],
    [
        'produto' => 'Celular',
        'preco' => 2643,
    ],
    [
        'produto' => 'TV',
        'preco' => 5876,
    ],
    [
        'produto' => 'Fone',
        'preco' => 432,
    ],
];

$arquivo = fopen('file.csv', 'w');

// Criar do cabeçalho
fputcsv($arquivo , $headers);

foreach ($dados as $linha ) {
    fputcsv($arquivo, $linha);
}

fclose($arquivo);

?>
~~~