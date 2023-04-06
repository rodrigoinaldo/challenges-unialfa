### código do desafio
#### <?php


#### $clientes = array(
####    '0' => array('id' => 1, 'nome' => "Caio",'idade' => 19),
####    '1' => array ('id' => 2, 'nome' => "Zé",'idade' => 80),
####    '2' => array('id' => 3, 'nome' => "Tonho",'idade' => 59)
#### );//neste array é passado os dados do cliente


#### $out = fopen("index.xls", 'w');//fopen abre o arquivo excel
#### foreach ($clientes as $cliente)
#### {
####    fputcsv($out, $cliente,"\t", '"');//fputs () é uma função embutida que é usada para escrever em um arquivo aberto.
#### }
#### fclose($out);//Fecha um ponteiro de arquivo aberto


#### ?>