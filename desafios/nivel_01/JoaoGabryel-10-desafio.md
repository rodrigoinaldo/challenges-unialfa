## João Gabryel
## Código CSS e JavaScript
<!DOCTYPE html>
<html lang="pt-br">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=[device-width], initial-scale=1.0">
    <title>Formulário</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-9ndCyUaIbzAi2FUVXJi0CjmCapSmO7SnpJef0486qhLnuZ2cdeRhO02iuK6FUUVM" crossorigin="anonymous">
    <script scr="script.js"></script>
</head>

<body>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-geWF76RCwLtnZ8qwWowPQNguL3RmwHVBC9FhGdlKrxdiJJigb/j/68SIy3Te4Bkz"
        crossorigin="anonymous"></script>
    <div class="container ">
        <form id="form">
            <div class="row">
                <div class="col-6">
                    <label for="exampleFormControlInput1" class="form-label">Seu nome</label>
                    <input type="text" class="form-control" id="nome" placeholder="Digite seu nome">
                </div>


                <div class="col-6">
                    <label for="exampleFormControlInput1" class="form-label">Seu Email</label>
                    <input type="email" class="form-control" id="exampleFormControlInput1"
                        placeholder="name@example.com">
                </div>

            </div>
            <div class="row">

                <div class="col-12">
                    <label for="exampleFormControlTextarea1" class="form-label">Descreva sobre você</label>
                    <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
                </div>

            </div>
            <div class="row">
                <div class="col">
                    <label for="exampleFormControlTextarea1" class="form-label">Data de Nascimento</label>
                    <input type="date" class="form-control" id="exampleFormControlInput1">
                </div>
                <div class="col">
                    <label for="exampleColorInput" class="form-label">Sua cor favorita</label>
                    <input type="color" class="form-control form-control-color" id="exampleColorInput" value="#563d7c"
                        title="Choose your color">

                </div>

                <div class="col">
                    <div class="mb-3">
                        <label for="formFile" class="form-label">Defina um Avatar</label>
                        <input class="form-control" type="file" id="formFile">
                    </div>
                </div>
                <div class="col">
                    <label for="inputPassword5" class="form-label">Digite uma senha</label>
                    <input type="password" id="inputPassword5" class="form-control" aria-labelledby="passwordHelpBlock">
                    <div id="passwordHelpBlock" class="form-text">
                        Sua senha deve ter de 8 a 20 caracteres, conter letras e números e não deve conter espaços,
                        carcteres especiais ou emoji.
                    </div>

                </div>
            </div>
            <div class="col">
                <button class="btn btn-success" type="submit">Enviar</button>
            </div>
        </form>

    </div>

<script src="script.js"></script>
</body>

</html>


const form = document.getElementById('form');
form.addEventListener('submit', function (event) {
    event.preventDefault();
    const nome = document.getElementById('nome').value;
    const email = document.getElementById('exampleFormControlInput1').value;
    const descricao = document.getElementById('exampleFormControlTextarea1').value;
    const dataNascimento = document.getElementById('exampleFormControlInput1').value;
    const corFavorita = document.getElementById('exampleColorInput').value;
    const senha = document.getElementById('inputPassword5').value;
    console.log('Nome: ' + nome);
    console.log('Email: ' + email);
    console.log('Descrição: ' + descricao);
    console.log('Data de Nascimento: ' + dataNascimento);
    console.log('Cor Favorita: ' + corFavorita);
    console.log('Senha: ' + senha);
}
);


