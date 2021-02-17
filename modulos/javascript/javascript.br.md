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
Para informações detalhadas sobre todos os tipos de dados: clique [Tipos de Dados](https://ricardo-reis.medium.com/tipos-de-dados-javascript-a1f6f498a7d4)
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


## Fontes de Pesquisa

[Developer Mozilla](https://developer.mozilla.org/pt-BR/docs/Learn/JavaScript/First_steps/O_que_e_JavaScript)</br>
[Data Types](https://ricardo-reis.medium.com/tipos-de-dados-javascript-a1f6f498a7d4)
