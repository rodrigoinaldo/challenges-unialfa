# Lista de desafios

1. Crie uma classe PHP de Produto, adicione dentro dessa classe as seguintes propriedades: nome, descricao, preco. Crie 2 objetos instanciando a classe Produto e imprima o nome dos dois objetos.
2. Pegue como continuacao a classe do exercicio 01 desse nível, adicione um construtor para a classe Produto. Esse construtor deve receber os valores nome, descricao e preco no momento que for instanciar para um novo objeto. Além disso, ajuste as propriedades para que elas nao fiquem publicas, devem ficar como privadas.
3. Pegue como continuacao a classe do exercicio 02 desse nível, crie os métodos Getters e Setters das propriedades nome, descricao e preco. No setter do nome certifique-se que sempre a primeira letra seja maiúscula.
4. Em dupla crie um github adicionando o seu parceiro como membro. Os dois em suas máquinas devem clonar o repositório, realizar modificações e subir no repositório essas modificações. Os dois devem dar git pull dessas modificações para terem os mesmos códigos em suas máquinas.
5. Para que serve os comandos: **docker images**, **docker ps -a**, **docker run ...**, **docker exec ...**
    Escreva em um arquivo .md e envie como resposta.
6. Realizar o exercicio do site oficial do docker para criar um ambiente de container de uma aplicação: https://docs.docker.com/get-started/02_our_app/
7. Faça o próximo exercicio do site oficial do docker para quando ocorrer alterações no código da aplicação, atualizar o container: https://docs.docker.com/get-started/03_updating_app/
8. Faça o exercicio do site oficial do docker para subir no Docker Hub a imagem criada: https://docs.docker.com/get-started/04_sharing_app/
9. Crie um container Docker a partir da imagem "hello-world" e o execute para verificar se o Docker está configurado corretamente.
10. Escreva em um arquivo Dockerfile uma imagem personalizada que execute um servidor web (nginx) que exiba "Hello, Docker" na porta 80
11. Crie e execute um container a partir da imagem "nginx" e publique a porta 80 do container para a porta 8080 do host