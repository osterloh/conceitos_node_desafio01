<h2 align="center"><a href="https://rocketseat.com.br/" target="_blank" style="text-decoration: none">
    <img alt="Bootacmp GoStack" src="https://camo.githubusercontent.com/0a35fb0a0add717a1556200218530580cca84bfd7a0e8c3f5c28fc72e02cd3fb/68747470733a2f2f73746f726167652e676f6f676c65617069732e636f6d2f676f6c64656e2d77696e642f626f6f7463616d702d676f737461636b2f6865616465722d6465736166696f732d6e65772e706e67" width="50%"/>
    <br>
    Desafio 01 do Bootcamp GoStack
    <br>
    Introdução ao nodeJS
</a></h2>

<center>
  <img alt="GIF projeto" src="assets/desafio01.gif" width="50%">
</center>

## Descrição

- Este projeto foi desenvolvido com a finalidade de cumprir o desafio 01 do Bootacamp GoStack da [Rocketseat](https://rocketseat.com.br/), utilizando o <strong>[nodeJS](https://nodejs.org/)</strong> para fins de capacitação pessoal.
- A finalidade desse projeto é para cadastrar os Repositórios com as Tecnologias de um DEV, atualizar os dados cadastrados, possibilidade de deltar esses dados e cadastrar Likes para esse repositório com as tecnologias desse dev.

## Etapas

- Para cumprir o desafio foram utilizadas e configuradas as rotas http GET, POST, PUT e DELETE.

```bash
* GET: Buscar informações do back-end;
* POST: Criar uma informação no back-end;
* PUT/PATCH: Alterar uma informação no back-end;
* DELETE: Deletar uma informação no back-end;
```

- Para cadastrar um repositório foi utilizado o método http POST para a rota "/repositories", passando como requisição body os seguintes dados em formato de json:

```js
{
  title, url, techs;
}
```

- Para listar os dados cadastrados foi utilizado o método http GET para a rota "/repositories".

- Para atualizar alguma informação cadastrada foi utilizado o método http PUT na rota "/repositories/:id", passando uma requisição de parâmetro o ID do repositório, caso o ID informado não seja encontrado é retornado um status code 400. Para atualizar os dados é realizado uma requisição body com os seguintes dados em formato de json:

```js
{
  title, url, techs;
}
```

- Para deletar algum dado cadastrato é utilizado o método http DELETE para a rota "/repositories/:id", passando como ma requisição de parâmetro o ID do repositório. Caso o ID informado não seja encontrado é retornado um status code 400 e caso o ID corresponda com algum cadastrado, as informações referente aquele ID serão deletadas e será retornado um status code 204.

- Para cadastrar Likes para o repositório é utilizado o método http POST para a rota "/repositories/:id/like", passando como ma requisição de parâmetro o ID do repositório. Caso o ID informado não seja encontrado é retornado um status code 400 e caso o ID corresponda com algum cadastrado será soma 1 like para aquele repositório.

## Tecnologias

- [nodeJS](https://nodejs.org/)
- [yarn](https://yarnpkg.com/)
- [express](https://github.com/expressjs/express)
- [nodemon](https://github.com/remy/nodemon)
- [uuidv4](https://github.com/thenativeweb/uuidv4)

---

Desenvolvido por [Johnatan Luiz Osterloh](https://www.linkedin.com/in/johnatanosterloh/)
