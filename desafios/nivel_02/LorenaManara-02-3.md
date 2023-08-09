~~~php
<?php
    // Gerando uma chave criptografada
    $key = random_bytes(SODIUM_CRYPTO_SECRETBOX_KEYBYTES);

    // Criando um número único para a critografia
    $nonce = random_bytes(SODIUM_CRYPTO_SECRETBOX_NONCEBYTES);

    // Usando a chave para criptografar a informação
    $mensagemCifrada = sodium_crypto_secretbox('ola.', $nonce, $key);
    
    // comverntendo binario pra exa decimal
    $menssagem = sodium_bin2hex($mensagemCifrada);

    $mcifrada = "menssagem criptografada" . $menssagem;

    echo $mcifrada;

    $conteudo = sodium_crypto_secretbox_open($mensagemCifrada, $nonce, $key);
    if ($conteudo === false)
    {
        var_dump("ERRO");
    }
    echo $conteudo;

?>
~~~