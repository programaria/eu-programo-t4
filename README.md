# Conteúdo das aulas do curso Eu ProgrAmo

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

HTML | 
------------ | -------------
Tags de **estrutura**: html, head, body |
Tags no **head**: title |
Tags de **divisão**: div |
Tags de **texto**: h1 ao h6, p | 
Tag de **link**: a |
Tag de **imagem**: img |


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

> **ATENÇÃO!**
> Não esqueçam de **indentar** o código! Isso ajuda na sua legibilidade, manutenção e colaboração com outros desenvolvedores.
> Para indentar, selecione a linha do código e aperte *tab*.


HTML | CSS
------------ | -------------
Comentário: ```<!-- seu comentário aqui -->``` | Propriedade de **cor**: color, background-color
Tags no **head**: link | Propriedade de **fonte**: font-size, text-align
Tags de **divisão**: br |


--------