# JavaScript Fundamentos

_Caso você ainda não tenha lido a nossa documentações dos fundamentos HTML clique [AQUI](https://github.com/iuricode/ensinando-frontend/blob/main/modulos/html/html.br.md)_ </br>

_Caso você ainda não tenha lido a nossa documentações dos fundamentos CSS clique [AQUI](https://github.com/iuricode/ensinando-frontend/blob/main/modulos/css/CSS.br.md)_

## O que é JavaScript?

JavaScript é uma linguagem de programação que permite a você implementar itens complexos em páginas web. Toda vez que uma página da web faz mais do que simplesmente mostrar a você informações estáticas, mostrando conteúdo que se atualiza em um intervalo de tempo, mapas interativos ou gráficos 2D/3D animados, etc. Você pode apostar que o JavaScript provavelmente está envolvido. É a terceira camada do bolo das tecnologias padrões da web, duas das quais ([HTML](https://github.com/iuricode/ensinando-frontend/blob/main/modulos/html/html.br.md) e [CSS](https://github.com/iuricode/ensinando-frontend/blob/main/modulos/css/CSS.br.md)) que já falamos sobre elas por aqui.

## Iniciando
Vamos por etapas.
### Etapa 1: Criar um arquivo JS:
O primeiro passo é criar um arquivo ".js". Então abrindo seu editor de códigos, crie um novo arquivo chamado de script.js(você pode nomeá-lo como quiser, porém não pode faltar o .js no final).
### Etapa 2: Linkar seu JS no HTML.
Precisamos conectar nossa página script.js à página HTML. Dentro da tag `<body>` de sua página html, vamos adicionar uma tag `<script>` para conectar nosso código JavaScript. É recomendado salvar no final do seu código, somente acima das tags `<body>` e `<html>`. Exemplo:
```html

    <script src="./script.js"></script>
        
</body>
</html>

```
## Comentários em JavaScript
Comentários são linhas de códigos não executáveis.
### Barra dupla // Serve para comentar uma linha de código
```html
// var texto = "esse código não será executado"
```
### Começa com /* e termina com */ Podemos comentar várias linhas de código
```htmL
/*
var idade = 15
var conseguir = 'você vai conseguir'
*/
```
O código acima não sera executado, pois está dentro de um comentário /* */.
## Variaveis
Uma variável é um espaço na memória do computador destinado a um dado. Pode inicar com as palavras var, let e const.
Obs: Variaveis podem ser executadas com qualquer nome, exceto se estiver entre esses:
Os nomes podem iniciar com $, _, ou letras.

Podem conter números mas não iniciar com eles

Case sensitive

nome é diferente de Nome // Maiscúlo é diferente de minúsculo

Não utilizar palavras reservadas, um link abaixo com todas as palavras reservadas de js.
https://www.w3schools.com/js/js_reserved.asp


### Sintaxe
Palavra chave (var,let ou const) seguida de um nome, sinal de "=" e o valor.
```html
var nome = 'andrew';
let idade = 18;
const estudante = true;
```
### Evitam repetições
```html
var quantidade = 5;
var valor = 20;
var total = quantidade * valor; // Nesse caso retornar 5 * 20 que é : 100;
```
```html
var valor1 = 10;
console.log(++valor1) // 11; o sinal de ++ é conhecido como operador de incremento e soma o 1 a variável `valor1` ou a qualquer outro elemento tipo Number.
// para ver o resultado do console.log. Abra seu arquivo html que está linkado com o .js no navegador, clique com o botão direito do mouse
"inspecionar" e procure por console. Lá ira aparecer o resultado dele.
```
## Tipos de dados
JavaScript possui 7 tipos de dados. Tirando os objetos, todos são primitivos.
```html
var idade = 18; // Number
var nome = 'andrew'; // String
var estudante = true; // Boolean
var time; // Undefined
var null = null; // Null
var simbolo= symbol(); // Symbol
var objeto = {}; // Obejto
```
### Descobrir o Tipo da variável
Para isso, utilizamos o Typeof().
```html
var time = 'vasco';
console.log(typeof(time)) // String
```
### Boolean
Vão sempre retornar um valor Booleano.
```html
10 < 5 // false; 10 é maior que 5?
7 > 2 // true; 7 é maior que 2?
5 <= 5 // true; 5 é menor ou igual a 5?
```
### Operadores Lógicos
O && compara se uma expressão `e` a outra é verdadeira.
o || compara se uma expressão `ou` a outra é verdadeira.
```html
true && true; // true
true && false; // false; somente uma delas é verdadeira
true || false; // true; Retorna o primeiro valor verdadeiro.
false || false; // false; Nenhuma delas é verdadeira.
```
### Condicionais if e else
Estruturas condicionais Javascript são como estruturas condicionais na maioria das linguagens de programação existentes,
as utilizamos para verificar uma condição e definir se algo deve ou não acontecer.
Se não chover hoje, vou jogar bola
Temos uma condição(se não chover) para executar uma ação(jogar bola) dependendo do resultado dessa condição. Se verdadeira, a ação é executada. </br>

```html
var naoChoveu = true;
if(naoChoveu){                         //  essa linha de código, verefica se a condição passada entre os parenteses é verdadeira.
  console.log('vou jogar bola')
}
else{
  console.log('ficarei em casa')
}
```
Coloque esse código em seu editor de códigos e veja o resultado. </br>
OBS: faça todos os teste você mesmo, faça exercícios, busque informações e se aprofunde.
## Exercícios
Abra seu editor de códigos e em um arquivo .js faça os exercícios abaixo. </br>
// Declare 5 variaveis e descubra o tipo delas



// Declare duas variaveis do tipo number e some elas. Guarde o valor em outra variável. </br>
Para informações detalhadas sobre todos os tipos de dados: clique [Tipos de Dados](https://ricardo-reis.medium.com/tipos-de-dados-javascript-a1f6f498a7d4) </br>
Obs: É recomendado que leia esse artigo para o melhor entendimento do contéudo a seguir!
## Funções
Funções são blocos de códigos fundamentais em JavaScript. Uma função é um procedimento de JavaScript, um conjunto de instruções que executa uma tarefa ou calcula um valor.
### Declarar uma função
A declaração de função consiste no uso da palavra chave `Function`.

```html
function multiplicacao(num){
 return num * num
}
console.log(multiplicacao(15)); // 225; chamando a função e demonstrando ela no console.
console.log(multiplicacao(2)); // 4;
console.log(multiplicacao(8)); // 64
```
### Parâmetros e Argumentos
Ao `criar` uma função, você pode definir o(s) parâmetros. <br>
Ao `Executar` uma função, você pode definir o(s) parâmetros.

```html
function imc(peso, altura){ //  Peso e Altura são parâmetros 
  const imc = peso / altura * 2
  return imc
}
console.log(imc(70, 1.90))  //  70, 1.80 são argumentos
```
## Objetos noções básicas
Um objeto é uma coleção de dados e/ou funcionalidades relacionadas (que geralmente consistem em diversas variáveis e funções, que são chamadas de propriedades e métodos quando estão dentro de objetos).
```html
var eu = {
  nome: 'andrew',
  idade: 18,
  time:'vasco',
}
console.log(eu) // { nome: "andrew", idade: 18, time = "vasco"}
console.log(eu.nome) // andrew

```
### Alterar nome de uma propriedade do objeto acima
```html
eu.nome = 'heitor';
```

### Adicionar uma nova propriedade no obejto acima
```html
eu.profissao = 'front end';
```

### Método é uma propriedade que possui uma função no local do seu valor.
Console.log() é um método, utilizado para demonstrar um determinado valor no console do navegador.
 ```html
var quadrado = {
  lados:4,
  area: function(lado){
    return lado + lado
  },
};
console.log(quadrado.lados); // 4
console.log(quadrado.area(4)); // soma 4 + 4 e retorna o 8.

```
### Quase tudo é objeto
Em JavaScript, quase tudo é um objeto. Todos os tipos primitivos, com exceção de null e undefined são tratados como objetos. Eles podem receber propriedades e métodos, e possuem todas as características de objetos.
```html
var nome = 'andrew';
console.log(nome.length) // 6; 6 letras existem no nome andrew
nome.replace("w", "ssa") // andressa; substituiu "w" por "ssa"
```
### Exercícios
Abra seu editor de códigos e em um arquivo .js faça os exercícios abaixo. </br>
Obs: Pratique muito JavaScript, isso te ajudará muito durante o aprendizado da linguagem. </br>
```html
// Crie um objeto com seu nome, idade e alguma outra informação


// Substitua o valor de uma propriedade do objeto acima e adicione uma nova


// Crie uma variável string e utilize 3 propriedades ou métodos nela.
// Não sabe? Faça uma rápida pesquisa no google "métodos e propiedades em JS" e teste os que achar.
```
## Arrays
O objeto Array do JavaScript é um objeto global usado na construção de 'arrays'. objetos de alto nível semelhantes a listas.
```html
var times = ["Barcelona", "Manchester United", "Milan"]
console.log(times) // (3) ["barcelona", "manchester united", "Milan"]
```
### Selecionando um valor em um Array
Para selecionarmos um valor em um array é necessário passar seu índice. Em um Array o primeiro índice é [0], então para chamarmos o primeiro valor do array acima, faremos assim:
```html
times[0]// barcelona;
times[1] // manchester united;
times[2] // Milan;
```
### Adicionando um valor ao final do Array
Utilizando o método push
```html
times.push("vasco");
console.log(times); // (4) ["barcelona", "manchester united", "Milan", "vasco"]
```
### Removendo o último item do array
Utilizando o método pop
```html
times.pop();
console.log(times) // (3) ["barcelona", "manchester united", "Milan"] // removeu o último valor que era o vasco.

```
## Loops
Um loop faz algo repetidamento até que uma condição seja atendida. Um loop possui 1 ou mais itens dos seguintes itens. </br>
O `contador`, é inicializado com um determinado valor. Este é o ponto inicial do loop. </br>
A condição de saída, que é o critério no qual o loop para, geralmente o contador atinge um certo valor. </br>
Um iterador, que geralmente incrementa o contador em uma pequena quantidade a cada loop, sucessivamente, até atingir a condição de saída. </br>
```html
for(var i = 1; i < 10;i++){
  console.log(i);
}
```
### Var, Const ou Let. Qual usar?
## DOCUMENT OBJECT MODEL (DOM) Introdução;
É uma interface que representa documentos HTML e XML através de objetos. Com ela é possível manipular a estrutura, estilo e conteúdo destes documentos.
Um exemplo de como adicionar uma class em uma section por exemplo com o Dom.
```html
var section = document.querySelector('section');
section.classList.add('nome da class que quer adicionar').
```
## Fontes de Pesquisa

[Developer Mozilla](https://developer.mozilla.org/pt-BR/docs/Learn/JavaScript/First_steps/O_que_e_JavaScript)</br>
[Data Types](https://ricardo-reis.medium.com/tipos-de-dados-javascript-a1f6f498a7d4) </br>
[Origamid](https://www.origamid.com)
