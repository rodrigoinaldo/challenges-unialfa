# Lista de desafios

1. Criar no Laravel um projeto de encurtador de links
2. O Objetivo é desenvolver uma api que recebe 2 pokemons e que eles possam batalhar e mostrar o resultado de quem venceu, abaixod orientacoes importantes para este exercicio:
    1. Esse projeto deverá ser uma API
    2. No arquivo api.php criar uma rota que recebe na url os dois pokemons, por ex.: /battle/{poke1}/{poke2}
    3. Essa rota deve enviar a request para a controller BattleController, no método show.
    4. Dentro do método show, deverá consumir a API https://pokeapi.co/api/v2/pokemon/ (GET) passando o nome de cada pokemon.
    5. Essa pokeapi retorna informacoes do pokemon.
    6. Após obter a resposta contendo os dados do pokemon, considere usar o campo **base_stat** como valor de atack que o pokemon tem.
    7. Após obter o valor de atack dos 2 pokemons, crie uma lógica que compare qual é o pokemon que tem maior valor de atack e retorne o vencedor.
    8. [feature] Após finalizar, adicionar também para gravar um log das batalhas em um arquivo.
3. Crie em seu github um novo repositório chamado desafio-unialfa-nivel04-ex3
    1. Realize o Clone do repositório
    2. Abra o repositório clonado no VsCode
    3. Desenvolva uma API que consuma a seguinte API: https://api.punkapi.com/v2/beers
    4. Ao obter o retorno dos dados, salve em um arquivo csv (Excel).
    5. Após realizar a gravacao, retorno a resposta em formato JSON informando que os dados foram gravados com sucesso.
    6. Desenvolva uma API que realize o Download do arquivo Excel.
        1. O endpoint vai buscar o arquivo excel gravado e retornar a opcao de download para salvarmos em algum diretório fora do projeto.
        2. Realize o commit e push para o repositório. Para responder este exercicio coloque o link do seu repositório em um arquivo .md enviando na sessao de respostas.
4. Crie em seu github um novo repositório chamado desafio-unialfa-nivel04-ex4
    1. Realize o Clone do repositório
    2. Abra o repositório clonado no VsCode
    3. Instale no projeto usando o composer a seguinte lib: **composer require openai-php/laravel**
        OBS: Repositório da lib: https://github.com/openai-php/laravel
    4. É necessário criar uma conta na plataforma openIA, para obter as credenciais: https://platform.openai.com/
    5. Desenvolver uma API com o endpoint **/chat**
    6. Enviar para a openIA através da lib que foi instalada o prompt passando alguma mensagem do que você quer
    7. Ao obter a reposta, guarde em um arquivo de LOG.
5. Clonar o repositório a seguir e resolver os bugs https://github.com/alexmpereira/php-xdebug
    OBS: Como resposta ao desafio, crie um arquivo markdown e coloque as soluções e explicando.
6. Clonar o repositório a seguir realizar a refatoração de boas práticas https://github.com/alexmpereira/good-coding-practices
    OBS: Como resposta ao desafio, crie um arquivo markdown e coloque as soluções e explicando.
7. Referente a **DDD**, seguir o passo a passo abaixo para a conclusão do desafio:
    1. Criar um repositório no **GitHub** chamado **desafio07_nivel04**
    2. Clonar localmente o repositório
        - OBS: Para cada task concluida, faça o commit. 
    3. Criar o **composer.json** inicial e configurar o **autoload** da **psr-4** defindo um namespace padrão para a src.
    4. Criar na raiz do projeto o **index.php** para testar as classes. Além disso, carregue o auload para facilitar os imports das classes da src.
    5. Criar a pasta **src** onde ficará os **modulos** e a camada de **dominio** para cada módulo. Por Exemplo: **Financeiro/Domain/Entity**
    6. Na src, desenvolver o módulo que vai representar a parte **Academica**. Como requisito para esse exercicio deve conter a classe **Aluno** como entidade de dominio.
        1. Coloque as seguintes propriedades: **nome, idade, cpf**
        2. Adicione as seguintes regras: **O nome pode conter no minimo 5 caracteres, idade acima de 18 e cpf com 11 digitos.**
    7. Na src, desenvolver o módulo que vai representar a **Contabilidade**. Como requisito para esse exericicio deve conter a classe **Cliente** como entidade de dominio.
        - **OBS: Para o pessoal de contabilidade, o Aluno é um Cliente.**
        1. Coloque as seguintes propriedades iniciais: **nome, idade, cpf, boletosEmAtraso, boletos**
        2. Adicione as seguintes regras dentro do dominio: **O nome pode conter no minimo 5 caracteres, idade acima de 18 e cpf com 11 digitos, buscar todos os boletos em atraso, na propriedade boletos trazer todos os boletos.**
    8. Na src, desenvolver o módulo que vai representar a parte **Financeira**. Como requisito para esse exericicio deve conter a classe **Cliente** como entidade de dominio.
        1. Implemente nessa entidade os seguintes atributos: **nome, idade, cpf, datamatricula**
        2. Adicione as seguintes regras dentro do dominio: **O nome pode conter no minimo 5 caracteres, idade acima de 18 e cpf com 11 digitos, datamatricula não pode ser vazio**
    9. Nosso sistema evoluiu conforme o tempo e agora foi solicitado pelo negocio adicionar uma nova **feature**. Quando o cliente completar 2 anos de matricula, adicionar para esse cliente **10% de desconto** nos boletos. Como sugestão, pode conter na classe um método que dispara para gerar o boleto, recebendo o cpf, valor. Antes de disparar para gerar o boleto devem chamar um método que será capaz de verificar a matricula e caso tenha mais que 2 anos adicione o desconto no valor, em seguida envie o novo valor na funcionalidade de gerar o boleto.
    10. Faça o commit de cada tarefa e como resposta, em um markdown coloque o repositório.
