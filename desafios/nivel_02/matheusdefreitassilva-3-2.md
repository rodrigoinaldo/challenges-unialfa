<?php

// Gerando uma chave criptografada
$key = random_bytes(SODIUM_CRYPTO_SECRETBOX_KEYBYTES);
// Criando um número único para a critografia
$nonce = random_bytes(SODIUM_CRYPTO_SECRETBOX_NONCEBYTES);
// Usando a chave para criptografar a informação
$mensagemCifrada = sodium_crypto_secretbox('Matheus de Freitas Silva', $nonce, $key);

$hex = sodium_bin2hex($mensagemCifrada);

$mCriptografada = "Mensagem criptografada:" . $hex ;

echo $mCriptografada;

$conteudo = sodium_crypto_secretbox_open($mensagemCifrada, $nonce, $key);
if ($conteudo === false)
{
    var_dump("ERRO");
}

$mDescriptografada = "\n Mensagem Descriptografada: " . $conteudo;

echo $mDescriptografada;