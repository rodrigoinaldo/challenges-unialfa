#### 1) Faltava adicionar um ";" no final do: 

public function setModel($model) {
        $this->model = $model; 
    }

#### 2) Faltava o metodo "age"

/** 
- add private age

public function setAge($age) { // add function age
        $this->age = $age;
    }

    public function getAge() { // add function age
        return $this->age;
    }
*/

#### 3) faltava adicionar o metodo:

    public function multiply($a, $b) { 
       return $a * $b; 
    }

#### 4) Faltava substituir o int pelo float

public function divide($a, $b): float { 
        return $a / $b;
    }

#### 5) Adicionar o metodo:

   public function getBalance() { 
         return $this->balance;
    }

#### 6) No caso o:

class StringUtils {
    public static function concatenate($str1, $str2) {
        return $str1 . $str2;
    }
}

estava passando dois metodos,

e no: echo StringUtils::concatenate("Hello", "world"); 

estava só com o "Hello"

#### 7) O problema está na variavel $minimumValue -> com voce podendo alterar o valor dele, o ideal seria tornar uma classe privada