# Resolução do desafio 1 do nível 3

### Primeiramene criei a seguinte classe: 
~~~php
class Produto {
    public $nome;
    public $descricao;
    public $preco;

    function __construct($nome, $descricao, $preco)
    {
        $this->nome = $nome;
        $this->preco = $preco;
        $this->descricao = $descricao;   
    }

}
~~~

### Em seguida instânciei essas classes e depois atribui valor as propriedades nome.

~~~php
$mouse = new Produto();
$mouse->nome = "Mouse Gamer";

$teclado = new Produto();
$teclado->nome = "Teclado Gamer";

~~~

### Agora é só mosstrar no console o nome de cada produto

~~~php

print_r("*********************************************************** \n");
print_r("* ");
print_r("TABELINHA DE VENDAS \n");
print_r("* ");
print_r("$mouse->nome \n");
print_r("* ");
print_r("$teclado->nome \n");
print_r("***********************************************************");
~~~

### roda o código pfv prof, ta mó bonitinho no terminal ;-;.