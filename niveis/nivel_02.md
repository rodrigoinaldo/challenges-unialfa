# Lista de desafios

1. Resolvendo problemas iniciais de configuracoes
   1. Clone o repositório a seguir dentro do htdocs do apache: https://github.com/alexmpereira/challenge-level-2-exercise01
   2. Com o MAMP ou XAMPP rodando, tente executar o projeto no navegador
   3. O Objetivo é listar no index o resultado do banco, resolvendo cada erro que encontrar.
   4. Para publicacao da resolucao, deve-se tirar um print da listagem do index.php e colocar como resposta na entrega do desafio.
2. Criar um arquivo PHP executável, ao ser chamado via terminal este arquivo, gere um arquivo excel listando os dados de um array.
3. Crie dois arquivos PHP executável um para encriptar e outro para descriptar textos usando a extensao Sodium do PHP.
   1. https://www.php.net/manual/pt_BR/book.sodium.php
4. Trabalhando com sessoes do PHP:
   1. **ATENCAO: A resposta desse desafio deverá conter o código dos dois arquivos, use o Markdown para estilizar e deixar fácil o entendimento do arquivo com as respostas.**
   2. Crie dois arquivos PHP:
      1. O primeiro deve conter um formulário com dois campos: login, password
         1. Ao se submeter no formulário, deve ser gravado na sessao do PHP esse login e password
      2. O segundo arquivo deve capturar da sessao o login e o password (se existir)
         1. Pode ser listado os valores com o print_r
5. Crie em seu github um novo repositório chamado desafio-unialfa-nivel02-ex5
    1. Realize o Clone do repositório em seu htdocs
    2. Abra o repositório clonado no VsCode
    3. O desafio: Criar um formulário HTML contendo os campos: nome, email, idade, hobbie. Ao clicar no botao de enviar o formulário envie os dados para o arquivo recupera-dados.php. Através do método POST
    4. No arquivo recupera-dados.php recupere esses dados vindos do formulário e crie validacoes nesses valores recebidos:
    5. O nome precisa ter no mínimo 6 caracteres. A idade precisa ser maior que 18, caso seja menor deve lancar uma mensagem de erro.
    6. Realize o commit e push para o repositório. Para responder este exercicio coloque o link do seu repositório em um arquivo .md enviando na sessao de respostas conforme foi feito em outros exercicios.
6. Crie um projeto no htdocs, dentro crie um arquivo banco-dados.php
    1. Dentro desse arquivo escreva o código necessário para se conectar no banco de dados. Considere se conectar em um database chamado ex6.
    2. Adicione o código feito no arquivo .md e envie como resposta de desafio conforme os outros exercicios.
7. Crie em seu github um novo repositório chamado desafio-unialfa-nivel02-ex7
    1. Realize o Clone do repositório em seu htdocs
    2. Abra o repositório clonado no VsCode
    3. O objeto é criar um arquivo pesquisa.php que consulte no banco de dados uma tabela chamada pesquisa e liste em uma tabela do html os dados que contém dentro dessa tabela.
    4. Os campos da tabela pode ser: regiao, descricao, status
8. Descreva em um arquivo .md qual a importancia do uso do bindParam e coloque um exemplo com base na explicacao que descrever.
9. Descreva em um arquivo .md para que serve os comandos ls, cd e cat dentro de um terminal (CMD, POWERSHELL, BASH).
10. Crie em seu github um novo repositório chamado desafio-unialfa-nivel02-ex10
    1. Realize o Clone do repositório em seu htdocs
    2. Abra o repositório clonado no VsCode
    3. Configure dentro do projeto o arquivo .htaccess
        1. Esse arquivo deve mapear sempre para o arquivo index.php
    4. Crie um arquivo index.php com a lógica para fazer as URLs dinamicas
    5. Crie um arquivo chamado contato.php e desenvolva uma página simples de formulário para contato.
    6. O Objetivo é chamar a url localhost:8888/desafio-unialfa-nivel02-ex10/contato e abrir a página corretamente sem precisar informar a extensao .php
11. Crie em seu github um novo repositório chamado desafio-unialfa-nivel02-ex11
    1. Realize o Clone do repositório em seu htdocs
    2. Abra o repositório clonado no VsCode
    3. Configure um arquivo capaz de se conectar no banco de dados, em um database com o nome de sua preferencia.
    4. Nessa database deve ter a tabela usuário com as colunas: nome, email, senha, descricao, idade
    5. Crie uma página login.php com bootstrap contendo os campos email e senha.
        1. Ao clicar em Logar, enviar os dados para o arquivo valida-login.php
    4. No arquivo valida-login.php deve-se verificar se o usuário existe na tabela usuario. Caso exista, grave os dados na sessao e redirecione para uma página home.php.
    5. Nessa página home.php deve conter um menu e no main deve carregar os dados do usuário na sessao.
    6. **OBS** A estilizacao do projeto etc fica a criatividade de cada um, desde que cumpra os requisitos principais citados.
12. [PHP básico] Crie uma variável que represente a idade. Crie uma variável que represente o endereço. Use o echo do PHP para imprimir a idade e o endereço com um texto complementar.
    OBS: Pode usar a função **readline()** para abrir um prompt de escritra no terminal. Nesse caso a execução do arquivo deve ser pelo terminal usando o comando **php arquivo.php**
13. [PHP básico] Crie um arquivo php chamado loops.php. Utilizando os loops do php **(while e for)** faça a impressão do número 1 a 15 com o **echo**.
    OBS: **WHILE**: quando não sabemos quando o loop se encerrará. Quando é uma decisão um pouco mais complexa.
        **FOR**: quando sabemos o momento de saída do loop. Normalmente, quando temos um caso de uso de variável contadora.
14. [PHP básico] Usando o código do exercício 13, escreva uma validação dentro do loop que pule on úmero 8.
    OBS: O número 8 não pode ser impresso, ele deve ser ignorado.
15. [PHP básico] Escreva um loop que imprima os números de 1 a 100 apenas os impares.
16. [PHP básico] Tabuadas - Escreva uma variável que representa o número do multiplicador que queremos da tabuada. Em seguida com o loop do PHP faça a multiplicação do 1 até o 10 de acordo com o multiplicador passado em variável.
17. [PHP básico] Calculo de IMC - Escreva o código necessário que pegue o peso e a altura e imprima se a pessoa está acima ou abaixo do peso.
    OBS: Pode usar a função readline() para capturar o texto digitado no terminal.
18. [PHP básico] Construir um algoritmo que leia 2 números e efetue a adição. Caso o valor somado seja maior que 20, este deverá ser apresentado somando-se a ele mais 8; caso o valor somado seja menor ou igual a 20, este deverá ser apresentado subtraindo-se 5.
19. [PHP básico] Ler um número inteiro entre 1 e 12 e escrever o mês correspondente. Caso o número seja fora desse intervalo, informar que não existe mês com este número.
20. [PHP básico] A biblioteca de uma universidade deseja fazer um algoritmo que leia o nome do livro que será emprestado, o tipo de usuário (professor ou aluno) e possa imprimir um recibo conforme mostrado a seguir. Considerar que o professor tem 10 dias para devolver o livro o aluno somente 3 dias.
21. [PHP básico] Crie um lista de contas correntes, contendo 4 contas bancárias. Em cada conta deve ter os seguintes dados: titular e saldo. Imprima em um echo os nomes dos titulares.