# Trabalhando com Funções

## 1 - o que são Funções e Como Criar

- Uma função é como uma fábrica, nós entregamos algo e ela devolve aquilo processado;
- Entrada, agente e saída, a função tem o papel de agente de mudança/ação;
- Uma função sempre tem uma ação no meio, podendo ou não ter uma entrada/saída;
- É como se guardasse uma parte do código em uma caixa para chamar depois quantas vezes quiser e com mais facilidade.
- Quando declara uma função: 
    - Não se nomeia ela com número no início;
    - Não coloca espaço no nome, usar sempre o padrão CamelCase;
    - Deixar o nome das funções com verbos, exemplos: enviarEmail(), salvarNoBD();
    - Deixar uma função para executar apenas uma ação, apenas um objetivo.

- Usar identação, usando tab e espaços para ficar visualmente mais organizado.

**Exemplo 1:**
```
// exemplo de uma torradeira

// chamando a função

inserirPao()
torrar()

// declarando a função
function torrar(){
    console.log("Torrando o pão")
}

function inserirPao(){
    console.log("Preparando para inserir o pão")
    console.log("Finalizado")
}
```
**Exemplo 2 (função dentro de função):**

```
// exemplo de uma torradeira

// chamando a função

inserirPao()


// declarando a função
function torrar(){
    console.log("Torrando o pão")
    console.log("Finalizado")
}

function inserirPao(){
    console.log("Preparando para inserir o pão")
    console.log("Finalizado")
    torrar()
}
```
**Exemplo 3:**
```
// chamando função que chama outras funções
main()

// declarando função que chama outras funções
function main(){
    getData()
    checkValues()
    sendToDataBase()
}

// declarando funções, o padrão é deixar os nomes das funções em inglês
function getData(){
    console.log("Pegando dados do usuário")
}

function checkValues(){
    console.log("Validando dados")
}

function sendToDataBase(){
    console.log("Cadastrando dados")
}
```

## 2 - Funções com Parâmetros

Passamos parâmetros quando queremos que uma função realize a mesma coisa com valores diferentes

**Exemplo:**
```
// chamando a função e declarando o valor da sua variável
torrar("pão de forma")
torrar("pão integral")

// criando função com um parâmetro
// essa variável pao apenas existe dentro da função
function torrar(pao){
	console.log("torrada feita com " + pao)
}
```


**Exemplo com mais de um parâmetro:** 
```
// chamando a função e declarando o valor da sua variável
torrar("pão de forma" , "Felipe")
// quando há um default e um valor definido fora, como aqui, ele dá prioridade para o nome de fora
torrar("pão integral" , "Ana")
// chamando função sem declarar um valor
torrar("pão puma")

// criando função com um parâmetro
// essa variável pao apenas existe dentro da função
// nome = "Cliente" é um valor default para quando não passarem esse valor
function torrar(pao, nome = "Cliente"){
	console.log("torrada feita com " + pao)
	console.log("ela é um pedido de " + nome)
}
```

**Observações:**
- Não podemos criar uma variável com let e chamar ela dentro de uma função
- O que podemos fazer é criar a variável com *var*, o var cria uma variável no código geral enquanto o let cria apenas em um escopo, mas não é muito recomendado
- Não conseguimos chamar uma variável parâmetro criada em uma função fora dela
- Quando há múltiplos parâmetros e você não passa um valor, no JavaScript ele coloca como undefined
- Quando houver mais de dois parâmetros e um deles for opcional de informar por fora, deixar ele por último: ``` function torrar(pao, valor, nome = "Cliente"){```
	- Mas caso ocorra, ao passar os valores por fora, deixar como undefined para chamar o valor default:
```
torrar("pão na chapa", undefined, "felipe")

function torrar(pao, valor = 50.25, nome){
	console.log("torrada feita com " + pao)
	console.log("ele é um pedido de " + nome)
	console.log("O valor total é de " + valor)
}
```

**Outro exemplo para apresentar a interpolação de strings:**
```
createStringConnection("db_products", "felipe", "9876")

function createStringConnection(databaseName, user, pass){
// interpolação de strings, substitui a utilização de + 
	console.log(`connect:DBCONNECT;user=${user};pass=${pass};initial_database=${databaseName}`)
}

```

## 3 - Funções com Retorno

- Algo que a função processa ou cria e que podemos utilizar fora dela;


```
// guardando o resultado do somatorio em uma variável por fora
let resultado = soma(5,3)

console.log("O resultado dessa função é " + resultado)

function soma(numA, numB){
	let somatorio = numA + numB
// return para retornar 
	return somatorio
}
```

- O return pode ser utilizado assim também: 

```
// guardando o resultado do somatorio em uma variável por fora
let resultado = soma(5,3)

console.log("O resultado dessa função é " + resultado)

function soma(numA, numB){
	return numA + numB
// não pode colocar pra retornar dois valores: return numA, numB
// apenas retorna um valor ou um vetor ou uma matriz
}
```

**Exemplo bem comum:**

```
let userName = getFirstName("Ana Luiza Migliavacca")

console.log("Seja bem vindo(a) " + userName)

// função para pegar o primeiro nome do cliente
function getFirstName(name){
	let firstName = name.split(" ")[0]
// split é uma função que já existe 
// serve para quebrar o nome de acordo com o que é passado
// e nesse caso será quando identificar espaço no nome
// depois de quebrar ele coloca em um vetor os valores quebrados do texto
	return firstName
}
```

**Exemplo diferente para uso do split:**

```
let userName = getFirstName("Ana Luiza Migliavacca", " ")

console.log("Seja bem vindo(a) " + userName)

userName = getFirstName("Matheus-Batista", "-")

console.log("Seja bem vindo(a) " + userName)

// função para pegar o primeiro nome do cliente
function getFirstName(name, splitChar){
// splitChar serve para declarar qual será o separador do nome no começo e não na função
	let firstName = name.split(splitChar)[0]

	return firstName
}
```




