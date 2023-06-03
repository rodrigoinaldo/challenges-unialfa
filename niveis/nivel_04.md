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