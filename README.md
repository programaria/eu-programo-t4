# Conteúdo das aulas do curso Eu ProgrAmo

## Documentação HTML e CSS
É importante saber onde consultar quando houver dúvida sobre tags de HTML, seletores e propriedades de CSS. Existem várias fontes de documentação.
- [Tags de HTML - W3Schools](https://www.w3schools.com/tags/default.asp);
- [Propriedades de CSS  - W3Schools](https://www.w3schools.com/cssref/default.asp);
- [Seletores de CSS - W3Schools](https://www.w3schools.com/cssref/css_selectors.asp);
- [Documentação HTML - MDN](https://developer.mozilla.org/pt-BR/docs/Web/HTML/HTML5);
- [Documentação CSS - MDN](https://developer.mozilla.org/pt-BR/docs/Web/CSS);
- [Várias documentações](https://devdocs.io/).


## Aula 1 - Conceitos básicos e HMTL
### Conceitos básicos
- Internet;
- Front vs. back;
- Introdução Projeto;
- Navegadores, website;
- Editores de texto.

#### Editores de texto
Para se modificar um arquivo .html e .css, precisamos de editor de texto. Apesar de que um simples bloco de notas pode ser a ferramenta para criação desses arquivos, vários softwares foram lançados no mercado para gostos dos programado res, oferecendo facilidades e plugins para facilitar o desenvolvimento. Alguns famosos e notáveis são:
- [Sublime Text](https://www.sublimetext.com/);
- [Notepad++](https://notepad-plus-plus.org/);
- [Atom](https://atom.io/);
- O que vamos usar durante as aulas é o [Visual Studio Code](https://code.visualstudio.com/);


#### Estrutura de pastas
A estrutura de pastas básicas é:
```
css
   style.css
img
   imagem.jpg

index.html
```
Ou seja, uma pasta com um arquivo **index.html na raiz** e duas pastas:
- Pasta *css* para inserção de nossos estilos .css 
- Pasta *img* para inserção de nossas imagens.

-----

### HTML
HTML é uma abreviação de **Hyper Text Markup Language** (linguagem de marcação em hipertexto). Ou seja, não se trata de uma linguagem de programação, pois não tem lógica (algoritmos, processos etc). Ele cria a **estrutura** de uma página ou aplicação web, determinando a separação de layout e seu conteúdo.

Documentos .html possuem tags de estruturação básica:
```html
<!doctype html>
<html>
    <head></head>
    <body></body>
</html>
```

Internamente, as tags html possuem uma anatomia básica também:
```html
<nome-da-tag atributo="valor do atributo">
    conteúdo
</nome-da-tag>
```

| HTML | 
| ------------ |
| Tags de **estrutura**: html, head, body |
| Tags no **head**: title |
| Tags de **divisão**: div |
| Tags de **texto**: h1 ao h6, p | 
| Tag de **link**: a |
| Tag de **imagem**: img |

--------

## Aula 2 - CSS
### CSS
CSS é abreviação de **Cascading Style Sheet** (folha de estilos em cascata). É a linguagem que define **estilos** para o HTML, portanto, não se trata de linguagem de programação. CSS tem "cascata" no nome, devido a sua forma de determinar a propriedade de um elemento - levando em consideração *hierarquia de seletores* e de chamadas de estilo (inline, internal e external).

Para fazer o link de um arquivo .css em um documento .html, devemos inserir a tag <link> no <head> do documento, com o href do caminho do arquivo.
```html
<!doctype html>
<html>
    <head>
        <link rel="stylesheet" type="text/css" href="css/style.css">
    </head>
    <body></body>
</html>
```

Dentro do arquivo .css, a anatomia é:
```css
seletor {
    propriedade: valor;
}
```

Exemplo:
```css
p {
    color: red;
}
```

Sobre as prioridades, o inline tem a máxima prioridade, enquanto o external tem a menor.
inline > internal > external.
Por esse motivo, por questões de responsividade e de escalabilidade do código, não vamos trabalhar com estilos inline nem internal.
Para trabalharmos questões de hierarquia, vamos tentar ser mais específicas em nossos seletores no CSS externo.

> **ATENÇÃO!**
> Não esqueçam de **indentar** o código! Isso ajuda na sua legibilidade, manutenção e colaboração com outros desenvolvedores.
> Para indentar, selecione a linha do código e aperte *tab*.

HTML | CSS
------------ | -------------
Comentário: ```<!-- seu comentário aqui -->``` | Propriedade de **cor**: color, background-color
Tags no **head**: link | Propriedade de **fonte**: font-size, text-align
Tags de **divisão**: br |

--------

## Aula 3 - Listas, Classes, Display e HTML semântico
### Listas ordenadas e não ordenadas
Listas são usadas para enumeração de items. No HTML, eles também são utilizados para marcação de outros elementos, como itens de menu de navegação.
Para criar uma lista *ordenada*, devemos fazer:
```html
<ol>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ol>
```

Para criar uma lista *não ordenada*, devemos fazer:
```html
<ul>
    <li>Item</li>
    <li>Item</li>
    <li>Item</li>
</ul>
```

-- _&&&_ --

#### Classes e id
Classes e ids são atributos que podem ser inseridos em qualquer tag dentro da <body>. Eles são **atributos de nomeação**, sendo class muito usada para referência em CSS e id para Javascript (apesar de que há outras boas práticas no mercado atualmente).
Uma diferença entre os dois é que podem haver várias classes com o mesmo valor, ao passo que ids devem ser **únicos**.

-- _&&&_ --

#### Display inline, block e inline-block
Toda tag em HTML tem por padrão algum valor de display. Os três mais básicos são inline, block e inline-block, cujo entendimento é de extrema importância para manipulação eficiente de elementos na sua página web.

**Block**: são elementos que "ocupam" toda a largura do elemento pai, fazendo com que não deixe outros elementos do lado dele. Mesmo que seja forçado a ter uma medida menor (a partir de propriedade width), ele não deixa outro elemento na mesma linha horizontal.
- Podem conter outros tipos de elementos (inline, block e inline-block);
- Pode estar dentro somente de outros elementos block;

**Inline**: são elementos que ocupam somente o espaço do conteúdo.
- Não podem conter elementos block;
- Podem estar dentro de qualquer tipo de elemento (block, inline, inline-block);
- Não cria linhas novas;
- Não se consegue definir propriedades de width e height para ele.


![Imagem explicativa dos vários tipos de display](https://i.stack.imgur.com/mGTYI.png)


**Inline-block**: são elemento híbridos, que permitem que outros elementos fiquem um ao lado do outro (em linha), mas que também possam receber valores de width e height.
> Fonte da imagem: https://stackoverflow.com/questions/9189810/css-display-inline-vs-inline-block

-- _&&&_ --

#### HTML5 e tags semânticas
HTML5 foi uma grande atualização da linguagem de markup, feita em 2014, que definiu e criou novas maneiras de se mostrar conteúdo multimídia (vídeo, áudio etc) e deixar o documento mais semântico.
O que significa deixar nosso documento mais semântico? Significa deixá-lo mais legível para algoritmos de sites de busca e para outros desenvolvedores.
Ao invés de criar tags div com classes de nav, header, footer, section, foram criadas novas tags com os mesmos nomes.
Exemplo de um documento sem tags semânticas:
```html
<div class="nav">
    <ul class="menu">
        <li>Nav 1</li>
    </ul>
</div>
<div class="header">
    <h1>Título</h1>
</div>
<div class="main">
    <div class="section">
        <p>Lorem</p>
    </div>
</div>
<div class="footer">
    Copyright
</div>
```

Exemplo com tags semânticas:
```html
<nav>
    <ul class="menu">
        <li>Nav 1</li>
    </ul>
</nav>
<header>
    <h1>Título</h1>
</header>
<main>
    <section>
        <p>Lorem</p>
    </section>
</main>
<footer>
    Copyright
</footer>
```
Nota-se que nem todas as classes foram transformadas em tags semânticas, como o menu.

Tags semânticas mais usadas são: header, nav, section, article, main e footer.
![Esquema exemplo de HTML semântico](https://www.w3schools.com/html/img_sem_elements.gif)


[Lista completa de tags semânticas](https://www.w3schools.com/html/html5_semantic_elements.asp)



HTML | CSS
------------ | -------------
Tags de **divisão**: div, span | Propriedades de **layout**: width, height, margin, padding, display (inline-block), border
Tags de **lista**: ul, ol, li | Propriedades de **lista**: list-style
Tags **semântico**: nav, header, main, section, article, aside, footer | Propriedades de **fontes**: Font (-family,  -style, -weight), Text-decoration, Text-transform


--------

## Aula 4 - Tabelas
#### Tabelas
Tabelas são usadas para organização de certos tipos de informação. Sua estrutura no HTML se faz através de tags como table, thead, tbody, tr, td. Saber o que cada sigla significa em português ajuda muito na hora de entender o uso de cada tag.
- table: tabela;
- thead: table head, ou **cabeça** de tabela;
- tbody: table body, ou **corpo** de tabela;
- tr: table row, ou **linha** de tabela;
- th: table header, ou **cabeçalho** de tabela;
- td: table data, ou **dado** de tabela.
Sendo assim, a estrutura básica de uma tabela é:
```html
<table>
    <thead>
        <tr>
            <th>Cabeçalho 1</th>
            <th>Cabeçalho 2</th>
            <th>Cabeçalho 3</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Dado de coluna 1</td>
            <td>Dado de coluna 2</td>
            <td>Dado de coluna 3</td>
        </tr>
    </tbody>
</table>
```
Existe também o tfoot, que define o footer de uma tabela. Para mais informações, consulte a [documentação](https://www.w3schools.com/html/html_tables.asp).

Podemos também definir quantas colunas ou linhas uma única célula (ou td/th) vai ocupar. Para isso, usamos os atributos *colspan* (para colunas) e *rowspan* (para linhas).

> E CSS em tabelas?
>
> Para estilizar nossas tabelas, é comum usar as propriedades de border, padding, text-align. Uma propriedade nova é a [border-collapse](https://www.w3schools.com/cssref/pr_border-collapse.asp), que não deixa as bordas adjacentes "duplicarem". Outra propriedade é o [border-spacing](https://www.w3schools.com/cssref/pr_border-spacing.asp), que define espaçamento entre células (só funciona para border-collapse: separate).

-- _&&&_ --

#### Responsividade
Hoje em dia, existem vários tipos de aparelhos e normalmente eles tem tamanhos de telas diferentes. O design que faz com que nossas aplicações e sites sejam usáveis em todos esses aparelhos se chama design responsivo.

Isso implica normalmente em termos sites com **layouts e imagens fluidos**. Por exemplo, se no computador o seu layout tem 3 colunas, no celular ele teria 1 apenas. O tamanho das imagens também se ajusta com o diferente tamanho de tela.

Para fazermos sites resposivos, vamos utilizar **media queries**. Elas separam pedaços de códigos em escopos para aparelhos com tamanhos de telas definidos por nós. Eles são inseridos no final do nosso código CSS. Exemplo:

```css
@media (min-width: 768px){
    p {
        color: red;
    }
}
```
Esse código quer dizer que para todo aparelho que tiver **no mínimo 768px de largura**, eu quero que os meus parágrafos sejam vermelhos.

Podemos usar vários pontos de quebra, ou seja larguras determinadas para a mudança de layout. Também chamamos esses pontos de *breakpoints*. Alguns breakpoints padrão são:
- 420px: celular
- 768px: tablet em posição retrato
- 1024px: tablet em posição paisagem
- 1200px: desktops
- 1800px+: desktops grandes e TVs

#### Desktop-first vs. Mobile-first
Desenvolver o site primeiro para computador ou para celular faz uma diferença para a determinação dos media queries.

Se escolher fazer desktop-first (computador primeiro), seu media query deve seguir a ordem decrescente e usar max-width.
```css
@media (max-width: 1200px){
    /* código para desktops menores que 1800px */
}

@media (max-width: 1024px){
    /* código para tablet paisagem */
}

@media (max-width: 768px){
    /* código para tablet retrato */
}

@media (max-width: 420px){
    /* código para celulares */
}
```
A ordem deve ser esta para que não haja conflito de estilos (o estilo do desktop sobrescrever o do celular, por exemplo).

Já se você optou por começar pelo mobile-first (celular primeiro), seu media query deve seguir a ordem crescente e usar min-width.
```css
@media (min-width: 420px){
    /* código para celulares maiores que 420px */
}

@media (min-width: 768px){
    /* código para tablet retrato */
}

@media (min-width: 1024px){
    /* código para tablet paisagem */
}

@media (min-width: 1200px){
    /* código para desktop */
}
```

-- _&&&_ --

#### Flexbox
O display: flex veio para nos ajudar a criarmos layouts fluidos e responsivos mais facilmente. 

Quando um elemento é flex, todos os seus elementos filhos ficam em linha, ou seja, um do lado do outro.

Além disso, com o display: flex, outras propriedades são habilidatas, como:
- **flex-direction** (determina se os elementos ficam alinhados horizontal ou verticalmente);
- **flex-wrap** (habilita e desabilita a possibilidade de os elementos irem para outra linha, caso não caibam todos dentro do container, na mesma linha);
- **justify-content** (propriedade de alinhamento no eixo principal, ou horizontal, por padrão);
- **align-items** (propriedade de alinhamento no eixo contrário, ou vertical, por padrão)

Para se familiarizar com as propriedades e com o display: flex, confira os links abaixo:
- [Artigo com gifs explicativos em Flex - inglês](https://medium.freecodecamp.org/an-animated-guide-to-flexbox-d280cf6afc35)
- [Guia completo de Flexbox - inglês](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [FlexFroggy: jogo para aprendizagem do flex. Disponível em português.](http://flexboxfroggy.com/)



HTML | CSS
------------ | -------------
Tags de **tabela**: table, thead, tbody, th, td, tr | Propriedades de **tabela**: border-collapse, border-spacing
--  | Propriedades de **flexbox**: display: flex, justify-content, align-items
