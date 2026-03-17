
---

#  4. passo-3-carrinho.md

```md id="r4"
#  Passo 3 - Lógica do Carrinho

##  Objetivo
Gerenciar os produtos adicionados.

##  Funcionalidades
- Adicionar item
- Remover item
- Atualizar quantidade
- Calcular total

##  Código

Arquivo: src/cart.js

```js
let cart = [];

function addItem(product, quantity = 1) {
    const existingItem = cart.find(item => item.product.name === product.name);

    if (existingItem) {
        existingItem.quantity += quantity;
    } else {
        cart.push({ product, quantity });
    }
}

function getTotal() {
    return cart.reduce((total, item) => {
        return total + item.product.price * item.quantity;
    }, 0);
}

module.exports = {
    addItem,
    getTotal
};
