# Desafio 3

### programa de funcionamento simples e intuitivo que cryptografa em código de 256 bits, funciona com 3 arquivos 
* encript.php
* decript.php
* data.php

### data.php é um arquivo que contem dados que são de uso comum para o restante dos arquivos, nele comtem a palavra que será cryptografada, a chave da cryptografia, a indentifiação da cyptografia e o "burlamento" de almuas palavras para não serem cryptografadas.

####  Estruturado da seguinte forma:

~~~php
    $palavra = "João gabriel grande";   
    $key = random_bytes(SODIUM_CRYPTO_AEAD_AES256GCM_KEYBYTES);
    $nonce = random_bytes(SODIUM_CRYPTO_AEAD_AES256GCM_NPUBBYTES);
    $additional_data = "";
~~~
* $palavra é a string para a cryptografia
* $key recebe uma chave de cryptografia 256 bits aleatoria
* $nonce recebe um indentificador 256 bits aleatório
* $additional_data recebe vazio pois não queremos "burlar" nenhuma palavra

### Indo para encript.php  aqui é executado a cryptoria da aplicação, utilizando o método sodium_crypto_aead_aes256gcm_encrypt() e passando como parámetro as variaveis de data.php.

~~~php
    <?php
    require"./data.php";
    echo"texto criptografato<br/>";
    $encriptString = sodium_crypto_aead_aes256gcm_encrypt($palavra,$additional_data, $nonce, $key) ;
    print_r($encriptString);
~~~

### indo para decript.php, aqui será descryptografado os dados, recebendo as variaveis de data.php e a variavel $encriptString de encript.php  será utilizado o método sodium_crypto_aead_aes256gcm_decrypt() passando esses dados como parametro.

~~~php
    < ?php
    require"./data.php";
    require"./encript.php";

    echo"<br/>Descriptografado com sucesso! <br/>";

    $stringDescript = sodium_crypto_aead_aes256gcm_decrypt($encriptString, $additional_data, $nonce, $key);
    echo $stringDescript;
~~~