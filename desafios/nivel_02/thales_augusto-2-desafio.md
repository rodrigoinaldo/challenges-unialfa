### Itens Feitos

*Primeiro criei um array com 6 registros.

*Depois criei a variável $arquivo para poder abrir o arquivo, usando a função fopen('file.csv', 'w').

*Para escrever o conteúdo no arquivo usei foreach e depois a função fputcsv.

*Para fechar o arquivo tive que usar fclose().

*Fiz também um cabeçalho. Antes do array fiz uma variável chamada $cabecalho, que também é um array,
*ordenei as colunas dos arrays. Depois lá embaixo antes de escrever o conteúdo no arquivo, usei o
*fputcsv novamente para fazer o cabeçalho.