*Desafio 2 

~~~php
<?php

// Cabeçalho do csv
$headers = ['Produto', 'Preço'];

$dados = [
    [
        'produto' => 'Celular',
        'preco' => 2000,
    ],
    [
        'produto' => 'Televisao Smart',
        'preco' => 5000,
    ],
    [
        'produto' => 'Fone JBL sem fio',
        'preco' => 200,
    ],
    [
        'produto' => 'Mouse Dragon',
     'preco' => 250,
    ],
];
~~~

~~~php
// Criar o cabeçalho
$arquivo = fopen('file.csv', 'w');

fputcsv($arquivo , $headers);

foreach ($dados as $linha) {
    fputcsv($arquivo, $linha);
}

fclose($arquivo);

?>
~~~