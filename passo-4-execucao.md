
---

#  5. passo-4-execucao.md

```md id="r5"
#  Passo 4 - Executando o Sistema

##  Objetivo
Testar o funcionamento do carrinho

##  Código

Arquivo: src/index.js

```js
const createProduct = require('./product');
const cart = require('./cart');

const produto1 = createProduct("Camiseta", 50);

cart.addItem(produto1, 2);

console.log(cart.getTotal());
