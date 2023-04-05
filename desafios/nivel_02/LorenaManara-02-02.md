<?php

    $pessoas = array(

    "Lorena" => "20",

    "Raphael" => "22",

    "Gabre" => "25"

);

$fp = fopen('pessoas.csv', 'w');

$header = array('Nome', 'Idade');
fputcsv($fp, $header);

foreach ($pessoas as $nome =>$idade) {
    $linha = array($nome, $idade);
    fputcsv($fp, $linha);

}
  
fclose($fp);

?>