#  Passo 2 - Criando Produtos

##  Objetivo
Criar uma função para representar produtos.

##  Conceito
Um produto precisa ter:
- Nome
- Preço

##  Código

Arquivo: src/product.js

```js
function createProduct(name, price) {
    return {
        name,
        price
    };
}

module.exports = createProduct;
