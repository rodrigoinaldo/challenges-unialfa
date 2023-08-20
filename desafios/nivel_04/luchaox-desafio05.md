# php-xdebug
how to use xdebug in a application php

<br>

## Erro 01: Erro de sintaxe

O erro estava presente na linha 11, onde estava um fechamento de chave "}".

A solução do erro foi inserir o ";" no final da linha 10, resolvendo assim o erro.

~~~php
return $this->model;
~~~


<br>

## Erro 02: Propriedade Indefinida

O erro estava presente na linha 14, onde uma propriedade estava indefinida.

~~~php
return $this->"age";
~~~

Para solucionar o erro, precisou ser criada a propriedade **private $age;**

~~~php
<?php 
class Person {
    private $name;
    private $age;
~~~
<br>

## Erro 03: Método Indefinido

O erro estava presente na linha 13, onde o *"multiply"* era um método indefinido.

~~~php
echo $calculator->"multiply"(2, 3);
~~~

Para resolver o erro, foi necessário criar a função para o método:

~~~php
public function multiply($a, $b) {
        return $a * $b;
    }
~~~
<br>

## Erro 04: Tipo de Retorno

O erro é que o método **divide()** retorna o valor do tipo **int**, mas a divisão dos números resultará em um valor de ponto float.

~~~php
public function divide($a, $b): int {
    return $a / $b;
}
~~~
Para o erro ser resolvido, é preciso ajustar o tipo de retorno para **float** ou **number** para refletir o tipo de valor que a função realmente retorna

~~~php
public function divide($a, $b): float {
    return $a / $b;
}
~~~

ou

~~~php
public function divide($a, $b): number {
    return $a / $b;
}
~~~

<br>

## Erro 05: Propriedade Privada

O erro estava presente na propriedade no echo que tenta acessar a propriedade **$balance** na classe *BankAccount*, que estava definida como privada **('private')**

~~~php
$account = new BankAccount();
$account->deposit(100);
$account->withdraw(50);
echo $account->balance; 
~~~

Para resolver este erro, é preciso criar um método público dentro da classe.

~~~php
public function getBalance() {
        return $this->balance;
    }
~~~

Agora ao invés de acessar o **$account->balance** é utilizado o método **getBalance()**.

<br>

## Erro 06: Retornando uma de duas strings

O erro estava presente na linha 8 do código, onde estava passando apenas uma string, porém o código requeria duas.

~~~php
echo StringUtils::concatenate("Hello");
~~~

Para resolver o erro, foi inserida a segunda string solicitada.

~~~php
echo StringUtils::concatenate("Hello", "World");
~~~


<br>


## Erro 07: Valor sendo alterado após verificação

O erro era que na função **$minimumValue** está sendo alterado após a verificação da condição, o que pode afetar o cálculo do desconto.

~~~php
<?php 
class DiscountCalculator {
    public function calculateDiscount($amount) {
        $minimumValue = 10;
~~~

Para não se ter problemas futuros, o melhor é evitar a alteração do valor minimo após a verificação da condição.

~~~php
<?php 
class DiscountCalculator {
    public function calculateDiscount($amount) {
        $minimumValue = 10;

        if ($amount > $minimumValue) {
            $discount = $amount * 0.1;
        } else {
            $discount = $amount * 0.05;
        }
        
        return $discount;
    }
}
?>
~~~