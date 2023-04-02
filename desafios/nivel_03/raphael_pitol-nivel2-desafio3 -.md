### Resolução Nivel 2 Desafio 2

*Criei um array ->cabeçalho com "id","nome","e-mail","endereco".
*Criei outro array ->nomes com "id","nome","e-mail","endereco" referenciando os dados para o cabeçalho.

*Depois criei uma variavel ->arquivo que recebe como valor a função fopen('file.csv', 'w'); que abre o arquivo excel
*Depois chamei a função fputcsv que formata a variavel arquivo e inserio cabeçalho.
*Fiz um foreach com o Array nomes jogando para cada linha os dados usando a função fputcsv.
