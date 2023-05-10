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