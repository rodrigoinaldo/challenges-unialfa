# Resolução do desafio 2 do nível 3

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

### Com 3 atributos publicos e um construtor que obriga prencher os 3 atributos na instanciação da classe.

### Em seguida instânciei essas classes.

~~~php
$mouse = new Produto("Mouse Gamer", "Mouse de jogar jogos", 100);

$teclado = new Produto("Teclado Gamer", "Teclado para programar melhor", 200);

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