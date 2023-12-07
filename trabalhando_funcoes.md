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




