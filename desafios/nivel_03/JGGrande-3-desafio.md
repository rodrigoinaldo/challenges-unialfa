# Resolução do desafio 3 do nivel 3

## Primeiramente implementei os getters and setters a classe ja existente. 

~~~php
class Produto {
    private $nome;
    private $descricao;
    private $preco;

    public function getNome(){
        return $this->nome;
    }
    public function getDescricao(){
        return $this->descricao;
    }
    public function getPreco(){
        return $this->preco;
    }

    public function setNome($nome){
        $this->nome = ucfirst($nome);
    }
    public function setDescricao($descricao){
        $this->descricao = ucfirst($descricao);
    }
    public function setPreco($preco){
        $this->preco = $preco;
    }

}
~~~

### Na sequencia instancios a classe porem agora usando o setter para atribuir os valores e sempre a primeira letra maiuscula.

~~~php
$mouse = new Produto();
$mouse->setNome("mouse Gameer");

$teclado = new Produto();
$teclado->setNome("Teclado Gamer");

~~~

### Por fim não menos importante, mostramos no console com getter.

~~~php
print_r("*********************************************************** \n");
print_r("* ");
print_r("TABELINHA DE VENDAS \n");
print_r("* ");
print_r("{$mouse->getNome()} \n");
print_r("* ");
print_r("{$teclado->getNome()} \n");
print_r("***********************************************************");
~~~