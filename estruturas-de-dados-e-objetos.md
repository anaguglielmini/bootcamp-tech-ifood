# Estruturas de Dados e Objetos

## Estrutura de Dados JSON

É um agrupamento de dados mais organizada. Como se fosse uma caixinha onde serão guardados os dados e transportados de um lugar para outro. 

Maneira de transferir dados de um lugar para outro de forma agrupada e fácil.

JSON - JavaScript Object Notation.

Anotação de objetos em JavaScript mas de forma universal para todas as linguagens de programação.

**Exemplo sem JSON:**
```
let name = "Felipe"
let age = 28
let products = ["mouse 2xwm", "teclado mecânico", "monitor"]
let productsValues = [29.90 , 129.99 , 899.99]

generateInvoice(name, age, products, productsValues)

function generateInvoice(name, age, products, productsValues){
    console.log("O comprador é " + name)
    console.log("A sua idade é " + age)
    console.log("O produto é " + products[0])
    console.log("O valor é " + productsValues[0])
}
```

**Exemplo com JSON:**

```
// declarando JSON
// posso declarar chaves e valores dentro do JSON
// a chave é o identificador dos valores
// name é chave e Felipe é o valor
let invoice = {
    name: "Ana",
    age: 19,
    products: {
        0: ["mouse razer", 29.90],
        1: ["teclado mecânico", 129.90],
        2: ["monitor", 899.99]
    }    
}
generateInvoice(invoice)

function generateInvoice(invoiceProducts){
    console.log(`O comprador é ${invoiceProducts.name}`)
    console.log(`A sua idade é ${invoiceProducts.age}`)

// for especifico para chamar todos os valores da lista
    for(let index in invoice.products){
        let [productName, productPrice] = invoice.products[index]
        console.log(`- ${productName}: R$ ${productPrice}`)
    }
}
```

## O que são Classes e Objetos