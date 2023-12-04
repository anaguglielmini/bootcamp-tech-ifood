
# Introdução a Lógica de Programação

## 1 - Entendendo Algoritmos e Fluxogramas

### Algoritmos

- Passo a passo lógico do que deve ser executado para resolver um problema e a ordem dos fatores altera no produto;
- Primeiro precisa saber qual problema você está tentando resolver.

### Fluxogramas
- Representação visual de uma sequência de acções lógicas;
- Sempre tem um "balãozinho", uma elipse, de Inicio no topo e Fim embaixo de tudo;
- A entrada de dados no sistema é representada por um paralelogramo;
- Questionamentos de Sim e Não (Estrutura de Decisão) são representados por um losagulo;
- "Caixinha" (blocos) representam ações;
- Estrutura de Looping acontece quando há uma estrutura de decisão e, dependendo da resposta, ele retorna em algum passo anterior;
- Estrutura de saída é representada por um trapézio com a mensagem que o sistema deverá mostrar.

### Material de Apoio
- [Mapa de aventura](https://helpful-jump-17b.notion.site/Mapa-de-aventura-91f3e9bd923842149d4dba754dc65c07)

### Na Prática
- [Meu Fluxograma](https://www.tldraw.com/s/v2_c_JTicnQ9E9cQL59ehTGyPW?viewport=-1080%2C-158%2C3316%2C1580&page=page%3Apage)

## 2 - Estrutura de um Software e Seu Ambiente de Desenvolvimento

### Processos dentro da aplicação

Toda aplicação tem esses 3 momentos:

1 - Input: entrada de dados no aplicativo/sistema. Todo momento que tem a interação com o usuário;

2 - Process: processos de verficação e processamento desses dados. São verificações e ações para realizar o pedido do usuário;

3 - Output: saída dos dados processados. São comandos de saída, para retornar alguma coisa ou dar algum posicionamento ou mensagem para o usuário.

- Features: funcionalidades, coisas que o usuário pode fazer na aplicação. Há diversas em uma aplicação e cada uma possuí um algoritmo com Input, Process e Output;
- Esses conceitos permanecem iguais independemente da linguagem de programação.

###  IDE


- Integrated Development Environment ou Ambiente de desenvolvimento integrado;

- Ferramenta que ajuda a escrever o código de forma mais fácil e prática;
- IDE online: Playcode.io/javascript;
- Há várias IDEs, Eclipse (mais para java), PyCharm (python), VsCode (para uso geral de linguagens), jetbrains (java) etc;
- A IDE ajuda a entender as coisas do código com cores.

**Explorando a IDE:**
- Explorer: onde ficam todas as pastas e arquivos do seu projeto;
- Editor de código;
- Console: parte visual do que está sendo programado/escrito, as saídas, serve para ver tudo o que se executa;
- Arquivos com final .js são arquivos javascript;
- Arquivos com final .cs são arquivos C charp;
- Arquivos com final .py são arquivos python;
- Esse "final" é chamado de extensão.
- Vamos usar o JavaScript - muito utilizada e fácil de aprender;
- Todo projeto tem uma pasta chamada Source (src), tem o código fonte da aplicação;
- // para fazer um comentário.

**Dica**: faça o caminho de uma forma diferente durante a programação para aprender quais tipos de erro aparecem e como resolve-los.

## 3 - Trabalhando com Variáveis

### Variáveis

A variável é um valor que será inputado e guardado para ser utilizado depois.

Iremos usar o playcode.io/javascript para "codar" e a linguagem JavaScript.

Atividade:
- O objetivo é fazer uma mensagem de saída pedindo o nome do usuário e recebe-lo em seguida usando seu nome;
- Para mostrar algo na tela, utilizamos no começo console para indicar que aparecerá algo nele;
- Em seguida usamos o .log() que é um método, representa uma ação que será realizada com o console;
- Dentro do log colocaremos "" e dentro dessas aspas duplas colocamos o texto a ser exibido, tudo o que está fora é pro computador ler e tudo o que está dentro é para, nesse caso, ser jogado na tela: 

```
console.log("Digite seu nome de jogador:")
```
- Para declarar uma váriavel nós escrevemos let e em seguida damos um "apelido" a essa variável para poder chamar ela depois;
- Para atribuir uma informação diretamente coloca o =, que na programação é chamado de atribuição, e em seguida a informação:

```
let nickname = "Beliack"
```
- Para uma variável aparecer na tela usamos o console.log(nickname), mas se quiser que apareça uma mensagem junto devemos concatenar utilizando o +, então ficaria:

```
console.log("Bem vinda " + nickname + "!")
```
- Nessa linguagem usamos o // para comentar algo e não interfirir no código;
- É importante comentar tudo o que se está fazendo no código para depois saber o que está acontecendo e para fixar também:

```
//mensagem inicial de saída
console.log("Digite seu nome de jogador:")

//declarando uma variável
let nickname = "Beliack"

//mensagem de saída concatenando uma mensagem fixa com uma variável utilizando o +
console.log("Bem vinda " + nickname + "!")
```

### Constantes x Variáveis

- Uma constante é uma mensagem que aparece com constância, repetidas vezes e não pode variar em nenhum momento depois que foi declarada, a não ser claro que seja reescrita na sua linha de  criação;
- Para declarar uma constante é preciso digitar const e dar um nome a ela:

```
const notificacao = "Pokemon Go diz: "
```

**obs**: ao programar palavras chaves e variáveis, evite colocar acentos, caracteres especiais como ç, números no começo (evite no final também), não coloque espaço (use letras maiusculas, camel case, ou _ para diferenciação) e utilize nomes objetivos para ser de fácil utilização e entendimento.

**Exemplo para diferenciação de variável e constante:**
- Constante:

```
// declarando uma constante
const notificacao = "Pokemon GO diz: "

// mensagem de saida com a constante
console.log(notificacao + "Você foi derotada por um líder de Ginásio")
console.log(notificacao + "Um novo pokemon apareceu na região")
console.log(notificacao + "Sua Eevee encontrou um doce enquanto caminhava com você")
```

Se eu tentar mudar essa constante para outro valor ele não irá funcionar e mostrará uma mensagem de erro.

- Variável:
 
```
// declarando uma variável
let notificacao = "Pokemon GO diz: "

// mensagem de saida com a variável
console.log(notificacao + "Você foi derotada por um líder de Ginásio")
console.log(notificacao + "Um novo pokemon apareceu na região")
console.log(notificacao + "Sua Eevee encontrou um doce enquanto caminhava com você")

// alterando valor da variável
notificacao = "Digimon GO diz: "

// mensagem de saida com a variável
console.log(notificacao + "Você foi derotada por um líder de Ginásio")
console.log(notificacao + "Um novo pokemon apareceu na região")
console.log(notificacao + "Sua Eevee encontrou um doce enquanto caminhava com você")
```

Agora ao invés de aparecer Pokemon GO diz: Você foi derotada por um líder de Ginásio ele mostrará Digimon GO diz: Você foi derotada por um líder de Ginásio no console.

### Exercício:

```
// declarando variáveis
let poteAcucar = "Açúcar Cristal"
let poteCafe = "Café Pilão"
let poteBiscoito = "Biscoito Maizena"

// declarando constante
const mensagemVovó = "Hoje na cozinha da vovó temos "

// mensagem de saída 
console.log(mensagemVovó + 
poteAcucar + ", " +
poteCafe + " e " +
poteBiscoito)

// a vovó trocou de marca de café
poteCafe =  "Café Forte"

// nova mensagem de saída para mostrar mudanças na variável
console.log(mensagemVovó + 
poteAcucar + ", " +
poteCafe + " e " +
poteBiscoito)
```

### Tipos de Variável

Mais comuns:
- String: São variáveis que armazenam textos (let nomePokemon = "pikachu", pode usar '' aspas simples também mas o padrão é a utilização de aspas duplas "");
- Number: São variáveis que armazenam números, tanto inteiros como quebrados, (let nivelPokemon = 20, quando é um valor numérico ele não requer que coloque aspas duplas);
- Boolean: São variáveis lógicas que armazenam apenas dois valores, True e False, são como alavancas, ou está ligado ou está desligado (let selecionavel = true OU let selecionavel = false);

O JavaScript é uma linguagem não tipada, ela não te obriga a declarar qual o tipo da variável mas em outras linguagens o caso é diferente.

Há diversos outros tipos de variáveis mas depende da linguagem que está sendo utilizada, algumas tem suas variáveis específicas.


### Exercício:

```
// reprensentando caso real em variável
// meu registro de gateira
// nome, idade, quantidade de gatos, algum é meu grude?

// declarando variáveis
// string
let nomeGateira = "Ana Luiza M. Guglielmini"
// number
let idadeGateira = 19
let qtdGatos = 3
// boolean
let algumGrude = false

// mensagem de saída 
console.log("Informações de gateiro(a): " + 
nomeGateira + ", " + 
idadeGateira + " anos, " +
qtdGatos + " gatos. " +
"Tem algum grude? " + algumGrude)
```

## 4 - Criando e Manipulando Vetores e Matrizes

### Vetores e Matrizes - Arrays

**Vetores:**

- Palavra chave: coleção;

- Caixa para guardar coisas = variáveis;
- Armário para guardar caixas = vetor, coleção de informações.

Como declarar um vetor:
```
let pokemon = ["Pikachu", "Charmander", "Bulbassaur"]
```

Para mostrar na tela essas informações é necessário indicar qual deve ser mostrada, ou seja, informando a sua posição:

```
console.log(pokemon[0])
```
Irá aparecer o Pikachu, *a contagem começa a partir do 0 sempre*.
Pode ser tanto uma constante ou uma variável.

Funções ou Métodos: 
- Aparecem após colocar . depois de informar a contante ou variável;
- Os métodos são representados por caixinhas roxas na IDE;
- Caixinhas azuis são propriedades.

Exemplo: ``` pokemon.fill... ```
- É indicado que utilize um padrão no vetor, apenas números ou apenas textos. Tentar não misturar para não gerar problemas. Guardar sempre as mesmas coisas dentro de um vetor.

**Matrizes:**

- Vetor BiDimensional;

- Caixa para guardar coisas = variáveis;
- Armário para guardar caixas = vetor, coleção de informações;
- Armário bidimensional = matrizes, vetores com linhas e colunas, é um plano cartesiano;
- Vetor que tem vetores.

**Exemplo:**

```
// declarando matriz
let timePokemon = [
	["Pikahu", "M", 1],
	["Charmander", "F", 99]
]

// mensagem de saída da matriz para mostrar o nome do pikachu
console.log(timePokemon[0][0])
// ele pega a linha primeiro e depois a coluna dessa linha, x e y
// mensagem de saída mais complexa 
console.log("O pokemon " + timePokemon[1][0] + " é mais forte que o pokemon " + timePokemon[0][0] + " e é do sexo " + timePokemon[1][1])

```