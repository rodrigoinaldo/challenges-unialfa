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
