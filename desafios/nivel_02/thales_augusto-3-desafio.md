### Itens Feitos

*Bom no arquivo encriptar.php criei a variável $chave e coloquei a função sodium_crypto_aead_chacha20poly1305_ietf_keygen(), criei uma $senha, fiz uma variável $numero coloquei as funções random_bytes(SODIUM_CRYPTO_AEAD_CHACHA20POLY1305_IETF_NPUBBYTES), logo depois fiz a variável $encriptar com a função sodium_crypto_aead_chacha20poly1305_ietf_encrypt() com as outras variáveis dentro e pra finalizar fiz um echo base64_encode() com a variável anterior.

*Já no descriptar.php fiz uma require do encriptar.php criei a variável $descriptar e dessa vez usei a função sodium_crypto_aead_chacha20poly1305_ietf_decrypt() e coloquei as variáveis $encriptar, $numero(2 vezes) e $chave e no final coloquei um echo com a variável principal.

#### Dentro do encriptar.php:

~~~php
<?php

    $chave = sodium_crypto_aead_chacha20poly1305_ietf_keygen();

    $senha = 'Santos';

    $numero = random_bytes(SODIUM_CRYPTO_AEAD_CHACHA20POLY1305_IETF_NPUBBYTES);

    $encriptar = sodium_crypto_aead_chacha20poly1305_ietf_encrypt($senha, $numero, $numero, $chave);

    echo base64_encode($encriptar);

?>
~~~

#### Dentro do descriptar.php

~~~php
<?php
   require "encriptar.php";

   $descriptar = sodium_crypto_aead_chacha20poly1305_ietf_decrypt($encriptar, $numero, $numero, $chave);

   echo $descriptar;
?>
~~~~