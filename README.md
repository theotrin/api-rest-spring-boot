# API REST com Java e Spring Boot
Este documento descreve a API REST desenvolvida com Spring Boot. A API fornece endpoints para CRUD (Create, Read, Update, Delete) de entidades e outras operações específicas do seu projeto.

## Tecnologias Utilizadas
- Java 17
- Spring Boot
- Spring Data JPA
- Lombok

# Rotas:

### Cadastrar um produto novo

#### `POST` `/products`

#### Exemplo de resposta

```javascript
// HTTP Status 201
{
    "id": 752,
    "name": "Iphone 15 pro max",
    "price": 1500000,
    "description": "Iphone de ultima geração com os componentes mais atualizados do mercado"
}

```


### Listar todos os produtos

#### `GET` `/products`

#### Exemplo de resposta

```javascript
// HTTP Status 200 / 201 / 204
// 2 contas encontradas
[
    {
        "id": 1,
        "name": "Iphone 15 pro max",
        "price": 1500000,
        "description": "Iphone de ultima geração com os componentes mais atualizados do mercado"
    },
    {
        "id": 2,
        "name": "Macbook Air M1",
        "price": 12500,
        "description": "notebook poderoso e com bateria de longa duração"
    }
]

```

### Listar um produto especifico

#### `GET` `/products/01`

#### Exemplo de resposta

```javascript
// HTTP Status 200 / 201 / 204
// 2 contas encontradas

{
    "id": 252,
    "name": "Macbook Air M1",
    "price": 12500,
    "description": "notebook poderoso e com bateria de longa duração"
}
```

#### Resposta caso o ID não seja encontrado no banco de dados
```javascript
/// HTTP Status 404

{
    "message": "Produto não encontrado :/"
}
```


### Deletar um produto

#### `DELETE` `/products/02`

#### Exemplo de resposta

```javascript
// HTTP Status 204



```

#### Resposta caso o ID não seja encontrado no banco de dados
```javascript
/// HTTP Status 404

{
    "message": "Produto não encontrado :/"
}
```

### Atualizar um produto do banco de dados

#### `PUT` `/products/02`

#### Exemplo de resposta

```javascript
// HTTP Status 204



```

#### Resposta caso o ID não seja encontrado no banco de dados
```javascript
/// HTTP Status 404

{
    "message": "Produto não encontrado :/"
}
```

