#### Gerando arquivo excel com PHP

* Aqui eu criei 3 arrays com as informações das pessoas, dentro de outro array 

~~~php
$dados = array(
    array('João', 25, 'joao@email.com'),
    array('Maria', 30, 'maria@email.com'),
    array('José', 40, 'jose@email.com')
);
~~~

* Essa parte está definindo o tipo e o nome do arquivo

~~~php
// aqui está dando o nome do arquivo excel
$arquivo = 'Teste4.xls';

// aqui está definindo o tipo de arquivo que vai ser enviado
header('Content-Type: application/vnd.ms-excel');
// aqui define o nome do arquivo na hora em que for baixado
header('Content-Disposition: attachment;filename="' . $arquivo . '"');
~~~

* Essa parte vai imprimir os dados nas células

~~~php
// esse foreach está fazendo as linhas, no momento em que um dos 3 arrays termina, ele pula para a próxima
foreach ($dados as $linha) {
    // esse foreach está fazendo as colunas, no momento em que imprime um dado, ele vai para a próxima célula
    foreach ($linha as $celula) {
        echo $celula . "\t";
    }
    echo "\n";
}
~~~
