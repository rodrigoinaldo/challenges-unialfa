#### Apenas o arquivo modelo de exemplo.

~~~php

index.php{

<!DOCTYPE html>
<html lang="en">
 <head>
 <meta charset="UTF-8">
 <meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Planilha</title>
 </head>
  <body>
   <a href="planilha.php">Gerar nova planilha</a>
 </body>
  </html>
 }

planilha.php{
    <?php
$armas = array(
  '0' => array('id' => 1, 'nome' => "M1 Garand",  "calibre" => ".30"),
  '1' => array ('id' => 2,    "nome" => "m16", "calibre" => "5.56",),
  '2' => array('id' => 3,       "nome" => "9mm", "calibre" => "9mm",)
 ); 
 $out = fopen("index.xls", 'w');
 foreach ($clientes as $cliente)
 {
   fputcsv($out, $cliente,"\t", '"');
 }
 fclose($out);

 ?>
 <h1>Planilha Criada, verifique seus arquivos</h1>
 }
~~~