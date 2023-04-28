### Resolução nivel 2, desafio 2.

* Foi inserido o segundo codigo:

<?php

    $export_data = array(
    array('id' => 1, 'nome' => 'Teste 1'),
    array('id' => 2, 'nome' => 'Teste 2'),
    array('id' => 3, 'nome' => 'Teste 3'),
    array('id' => 1, 'nome' => 'Teste 1'),
    array('id' => 2, 'nome' => 'Teste 2'),
    array('id' => 3, 'nome' => 'Teste 3')
    );

    $fileName = "export_data" . rand(1,100) . '.xls';

    if ($export_data) {
        function filterData(&$str) {
            $str = preg_replace("/\t/", "\\t", $str);
            $str = preg_replace("/\r?\n/", "\\n", $str);
            if(strstr($str, '"')) $str = '"' . str_replace('"', '""', $str) . '"';
        }
        // headers for download
        header("Content-Type: application/vnd.ms-excel");
        header("Content-Disposition: attachment; filename=\"$fileName\"");

        $flag = false;
        foreach($export_data as $row) {
            if(!$flag) {
                // display column names as first row
                echo implode("\t", array_keys($row)) . "\n";
                $flag = true;
            }
            // filter data
            array_walk($row, 'filterData');
            echo implode("\t", array_values($row)) . "\n";
        }
        exit;            
    }   

  ?>
