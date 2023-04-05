### Resolução Nivel 2 Desafio 2

*Criei um array ->cabeçalho com "id","nome","e-mail","endereco".
*Criei outro array ->nomes com "id","nome","e-mail","endereco" referenciando os dados para o cabeçalho.

*Depois criei uma variavel ->arquivo que recebe como valor a função fopen('file.csv', 'w'); que abre o arquivo excel
*Depois chamei a função fputcsv que formata a variavel arquivo e inserio cabeçalho.
*Fiz um foreach com o Array nomes jogando para cada linha os dados usando a função fputcsv.

<?php

$cabecalho = array("id","nome","e-mail","endereco");

$nomes =[
    ['id'=> '1',
    'nome'=> 'Raphael',
    'email'=> 'raphael@com.br',
    'endereco'=> 'Rua da saudade'
    ],
    ['id'=> '2',
    'nome'=> 'joao',
    'email'=> 'joao@com.br',
    'endereco'=> 'Rua da a'
    ],
    ['id'=> '3',
    'nome'=> 'Pedro',
    'email'=> 'pedro@com.br',
    'endereco'=> 'Rua da b'
    ],
    ['id'=> '4',
    'nome'=> 'Joana',
    'email'=> 'joan@com.br',
    'endereco'=> 'Rua da c'
    ],
    ['id'=> '5',
    'nome'=> 'Raphael',
    'email'=> 'raphael@com.br',
    'endereco'=> 'Rua da saudade'
    ],
    ['id'=> '6',
    'nome'=> 'joao',
    'email'=> 'joao@com.br',
    'endereco'=> 'Rua da a'
    ],
    ['id'=> '7',
    'nome'=> 'Pedro',
    'email'=> 'pedro@com.br',
    'endereco'=> 'Rua da b'
    ],
    ['id'=> '8',
    'nome'=> 'Joana',
    'email'=> 'joan@com.br',
    'endereco'=> 'Rua da c'
    ],
    ['id'=> '9',
    'nome'=> 'Raphael',
    'email'=> 'raphael@com.br',
    'endereco'=> 'Rua da saudade'
    ],
    ['id'=> '10',
    'nome'=> 'joao',
    'email'=> 'joao@com.br',
    'endereco'=> 'Rua da a'
    ],
    ['id'=> '11',
    'nome'=> 'Pedro',
    'email'=> 'pedro@com.br',
    'endereco'=> 'Rua da b'
    ],
    ['id'=> '12',
    'nome'=> 'Joana',
    'email'=> 'joan@com.br',
    'endereco'=> 'Rua da c'
    ],
];

$arquivo = fopen('file.csv', 'w');

fputcsv($arquivo, $cabecalho, ';');

foreach($nomes as $row_nome){
    fputcsv($arquivo, $row_nome, ';');
}

fclose($arquivo);