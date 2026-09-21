# games-shop-PRJ
Projeto de web page de uma loja de jogos utilizando HTML e CSS, com o objetivo de aplicar conceitos de design responsivo, incluindo a utilização de Flexbox para criar um layout flexível e adaptável.

## 1 - Header (cabeçalho)
### Objetivos:
- Compreender os elementos principais que compõem o cabeçalho de um site, incluindo o logotipo da loja, o menu de navegação e seus respectivos links; aplicar estilos CSS para criar um cabeçalho visualmente atraente e funcional;
- Compreender os conceitos básicos de layout usando Flexbox.

### Etapas:
#### Criação do header (HTML):

```HTML
<!--`html:5` para criar a estrutura básica do projeto-->

<!DOCTYPE html>

<html lang="pt-br"><!--alteração da linguagem para "pt-br"-->

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Games Shop - A sua loja de games</title><!--alteração do título da aba da página-->

    <link rel="stylesheet" href="./main.css"/>

</head>

<body>

    <header>

        <div class="container"><!--`.container` para controle geral do header-->

            <h1>Games Shop</h1>

        <nav><!--elemento semântico informando que o conteúdo são links de navegação-->

            <ul><!--lista não ordenada-->

                <li><!--item da lista-->

                    <a href="#">Sobre a loja</a>

                </li>

                <li><!--item da lista-->

                    <a href="#">Contato</a>

                </li>

            </ul>

        </nav>

        </div>

    </header>

</body>

</html>
```
#### Estilização do header (CSS):
```CSS
/*removendo estilos padrão*/

* {

    margin: 0; /*removendo espaço externo padrão*/

    padding: 0; /*removendo espaço interno padrão*/

    box-sizing: border-box; /*removendo cálculo padrão*/

}

/*alteração do cabeçalho*/

header {

    padding: 16px 0;

    background-color: #182C61;

    color: #ecf0f1

}

/*alteração das listas de navegação*/

header nav li {

    display: inline; /*links lado a lado*/

    margin-left: 16px; /*margem esquerda para afastar os links*/

    font-size: 24px; /*aumenta o tamanho da fonte dos links*/

}

/*alteração da cor das listas de navegação*/

header nav li a{

    color: #ecf0f1; /*a cor só pode ser alterada na ancora <a>*/

    text-decoration: none; /*retira o sublinhado*/

}

/*criação de container para controlar o conteudo do header*/

.container {

    max-width: 1280px;

    width: 100%; /*estilo vai ocupar 100% da largura até chegar em 1288px*/

    margin: 0 auto; /*centraliza o texto com aumento da tela automaticamente*/

}

header .container {

    display:flex; /*coloca os links ao lado do título da página*/

    align-items: center; /*centraliza os links em relação a altura do título da página*/

    justify-content: space-between; /*coloca espaço máximo entre titulo e links*/

}
```


## 2 - About (sobre)
### Objetivos:
- Compreender a importância de criar seções bem estruturadas em uma página da web e como usar as tags semânticas HTML para definir a estrutura do conteúdo;
- Posicionar imagens e texto lado a lado, aplicar margens e espaçamentos para obter o espaçamento desejado entre os elementos e usar propriedades de fonte para estilizar o texto;
- Aprender a criar classes e IDs para segmentar elementos específicos no HTML e aplicar estilos apenas a esses elementos.

### Etapas:
#### Criação do about e importação de fontes (HTML):

```HTML
<!--código abaixo adicionado ao <head>-->

<!--importando as fontes Bungee e Lato-->

    <link rel="preconnect" href="https://fonts.googleapis.com">

    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

    <link href="https://fonts.googleapis.com/css2?family=Bungee&family=Lato:ital,wght@0,100;0,300;0,400;0,700;0,900;1,100;1,300;1,400;1,700;1,900&display=swap" rel="stylesheet">

<!--fim do código adicionado ao <head>-->

<!--código abaixo adicionado ao <body>-->

<!--criação da seção about/sobre-->
    <section>

        <div class="container">

            <img class="store-front" src="./Images/loja.jpg" alt="Fachada da loja Games Shop" />

            <div>

                <h2>Sobre a loja</h2><!--criação do about-->

                <p>

                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore ut veniam,
                    distinctio dolor eaque earum repudiandae voluptatibus iure quas blanditiis atque
                    molestias odit quibusdam ipsum vel aliquam? Quisquam, optio blanditiis.

                </p>

                <p>

                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore ut veniam,
                    distinctio dolor eaque earum repudiandae voluptatibus iure quas blanditiis atque
                    molestias odit quibusdam ipsum vel aliquam? Quisquam, optio blanditiis.

                </p>

                <ul class="brands-list"><!--criação da lista de logotipos das marcas-->

                    <li><img src="./Images/nintendo.png" alt="Logo Nintendo" /></li>

                    <li><img src="./Images/playstation.png" alt="Logo Playstation" /></li>

                    <li><img src="./Images/xbox.png" alt="Logo Xbox" /></li>

                </ul>

            </div>

        </div>

    </section>

<!--fim do código adicionado ao <body>-->
```
#### Estilização do about (CSS):

```CSS
/*início das adições/modificações do CSS*/

/*controle do tamanho dos logos das marcas*/

.brands-list img {

    height: 24px;

}

.brands-list li {

    display: inline; /*colocando as imagens dos logos das marcas lado a lado*/

    margin-right: 8px; /*espaçamento entre as imagens*/

}

/*controle do conteúdo do about*/

section .container {

    display: flex;

    align-items: flex-start; /* ajusta para o topo o texto em relação a altura do título da página*/

    justify-content: space-between;

}

/*adicionando espaçamento e cor padrão na section*/

section {

    padding: 24px 0;

    color: #182C61;

}

/*adicionando margem baixa no about*/

section h2 {

    margin-bottom: 16px;

}

/*adicionando margem baixa no parágrafo*/

section p {

    margin-bottom: 8px;

}

/*adicionando margem direita na imagem da loja*/

.store-front {

     margin-right: 32px;

}

/*regras para a fonte Bungee*/

.bungee-regular {

  font-family: "Bungee", sans-serif;

  font-weight: 400;

  font-style: normal;

}

/*regras para a fonte Lato*/

.lato-regular {

  font-family: "Lato", sans-serif;

  font-weight: 400;

  font-style: normal;

}

/*utilizando a fonte Bungee nos headers e h2*/

header,

section h2 {

    font-family: 'Bungee', cursive;

}

/*utilizando a fonte Lato no restante do corpo da página*/

body {

    font-family: 'Lato', sans-serif;

}

/*removendo o font-weigth padrão do navegador (bold)*/

header h1,

section h2 {

    font-weight: normal;

}

/*fim das adições/modificações do CSS*/
```
