## Carolina Aguera

### Exercício 5

1 - É o ponto e vírgula (;), que estava faltando.

2 - Faltava o método de atribuir a idade, faltava o private $age, e chamar o método para fazer o set da idade.

```
<?php
class Person
{
    private $name;
    private $age;

    public function setName(String $name)
    {
        $this->name = $name;
    }

    public function getName(): string
    {
        return $this->name;
    }

    public function setAge(Int $age)
    {
        $this->age = $age;
    }

    public function getAge(): int
    {
        return $this->age;
    }
}

$person = new Person();
$person->setName("John");
$person->setAge(20);
echo $person->getName();
echo $person->getAge();

```

3 - Faltava o método de multiplicar

```
public function multiply($a, $b)
    {
        return $a * $b;
    }
```

4 - O erro era o o tipo estava errado

```

 public function divide($a, $b): float

```

5 -  Criar um método publico getBalance que retorna o valor do balance e não pega diretamente

6 - Colocar uma outra palavra, como atributo na função

```
<?php
class StringUtils
{
    public static function concatenate($str1, $str2)
    {
        return $str1 . $str2;
    }
}

echo StringUtils::concatenate("Hello", "World");
```

7 - Criar uma constante para mudar global e não sair atribuindo novos valores para baixo

```
<?php
class DiscountCalculator
{
    const minimumValue = 10;

    public function calculateDiscount($amount, $minimumValue)
    {
        if ($amount > $minimumValue) {
            $discount = $amount * 0.1;
        } else {
            $discount = $amount * 0.05;
        }
        return $discount;
    }
}

$calculator = new DiscountCalculator();
echo $calculator->calculateDiscount(15, DiscountCalculator::minimumValue);
```
