# HTML Fundamentos

## O que é HTML?
HTML, ou *Hypertext Markup Language* é uma linguagem de marcação (não de programação) da web - cada vez que você carrega uma página da web, você está carregando um código HTML.
Pense em HTML como o esqueleto de uma página da web, ele é responsavel pelos textos, links, listas e imagens - ele oferece *conteúdos* (enquanto javascript fornece *comportamento dinamicos* e o css *estilos*).

---

## Iniciando
HTML é escrito em arquivos *.html*. Para criar uma página HTML é facíl, entre em seu editor de código e salva em arquivo em branco como `meu-site.html` (você pode nomeá-lo como quiser).

---

## Sintaxe
Os elementos HTML são escritos usando tags. Todas as tags tem uma chave de abertura e fechamento (por exemplo, `<tag>`) e uma tag de fechamento que tem uma barra após o primeiro colchete (por exemplo, `</tag>`).

```
<tag>
  iuricode
</tag>
```

Por exemplo, se você deseja criar um parágrafo, usaremos as chaves de abertura `<p>` e fechamento `</p>`:

```
<p>
  Um programador sem café é um poeta sem poesia.
</p>
```

*Os elementos podem entrar dentro de outros elementos:*

```
  <pai>
    <filho>
      Esta tag está dentro de outra tag também conhecida como a tag pai.
    </filho>
  </pai>
```
---

## Estrutura de uma página HTML
A estrutura inicial do seu html é essa:

```
<! DOCTYPE html>
<html>
  <head>
  </head>
  <body>
  </body>
</html>
```

*Vou explicar sobre elas*
+ `<! DOCTYPE html> `- Essa tag (não tem fechamento dela) informa ao seu navegador que o arquivo faz parte de um documento HTML5. 
+ `<html>` - Essa é tag que seu código todo vai fichar dentro `<html>` seu código aqui `</html>`.
+ `<head>` - O head contém informações sobre seu site, mas não é o conteudo que vai aparecer na sua página. Ela conterá coisas como: links para folhas de estilo (CSS), título pa sua página, link de fontes e tudo aquilo que você quiser linkar (só não recomendo link seu script dentro dessa tag).
+ `<body>` - No body contém todo o conteúdo que vai aparecer na sua página. Todo o código que você escrever irá dentro dele.

---

## Indentação adequada 
As quebras de linha entre suas tags são **super importante** para escrever um bom código HTML. 

```
<! DOCTYPE html>
<html>
  <head>
  </head>
  <body>
    <h1> Aqui temos um título </h1>
    <p> E aí, já curtiu esse repositório? </p>
  </body>
</html>
```

*Abaixo temos um indentação não recomendada:*

```
<! DOCTYPE html> <html> <head> </head> <body> <h1> Não faça isso! </h1> </body> </html>
```

# Tags
*Agora vamos apresentar as principais tags do HTML*

## Tags de títulos

Os elementos de cabeçalho *H* representam seis níveis de título de seção. `<h1>` é o nível de seção mais alto e `<h6>` é o mais baixo. Quanto maior for o nível do *H* menor vai ser o tamanho de pontos da fonte. Vejamos:

```
<h1> tamanho 24 pontos </h1>
<h2> tamanho 18 pontos </h2>
<h3> tamanho 14 pontos </h3>
<h4> tamanho 12 pontos </h4>
<h5> tamanho 10 pontos </h5>
<h6> tamanho 8 pontos </h6>
```

*Ficara assim na página:*

<h1> tamanho 24 pontos </h1>
<h2> tamanho 18 pontos </h2>
<h3> tamanho 14 pontos </h3>
<h4> tamanho 12 pontos </h4>
<h5> tamanho 10 pontos </h5>
<h6> tamanho 8 pontos </h6>

---

# Tags de imagem
*Vamos colocar uma imagem no seu site?*

É bem simples colocar uma imagem no HTML. Vejamos:

```
<img src="nomeDoArquivo.formato">
```

Você talvez deve ter se perguntado o que é esse `src`, src (source) é atributo da tag `<img>`, nele vai conter a url da imagem que será inserida por você.

Alguns pontos importante:
+ A tag img não tem a chave de fechamento.
+ Se você tiver com a imagem de uma pasta deve colocar o caminho dela dentro do *src*.
+ Recomendamos que você coloque o atributo `alt` para que pessoas com deficiência saberem do que se trata a imagem na página.

```
<img src="nomeDaPasta/nomeDoArquivo.formato" alt="descrição sobre a imagem">
```
---

## Tags de lista
Vamos falar agora um pouco sobre as listas (ordenadas e desordenadas) e como elas funcionam no HTML.
As listas são muito importantes quando queremos listar alguns itens no site e também para a criação de menu de navegação.

+ Listas ordenadas.
+ Listas desordenadas.

#### Listas ordenadas

```
<ol>
  <li>html</li>
  <li>css</li>
  <li>javascript</li>
  <li>front-end</li>
</ol>
```

Aparecerá assim no site:

1. html
2. css
3. javascript
4. front-end

Caso você queria deixar em ordem alfabética é simples, coloque o atributo `type="a"` dentro da tag `<ol>`.

```
<ol type="a">
  <li>html</li>
  <li>css</li>
  <li>javascript</li>
  <li>front-end</li>
</ol>
```

Aparecerá assim no site:

a. html
b. css
c. javascript
d. front-end

Você também pode deixar com algarismos romanos.

```
<ol type="I">
  <li>html</li>
  <li>css</li>
  <li>javascript</li>
  <li>front-end</li>
</ol>
```

Aparecerá assim no site:

I. html<br>
II. css<br>
III. javascript<br> 
IV. front-end<br>

#### Listas desordenadas
As listas desordenadas seguem o mesmo padrão apenas mudando de `<ol>` para `<ul>`. Em seu visual ele mudara para pontos (na lateral dos itens) no lugar de números.

```
<ul>
  <li>html</li>
  <li>css</li>
  <li>javascript</li>
  <li>front-end</li>
</ul>
```

Aparecerá assim no site:

* html
* css
* javascript
* front-end

---

## Tags para formulário
*Essa seção vamos mostrar como montar seu formulario.* 
Formulários HTML são um dos principais pontos de interação entre um usuário e um web site. Um formulário HTML é feito de um ou mais widgets. Esses widgets podem ser campos de texto (linha única ou de várias linhas), caixas de seleção, botões, checkboxes ou radio buttons. 

Para construir o nosso formulário de contato, vamos utilizar os seguintes elementos `<form>` , `<label>` , `<input>` , `<textarea>`  e `<button>`.

#### Elemento Form

Todos formulários HTML começam com um elemento `<form>` como este:

```
<form action="/pagina-processa-dados-do-form" method="post">

</form>
```

*Todos os seus atributos são opcionais, mas é considerada a melhor prática sempre definir pelo menos o atributo action e o atributo method.*

+ O atributo action define o local (uma URL) em que os dados recolhidos do formulário devem ser enviados.
+ O atributo method define qual o método HTTP para enviar os dados (ele pode ser "GET" ou "POST" (veja as diferenças aqui).

#### Elementos Label, Input e Textarea
O nosso formulário de contato é muito simples e contém três campos de texto, cada um com uma etiqueta. O campo de entrada para o nome será um campo básico texto de linha única ("input"); o campo de entrada do e-mail será um campo de texto com uma única linha ("input") que vai aceitar apenas um endereço de e-mail; o campo de entrada para a mensagem será um campo de texto de várias linhas ("textarea").

Em termos de código HTML, teremos algo assim:

```
<form action="/pagina-processa-dados-do-form" method="post">
    <div>
        <label for="nome">Nome:</label>
        <input type="text" id="nome" />
    </div>
    <div>
        <label for="email">E-mail:</label>
        <input type="email" id="email" />
    </div>
    <div>
        <label for="msg">Mensagem:</label>
        <textarea id="msg"></textarea>
    </div>
</form>
```

*Algumas observações:*

+ Observe o uso do atributo for em todos os elementos `label`; é uma maneira para vincular uma label à um campo do formulário.
+ No input temos o atributo `type`. Esse atributo ele defina a forma que nosso input se comporta. Exemplo: `type="text"` (é o valor padrão para este atributo), o `type="email"` ele define que o campo aceita só endereço de e-mail.
+ Por último, mas não menos importante, a tag `<textarea>`. O tipo *textarea* não é um elemento de auto-fechamento, então você tem que fechá-lo com a tag final adequada.

#### Elemento Button
Pronto! O nosso formulário está quase pronto; nós temos apenas que adicionar um botão para permitir que o usuário envie seus dados depois de ter preenchido o formulário. Isto é simplesmente feito usando o elemento `button`:

```
<div class="button">
  <button type="submit">Enviar sua mensagem</button>
</div>
```

*Um botão pode ser de três tipos: `submit`, `reset` ou `button`*

+ Um clique sobre um botão de submit envia os dados do formulário para a página de web definida pelo atributo action do elemento `<form>`.
+ Um clique sobre um botão de reset redefine imediatamente todos os campos do formulário para o seu valor padrão. 
+ Um clique em um botão do tipo button faz ...ops, nada! Isso soa bobo, mas é incrivelmente útil para construir botões personalizados com JavaScript, ou seja, ele pode assumir qualquer comportamento através desta linguagem.

*Resultado final*

```
<form action="/pagina-processa-dados-do-form" method="post">
    <div>
        <label for="nome">Nome:</label>
        <input type="text" id="nome" />
    </div>
    <div>
        <label for="email">E-mail:</label>
        <input type="email" id="email" />
    </div>
    <div>
        <label for="msg">Mensagem:</label>
        <textarea id="msg"></textarea>
    </div>
    <div class="button">
  <button type="submit">Enviar sua mensagem</button>
</div>
</form>
```

*Última observação*

Você pode ter percebi que no nosso formulário usamos a tag `div`. A tag *div* não tem nenhum efeito em nosso formulário, como ela tem um propriedade *display block* como padrão, o uso dela ajuda a quebrar os elementos em linhas, deixando melhor a visualização.

---

## Tags semânticas
Na vida sempre temos uma forma correta de fazer as coisas, no HTML não é diferente! 
As tags semânticas além de deixar o código melhor para o SEO dos navegadores, ela ajuda outros desenvolvedores a entender seu código só batendo o olho, isso é **ótimo** para que outros desenvolvedores contribuem em seus projetos.
Uma observação: *as tags semânticas não tem **nenhum** efeito na apresentação na página da web.*

+ Elementos semânticos: tem significado e deixam seu conteúdo claro `<form>`, `<table>`, `<article>`, `<footer>` e `<section>`*.
+ Elementos não semânticos: não deixam seu conteúdo claro `<div>` e `<span>`.

*Exemplo:*

Veja que div é amplo, mas footer dá significado (que é o rodapé). Portanto ao invés de

```
<div id="footer">
```

*não seria melhor:*

```
<footer>
```

### As principais tags semânticas

+ `<article>` expressa um elemento independente, ou seja, que possa ser lido e interpretado sem depender do resto da página. Um bom exemplo é uma notícia de jornal ou uma pergunta no Stackoverflow.
+ `<aside>`: por conceito, expressa um conteúdo a parte do conteúdo da página. Na prática, pense em um box de informações dentro de uma página.
+ `<datails>`: representa detalhes adicionais que o usuário pode mostrar ou esconder.
+ `<figcaption>`: representa uma legenda para um elemento `<figure>`.
+ `<figure>`: representa um conteúdo independente, como ilustrações, diagramas, etc...
+ `<footer>`: representa o rodapé de um documento ou section.
+ `<header>`: representa o cabeçalho de um documento ou section.
+ `<main>`: representa o conteúdo principal de um documento.
+ `<mark>`: representa um texto destacado.
+ `<nav>`: representa links de navegação.
+ `<section>`: representa uma seção dentro de um documento.
+ `<summary>`: representa um cabeçalho para um elemento details.
+ `<time>`: representa uma data/hora.


# Fontes de pesquisa

[Developer mozilla](https://developer.mozilla.org/pt-BR/docs/Web/HTML)

[Stack oveflow](https://pt.stackoverflow.com/)



[⬅ Voltar ao README principal](https://github.com/iuricode/estudos-no-frontend)