# Explorando Operadores

## 1 - Operadores e Expressões

Os operadores ajudam a escrever expressões nos softwares que, por sua vez, ajudam a manipular os dados armazenados. 

### Operadores Aritméticos
Para realizar cáculos
| Operador | Descrição |Exemplo |
|------|---------|--------|
|+|Adição|``` let result = 5 + 3; ```|
|-|Subtração|``` let result = 8 - 5;  ```|
|*|Multiplicação|``` let result = 6 * 8; ```|
|/|Divisão|``` let result = 22 / 2; ```|
|%|Módulo (resto da dicisão)|``` let result = 25 % 3; ```|
 
### Operadores Relacionais
Verifica a relação de algum valor com outro

| Operador | Descrição |Exemplo |
|------|---------|--------|
|==|Igual a|``` let isEqual = (x == y); ```|
|!=|Diferente de |``` let isNotEqual = (x != y);  ```|
|>|Maior que|``` let isGreater = (x > y); ```|
|<|Menor que|``` let isLess = (x < y); ```|
|>=|Maior ou igual a|``` let isGreaterOrEqual = (x >= y); ```|
|<=|Menor ou igual a|``` let isLessOrEqual = (x <= y); ```|

### Operadores Lógicos
Realiza condições lógicas

| Operador | Descrição |Exemplo |
|------|---------|--------|
|&&|AND lógico|```if (condition1 && condition2```|
|!|NOT lógico|```if (!condition!) ``` |


|| - OR lógico - ``` if (condition1 || condition2)```

### Operadores de Atribuição
(servem para quando vai guardar um valor em uma variável)

| Operador | Descrição |Exemplo |
|------|---------|--------|
|=|Atribuição|``` let x = 5; ```|
|+=|Adição e atribuição|``` let num = 10; num +=2; ```|
|-=|Subtração e atribuição|``` let num = 10; num -=3; ```|
|*=|Multiplicação e atibuição|``` let num = 5; num *= 4; ```|
|/=|Divisão e atibuição|``` let num = 10'num /= 2; ```|
|%=|Módulo e atribuição|``` let num = 10; num %= 3; ```|

### Operadores de Incremento e Decremento

| Operador | Descrição |Exemplo |
|------|---------|--------|
|++|Incremento|``` let counter = 0; counter++;```|
|--|Decremento|``` let counter = 5; counter--; ```|

**obs**: esses operadores se mantêm na maioria das linguagens de programação.

## 2 - Trabalhando com Operadores Aritméticos


**Exemplo 1 - apenas com números:**

```
// declarando variável
let idade = 19

// mensagem de saída
console.log(idade)

// fazendo uma operação de soma
idade = 30 + 6

// mensagem de saída
console.log(idade)

// fazendo uma operação de subtração
idade = 30 - 6

// mensagem de saída
console.log(idade)
```

**Exemplo 2 - Números e variáveis:**

 ```
// declarando variável
let codigoProduto = 1034

// fazendo a conta ao mesmo tempo em que mostra na tela
console.log(codigoProduto - 1000)
console.log(codigoProduto + 1000)
console.log(codigoProduto * 1000)
console.log(codigoProduto / 1000)
console.log(codigoProduto % 1000)
 ```

**Exemplo 3 - Cáculo na variável:**

 ```
// declarando variáveis
let precoProduto = 200.50
let valorComTaxa = precoProduto * 3.14

//obs: na programação se usa o ponto para definir um número com vírgula

// mensagem de saída com o valor
console.log(valorComTaxa)

 ```

**Exemplo 4 - Entre variáveis:**

 ```
// declarando variáveis
let primeiroNumero = 1054
let segundoNumero = 250

// fazendo a conta ao mesmo tempo em que mostra na tela
console.log(primeiroNumero + segundoNumero)
console.log(primeiroNumero - segundoNumero)
console.log(primeiroNumero * segundoNumero)
console.log(primeiroNumero / segundoNumero)
console.log(primeiroNumero % segundoNumero)
 ```
 
**Exemplo 5 - Entre variáveis 2.0:**

 ```
// declarando variáveis
let multiplicador = 5
let multiplicando = 45
let produto = multiplicador * multiplicando

// mensagem de saída
console.log("O resultado da multiplicação é " + produto)

// alterando variável
multiplicador = multiplicador + 20
// OU multiplicador += 20, esse é um operador de atribuição
// conferindo se somou
console.log(multiplicador)

// refazendo a conta pois o programa lê de forma sequêncial
produto = multiplicador * multiplicando

// mensagem de saída
console.log("O novo resultado da multiplicação é " + produto)
 ```

**Exemplo 6 - Incremento e Decremento:**

 ```
// declarando variáveis
let contador = 1

// '++' incremento

contador++
contador++

console.log(contador)

// '--' decremento

contador--

console.log(contador) 
 ```

**Exemplo 7 - Escopo**

```
// declarando variáveis

let conta = 3 * ((5 + 3) / 2)

// mensagem de saída
console.log(conta)
```

## 3 - Operadores de Comparação/Relacionais

**Comparam duas coisas para ver se é verdade ou não:**

```
let numero = "1"
console.log(numero == 1)
// vai dar como true

console.log(numero ==+ 1)
// vai dar como false 

// = é atribuição
// == é para comparar o valor
// === é para comparar o valor e o formato do conteúdo, forma mais segura

let marca = "Motorola"
console.log(marca !== "Motorola")

// !== é como se perguntasse: é diferente? 

// posso também guardar o resultado de uma expresão em uma variável como TRUE ou FALSE
let modelo = "S 20"
let resultado = modelo !== "S 20 FE"

console.log(resultado)
// ao comparar textos, ele tem que estar 100% igual para dar true, inclusive letras minusculas e maiusculas 
```
**Exemplo prático de um registro com cpf bloqueado:**
```
let cpfBloqueado = "123.445.222-45"
let cpfUsuario = "222.111.222-09"
let ehCPFBloqueado = cpfUsuario === cpfBloqueado

console.log("O usuário está barrado? " + ehCPFBloqueado)
```

**Exemplo para utilizar maior e menor que:**
```
let idadeMinima = 18
let idadeUsuario = 17
let idadePermitidaValida = idadeUsuario >= idade Minima
sonsole.log(idadePermitidaValida)

let idadeDeCorte = 50
idadeUsuario = 45
let resultadoEhTerceiraIdade = idadeDeCorte <= idadeUsuario
console.log(resultadoEhTerceiraIdade)
```

## 4 - Operadores Lógicos

Servem para realizar perguntas complexas/duplas

### AND (&&) - exemplo para ir viajar

```
let idade = 18
let vistoVerificado = true
let resultado = (idade >=18) && (vistoVerificado === true)
console.log(resultado)

// se idade fosse 17 o resultado seria false pois nesse caso ambas as condições devem ser verdadeiras para que o resultado seja true
```

### OR (||) 
Exemplo onde o boneco só pode sair se não estiver chovendo OU se estiver com um guarda chuva:

```
let tempo = "Sol"
let item = "guarda chuva"
let podeSair = (tempo !== "Chuva") || (item === "guarda chuva")

console.log("Nosso personagem pode sair? " + podeSair)

// nesse caso apenas uma das condições precisa ser verdadeira para dar true, apenas se ambas forem falsas ele dará falso

```

### NOT (!)
Ele nega uma afirmação - exemplo para verificar se o tempo é de chuva

```
let tempo = "Chuva"
let resultado = tempo !== "Chuva"

console.log(resultado)

// ou
 
tempo = "Chuva"
resultado = tempo === "Chuva"

console.log(!resultado)
// ele inverte o boolean na hora de exibir

// ou

tempo = "chuva"
let horario = 8

let resultado = !((tempo !== "chuva") && (horario > 6))
console.log(resultado)
```