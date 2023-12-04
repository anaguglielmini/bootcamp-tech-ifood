
# Dominando Estruturas de Controle

## 1 - Trabalhando com Estruturas Condicionais (if, else if, else)

### Condicionais com If

- Iremos utilizar o [w3schools](https://www.w3schools.com/tryit/trycompiler.asp?filename=demo_nodejs) pois não tem limite de linhas; 
- São blocos de códigos que apenas serão executados se forem verdadeiros.

**Exemplo 1:**
```
let ehLigado = false

// como é booleano e definido como falso, não irá executar pois tudo o que está dentro dos parênteses do IF tem que ser igual a true para executar
if(ehLigado){
	console.log("executou comando")
}

ehLigado = true
if(ehLigado){
	console.log("Agora ele executa o comando")
}
```

**Exemplo 2:**

```
let possuiOvos = false
let itensComprados = ""

if(possuiOvos){
 itensComprados = "Leite"
}

console.log("Item comprado: " + itensComprados)
// retornará apenas "Item comprado: ", pois o valor possuiOvos é false então ele não realiza um novo registro em itensComprados

possuiOvos = true

if(possuiOvos){
 itensComprados = "Leite"
}

console.log("Item comprado: " + itensComprados)
```

### Condicionais com Else

- Não é obrigatótio ter o Else em todo if mas todo else tem que ter um if;
- Se o if der como falso ele executa o else idependemente da condição.

```
let possuiOvos = false
let itensComprados = ""

if(possuiOvos){
 itensComprados = "Leite"
}
else{
 console.log("Não tinha ovos e passou na sessão de congelados")
 itensComprados = "Lasanha Congelada"
}
console.log("Item comprado: " + itensComprados)
```

### Condicionais com Else If

- IF encadeado, junto com outro if;
- Faz uma segunda pergunta se o primeiro if der como falso.

```
let nivelDeFome = 0

if(nivelDeFome <= 1){
 console.log("Pouca fome")
}else if(nivelDeFome === 2){
 console.log("Muita fome")
}else{
 console.log("Comeria um boi")
}
```

## 2 - Trabalhando com Estruturas de Decisão (estrutura Switch Case)

- Switch case & Break default;
- Recomendado para quando se tem muitas situações para tratar.

### Switch  Case

```
let fruta = "Banana"


// leva em consideração o que está dentro da variável fruta
switch (fruta){
	case "Laranja": 
	console.log("Suco de Laranja")

	case "Banana":
	console.log("Vitamina de banana"

	case "Maçã":
	console.log("Suco de maçã")	
// irá retornar tanto "Vitamina de banana" quato "Suco de maçã" pois o valor de fruta é banana, então ele executa tudo o que vier depois 
}
```

### Break

Encerra o bloco do case caso de como verdadeiro:

```

let fruta = "Banana"

switch (fruta){
	case "Laranja": 
	console.log("Suco de Laranja")
	break 

	case "Banana":
	console.log("Vitamina de banana"
	break

	case "Maçã":
	console.log("Suco de maçã")	
	break
}
```

### Default

Mensagem para quando o valor que está sendo utilizado nos cases for diferente de todos:

```
let fruta = "Abacaxi"

switch (fruta){
	case "Laranja": 
	console.log("Suco de Laranja")
	break 

	case "Banana":
	console.log("Vitamina de banana"
	break

	case "Maçã":
	console.log("Suco de maçã")	
	break

	default:
	console.log("suco genérico")
}
```

## Outra possibilidade com Switch Case

**Pode colocar mais de um case para uma ação:**

```
let fruta = "Maçã"

switch (fruta){
	case "Laranja": 
    case "Maçã":
	console.log("Suco de " + fruta)
	break 

	case "Banana":
	case "Morango":
	console.log("Vitamina de " + fruta)
	break

	default:
	console.log("suco genérico")
}
```

**Com números:**

```
let fruta = 3

switch (fruta){
	case 1: 
   	case 2:
	console.log("Suco de laranja")
	console.log("Suco de maçã")
	break 

	case 3:
	case 4:
	console.log("Vitamina de banana")
	console.log("Vitamina de morango")
	break

	default:
	console.log("suco genérico")
}
```

## 3 - Trabalhando com Estruturas de Repetição (for, while, do-while)

