```php
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <?php
    $key = sodium_crypto_aead_chacha20poly1305_ietf_keygen();

    //criptografar
    $texto = 'Baahh é os guri'; 

    $nonce = random_bytes(SODIUM_CRYPTO_AEAD_CHACHA20POLY1305_IETF_NPUBBYTES);

    $encrypted = sodium_crypto_aead_chacha20poly1305_ietf_encrypt($texto, $nonce, $nonce, $key);

    echo sodium_bin2hex($encrypted) ;

    //discriptografar
    $decrypted = sodium_crypto_aead_chacha20poly1305_ietf_decrypt($encrypted, $nonce, $nonce, $key);


    echo "</br> $decrypted";
    ?>
    ´´´
```
</body>

</html>
´´´