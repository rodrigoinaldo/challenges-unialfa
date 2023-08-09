<?php
//variavel dados recebe um array com nomes de cigarros
$dados = [
        'MALBORO',
        'DERBY',
        'CAMEL',  
        
];
//variavel arquivo recebe um arquivo tipo csv em modo de writing
$arquivo = fopen('cigarros.csv', 'w');
    // ele percorre o array dentro da variavel dados que recebe um apelido de row_dados
    foreach($dados as $row_dados){
    //ele escreve as informacoes contidas em arquivo
        fputcsv($arquivo, [$row_dados], ';');
    }
    // fecha o arquivo
    fclose($arquivo);

    ?>