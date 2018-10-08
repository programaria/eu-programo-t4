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