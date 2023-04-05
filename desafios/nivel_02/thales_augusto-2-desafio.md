### Itens Feitos

*Primeiro criei um array com 6 registros.

*Depois criei a variável $arquivo para poder abrir o arquivo, usando a função fopen('file.csv', 'w').

*Para escrever o conteúdo no arquivo usei foreach e depois a função fputcsv.

*Para fechar o arquivo tive que usar fclose().

*Fiz também um cabeçalho. Antes do array fiz uma variável chamada $cabecalho, que também é um array, ordenei as colunas dos arrays. Depois lá embaixo antes de escrever o conteúdo no arquivo, usei o fputcsv novamente para fazer o cabeçalho.


*<?php

*$cabecalho = ["Nome", "Ano", "Distribuidora"];

*$array = [
    ["Nome" => "Rei Leao", "Ano" => "1994", "Distribuidora" => "Disney", ],
    ["Nome" => "Aladin", "Ano" => "1992", "Distribuidora" => "Disney", ],
    ["Nome" => "Gato de Botas 2", "Ano" => "2022", "Distribuidora" => "DreamWorks", ],
    ["Nome" => "Mulan", "Ano" => "1998", "Distribuidora" => "Disney", ],
    ["Nome" => "Como Treinar o seu Dragão", "Ano" => "2010", "Distribuidora" => "DreamWorks", ],
    ["Nome" => "Shrek", "Ano" => "2001","Distribuidora" => "DreamWorks",],
];

*$arquivo = fopen('file.csv', 'w');

*fputcsv($arquivo, $cabecalho, ';');

*foreach($array as $row_array) {
    fputcsv($arquivo, $row_array, ';');
}

*fclose($arquivo);