# Desafio3

~~~php
<?php

// Gerando uma chave criptografada
$key = random_bytes(SODIUM_CRIPTO_SECRETBOX_KEYBYTES);
// Criando um numero unico para criptografia
$nonce = random_bytes(SODIUM-CRYPTO_SECRETBOX_NONCEBYTES);
// Usando a chave para criptografar a informaçao
$mensagemCifrada = solidum_cripto_secretbox('Luiz Henrique Assumpçao Sampaio', $nonce, $key);

$hex  sodium_bin2hex($mensagemCifrada);

$mCriptografada = "mensagem criptografada" . $hex ;

acho $mCriptografada;

$conteudo = sodium_crypto_secretbox_open($mensagemCifrada, $nonce, $key);
if ($conteudo === false)
{
    var_dump("ERRO");
}

$mDescriptografada = "\n Mensagem Descriptografada: " . $conteudo;

echo $mDescriptografada;
~~~