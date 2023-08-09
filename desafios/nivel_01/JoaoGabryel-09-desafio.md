## João Gabryel
## Código HTML e CSS
<!DOCTYPE html>
<html lang="pt-br">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="style.css">
  <title>Document</title>
</head>

<body>
  <div class="container">
    <div class="header">
      <p>Header</p>
    </div>
    <div class="main">
      <p>Conteúdo</p>
    </div>
    <div class="sidebar">
      <p>Sidebar</p>
    </div>
    <div class="footer">
      <div class="item1">
        <p>Parte 1</p>
      </div>
      <div class="item2">
        <p>Parte 2</p>
      </div>
      <div class="item3">
        <p>Parte 3</p>
      </div>
    </div>
  </div>
</body>

</html>

body {
    margin: 0;
}

.container {
    display: grid;
    grid-template-areas: 'header header header header'
        'main main main sidebar'
        'footer footer footer footer ';
    grid-template-rows: auto;
}

p {
    text-align: center;
}

.header {
    grid-area: header;
    padding: 25px;
    background-color: orange;
}

.main {
    grid-area: main;
    padding: 200px;
    background-color: plum;
}

.sidebar {
    grid-area: sidebar;
    background-color: greenyellow;
}

.footer {
    grid-area: footer;
    display: flex;
    justify-content: space-evenly;


}

.item1 {
    background-color: rgb(206, 144, 144);
    width: 350px;

}

.item2 {
    background-color: rgb(241, 252, 143);
    padding-bottom: 40px;
    flex: 2;

}

.item3 {
    background-color: rgb(206, 144, 144);
    width: 350px;

}

@media screen and (max-width: 768px) {
    .container {
        grid-template-areas:
            'header'
            'main'
            'sidebar'
            'item1'
            'item2'
            'item3'
            'footer';
    }
    .footer {
        flex-direction: column;

    }
    .main{
        padding: 10px;
    }
    .item1{
        width: 100%;
    }
    .item2{
        
            width: 100%;
    
    }
    .item3{
        width: 100%;
    }
   
}

