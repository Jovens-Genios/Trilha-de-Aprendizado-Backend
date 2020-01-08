# Projeto 1 - MyFavoriteMovies

**Objetivo**: Criar uma aplicação web fullstack onde o usuário consiga ver uma lista de filmes e marcar seus favoritos.

![projeto 1](../imagens/backend-projeto1.png?raw=true)  

### Descrição

Neste primeiro projeto você desenvolverá seus primeiros superpoderes no mundo back-end web. Sua missão é desenvolver uma aplicação web completa onde o usuário consiga ver uma lista de filmes e marcar seus favoritos. Você precisará de um front-end simples (pode usar Vue.js + Vuetify, para ficar com visual mais bem acabado) e uma API no back-end utilizando Laravel.

Ações importantes que o usuário deve ser capaz de fazer:

*   Ver listas de filmes;
*   Pesquisar um filme específico;
*   Adicionar um filme como favorito;
*   Visualizar sua lista de filmes favoritos;
*   Criar conta;
*   "Logar" na sua conta (não precisa de autenticação, basta colocar seu email)
*   Deletar sua conta;

Para isso, sua aplicação deverá conter:

*   Uma interface web front-end para interação do usuário;
*   API REST com Laravel para conexão com bancos de dados MySQL;
*   Utilize o ORM do Laravel (Eloquent) para modelar as relações entre as entidades no banco de dados;

### Instruções

Uma recomendação forte é que você siga o seguinte fluxo de criação do projeto:

1.  Criação da interface front-end com dados dummy (View);
2.  Modelagem do banco de dados, quais relações entre entidades e quais seus atributos (Model);
3.  Desenvolver o código back-end para a aplicação (Controller);

Outra recomendação, utilize o [Postman](https://www.getpostman.com/) para testar as rotas de sua API. Ele fornece ferramentas poderosas para seus testes.

Além disso, crie um repositório no Github para este projeto, com boa documentação. Se você ainda não sabe como utilizar o Git para fazer controle de versão no seu código, esta é uma boa [Introdução ao Git](https://blog.dankicode.com/introducao-ao-git-e-github/).

Para rodar seu projeto localmente, utilize a [infraestrutura em Docker neste repositório](/docker/Instruções.md).

### Dados sobre os filmes

Os dados sobre os filmes foram importados do [Kaggle no dataset "The Movies Dataset"](https://www.kaggle.com/rounakbanik/the-movies-dataset). Eles estão disponíveis na pasta [/dados/movies_metadata.csv](/dados/movies_metadata.csv) neste repositório. 

Você deve importá-los em sua tabela no MySQL (pelo PhpMyAdmin, é possível importar .csv). E não necessáriamente todas as colunas farão sentido para sua aplicação.

### Onde buscar conhecimento

Lembrando sempre, um bom desenvolvedor não é quem já sabe de tudo e sim quem sabe procurar o que precisa. Se está travado em algum ponto, busque a solução na internet! 

Recomendações de onde buscar conhecimento:

*   [REST API concepts and examples](https://www.youtube.com/watch?v=7YcW25PHnAA)
*   [Sua Primeira API REST com Laravel](https://www.youtube.com/watch?v=oVRWQJE5a1c)
*   [Normalização em Bancos de Dados](https://medium.com/@diegobmachado/normaliza%C3%A7%C3%A3o-em-banco-de-dados-5647cdf84a12)
*   [Database Relationships (Part 1 of 3) - Data Normalization](https://www.youtube.com/watch?v=oexOYUUyQik)
*   [Database Relationships (Part 2 of 3) - One-to-Many Relationships](https://www.youtube.com/watch?v=IstAk982ntA)
*   [Database Relationships (Part 3 of 3) - Many-to-Many Relationships](https://www.youtube.com/watch?v=7D8u6Lb2BKU)
*   [Documentação Laravel](https://laravel.com/docs/6.x)


