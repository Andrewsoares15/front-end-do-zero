# CSS Fundamentos

*Caso você ainda não tenha lido a nossa documentações dos fundamentos HTML clique [AQUI](https://github.com/iuricode/ensinando-frontend/blob/main/modulos/html/html.br.md)*

## O que é CSS?
CSS ou *folhas de estilo em cascata* é a linguagens de marcação (não de programação) responsável por adicionar estilos nos sistema na web, como cores, tamanhos, posicionamentos. Sem ele, os sites são apenas um monte de texto e links, html acaba virando um Markdown.

---

## Aplicando estilo CSS em uma página HTML
Vamos por etapas:

### Etapa 1: Criar um arquivo CSS
A primeira coisa que precisamos fazer é criar um arquivo css do qual nossa página html possa obter seu estilo. Então em seu editor de código crie um novo arquivo chamado `style.css`.

### Etapa 2: Linkar seu CSS no HTML
Precisamos conectar nossa página `style.css` à página HTML. Dentro da tag `<head>` de sua página html, vamos adicionar uma tag `<link>` para conectar a nossa nova folha de estilo.

```html
<link rel = "stylesheet" href = "style.css">
```

*certifique-se de que sua página html e sua folha de estilo css estão no mesmo nível de pasta, caso ele esteja dentro de uma pasta é simples chamar, basta colocar o nome da página antes do nome do arquivo seperado ele com uma barra (/)* 

```html
<link rel = "stylesheet" href = "nomeDaPasta/style.css">
```

### Etapa 3: Selecione e dê estilo aos elementos, por elemento
Experimente selecionar um elemento e estilizá-lo! Em seu tipo de folha de estilo:

```css
h1 {
  color: #00f;
  font-size: 25px;
}
```

*Isso para que todos os elementos h1 da sua página fique com um tamanho 25px e com a cor azul. (atualize a página sempre que aplicar um CSS ou HTML)*

---

# Folha de Estilos
O que constitui uma folha de estilos? Bem, basicamente uma folha de estilos é algo simples, descrevem um conjunto de regras no css onde apresenta tags para o leitor identificar de forma mais explícita referências ou algum recurso em específico, aplicando estilos. Iremos usar serão definidos dentro do par de tags ```<head>...</head>``` como será mostrado a seguir.

```html
<style type="text/css" title="mystyles" media="all">

</style>
```

Iremos a explicação básica dos elementos citados acima:

`type="text/css` - Até aqui nada em especial, isto diz ao navegador que estamos usando um tipo de arquivo puro para descrever os estilos que iremos usar.

`title=Meuestilo` - Este em especial é algo de sua livre escolha para nomear e mais tarde identificar os estilos presentes, pode conter qualquer nome.

`media=all` - Quando chega aqui nestas palavras as coisas já começam a ficar interessantes pois começam a se tratar de elementos responsivos para ajudar os "bots" dos navegadores a encontrarem o seu conteúdo no meio de milhares de sites. A palavra media significa que você pode ter livre-arbítrio para escolher o que sua página irá apresentar na tela do navegador do usuário, adaptando cores, altura e largura citamos alguns exemplos:

`media=print` - Foi designada para o layout de impressão em papel.

`media=tv` - Designada para televisores.

`media=all` - Todos os dispositivos.

`media=embossed` - Para dispositivos que imprimem em braile entre outros.

## Aplicando Cor de Fundo

Agora iremos aos estilos, a primeira coisa que iremos realizar é a abertura da tag ```<body>...</body>```. De forma resumida tudo que estiver dentro desta tag irá afetar os elementos da página de forma geral.
A definição de body é seguida com um par de chaves.

```css
body {
  ...
}
```
Os navegadores por padrão processam as páginas na cor branca e textos na cor escura, primeiramente dentro do body mesmo iremos realizar alterações no padrão de cor de fundo.

```css
body {
  background color: #4169E1;
}
```
Repare que eu usei o elemento "#" na hora de definir uma cor, isto acontece pois o css utiliza o formato de cores com o código hexadecimal, o nome das cores em inglês e também o valor RGB (Red, Green, Blue) para definir o seu estilo

## Aplicando cor ao texto

Da mesma maneira podemos definir partir da tag "color", cores ao texto tirando o padrão preto dele de antigamente.

```css
body {
  background color: #5d665b;
  color: #5d665b;
}
```
Observação: Da mesma maneira que eu coloquei na cor de fundo, nunca esqueça de incrementar o ponto vírgula no final, pois no css a pontuação é algo fundamental podendo causar até erros

## Aplicando a margem

Também podemos aplicar a famosa margem muita usada principalmente por mim para alinhar e acertar o posicionamento desejado de seu texto

```css
body {
  background color: #5d665b;
  color: #5d665b;
  margin: 50px;
}
```
---
# Class e ID
Class e ID são tipos de atributos que podemos adicionar a um elemento para ser mais específicos com nossos seletores CSS.
Até agora, só pudemos selecionar elementos (como `<h1>`). Embora isso seja útil, às vezes precisamos ser mais específicos. Exemplo, temos várias tags `<p>` em uma página, mas temos um `<p>` que queremos mudar de cor. E nesses casos que entrar a Class e o ID para selecionar apenas um elemento. Exemplo:


```html
<p class = "souClass">
```

```html
<h1 id = "souID">
```

## Chamando no CSS
Para fazemos referência a uma classe usando um `.` e o nome da classe, exemplo:

```css
.souClass {
  color: # f00;
}
```

Fazemos referência a um id usando um `#` e o nome do id:

```css
#souID principal {
  color: # f00;
}
```

*Dessa forma, todos os elementos que tiverem a Class .souClass e o ID #souID vão ficar com a cor de texto de vermelho.*

## E qual usar?
Agora te bateu uma dúvida né? *Se os dois fazem a mesma coisa, qual devo usar?*

A resposta é simples, se você tem vários elementos (no nosso caso é o `<p>`) e queira usar de cor de texto vermelha em algumas, nesse caso usamos a Class, pense a Class em uma união em comum. Vou dar um exemplo que meu professor disse na faculdade, todos nós tem uma Class em como, que no caso é *humano* porém, todos nós temos um ID, que no caso é o *RG*. Então caso queira mudar somente em um elementos, usamos o ID.

---

# Bônus
Aqui vou dizer dois padrões que eu uso sempre no começo do meu CSS, o primeiro é o uso da *fonte* e o segundo é o *reset* nos padrões dos navegadores.

## Fontes
Para colocar fonte no seu site é preciso chamar ele no seu CSS (ou no HTML), para isso vamos entrar no site do Google Fonts. Logo em seguida, procure uma fonte que você deseja e clique no botões "Select this style" para assim adicionar os estilos que você deseja (perceba que quando você selecionar uma vai abrir uma aba na lateral direita). Nessa aba vai ter duas opções para colocar no seu site, um é o `<link>` e o outro `@import`. O link é para importar no seu HTML e o import é para o seu CSS, agora você me pergunta *qual eu devo usar?*, você pode escolher qualquer um, isso vai com seu gosto. Como para mim a fonte é um estilo, então eu sempre importo ele para meu CSS.

Logo depois de importar precisamos falar para nossa página que queremos aquela fonte em nossos textos e como fazer isso? É bem simples! 

Perceba de logo depois do import (na página do Google Fonts), em baixo tem uma código CSS com o nome *font-family*, é exatamente ele que vamos usar para colocar para dizer que aquela vai ser a fonte da nossa página. No seu CSS, coloque ela. 

```css
*{
  font-family: 'Nome da sua fonte aqui';
}
```

*Uma observação, se você está se perguntando o que é esse `*` no CSS, ele é um elemento universal, quer dizer que vai aplicada em toda sua página de estilo*

## Reset
Agora vamos resetar os navegadores, mas espera, o quer isso quer dizer?
Quer dizer que os navegadores tem um padrão deles, e alguns desses padrões não são legais, então vamos tirar alguns deles (três para falar a verdade)!

Primeiro vamos zerar os espaçamentos das nossas páginas. Quando criamos um HTML, por padrão, nosso site tem um espaçamentos e quando criamos algo, nossos estilos não fica da forma que queremos, eles acabam sempre tento um espaço em volta dele. Para tirar esse padrão usamos duas coisas. Um é o *padding* (espaçamento dentro do conteúdo) e o *margin* (espaçamento fora do conteúdo). Veja o exemplo:

```css
*{
  font-family: 'Nome da sua fonte aqui';
  padding: 0;
  margin: 0;
}
```

E por último, vamos aplicar o `box-sizing: border-box;` no nosso CSS. Mas você como é um gafanhoto curioso vai ser perguntar *o que ele faz? e por que devo usar ele?*, quando criamos uma caixa algo que use largura e altura, sempre definimos o valor delas (no nosso exemplo vai ser 300px e cada um). Mas caso você queira colocar um elemento dentro dessa tag que você definiu a largura e altura, e coloque um espaçamentos dentro dela (padding) de 30px, o elemento vai deixar de ser 300px e será 330px.

Mas a gente não quer isso, não é? Queremos que o elemento continue 300px (na altura e largura) porém, com um espaçamento dentro dela. É aí que entra o nosso querido `box-sizing: border-box;`. Veja o exemplo:


```css
*{
  font-family: 'Nome da sua fonte aqui';
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
```

*Caso queira testar com e sem o box-sizing: border-box;*

Aplique no seu CSS e no HTML:

*sem*

```css
*{
  font-family: 'Nome da sua fonte aqui';
  padding: 0;
  margin: 0;
}
#caixa{
  width: 300px;
  height: 300px;
  background-color: #ddd;
  padding:30px;
}
```

```html
<div id="caixa">
<p>iuricode</p>
</div>
```

*com (vamos apenas colocar o box-sizing: border-box; no nosso elemento universal)*

```css
*{
  font-family: 'Nome da sua fonte aqui';
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
#caixa{
  width: 300px;
  height: 300px;
  background-color: #ddd;
  padding:30px;
}
```


# Fontes de pesquisa

[Developer mozilla](https://developer.mozilla.org/pt-BR/docs/Web/CSS)

[Stack oveflow](https://pt.stackoverflow.com/)


[⬅ Voltar ao README principal](https://github.com/iuricode/ensinando-frontend)
