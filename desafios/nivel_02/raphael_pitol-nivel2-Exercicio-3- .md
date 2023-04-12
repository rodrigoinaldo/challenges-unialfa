## Resolução Desafio 2 Exercicio 3
==================

*Segue Resolução do desafio sodium
**Fiz de 3 formas diferentes**.

### 1ª Forma

*Traz um resultado hexadecimal*
```php

$mensagem = 'Raphael Pitol Juliani';
$encriptado = sodium_bin2hex($mensagem);

echo $encriptado;
echo '<br>';

$decriptado = sodium_hex2bin($encriptado);
echo '<br>';

 echo $decriptado;
 ?>
```
 ### 2ª Forma
 ```php
 $key = random_bytes(SODIUM_CRYPTO_SECRETBOX_KEYBYTES);
$nonce = random_bytes(SODIUM_CRYPTO_SECRETBOX_NONCEBYTES);
const mensagem = "Consegui usar o Sodium para criptografar";
$senha = sodium_crypto_secretbox(mensagem, $nonce, $key);
$encriptado = sodium_bin2hex($senha);
echo '<br>';
echo $encriptado;
echo '<br>';

$conteudosenha = sodium_crypto_secretbox_open($senha, $nonce, $key);

echo '<br>';
echo $conteudosenha;
?>
```
 ### 3ª Forma
 ```php
 $mensagem = " <=Raphael Pitol Juliani=> ";
$cipher = "AES-256-CBC";
$secret = "1234567890123456789012";
$options = 0;
$iv = str_repeat ("0", openssl_cipher_iv_length($cipher));

$encryptedString = openssl_encrypt($mensagem, $cipher, $secret, $options, $iv);

echo $encryptedString;
echo '<br>';


$decryptedString = openssl_decrypt($encryptedString, $cipher, $secret, $options, $iv);


echo $decryptedString;
?>
```