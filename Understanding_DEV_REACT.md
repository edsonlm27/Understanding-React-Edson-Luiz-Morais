# ANOTAÇÕES DE AULA 
## CURSO DEV_REACT / ENTRA21-2023

## Autor: Edson Luiz Morais




### GIT E GITHUB

- Inicialmente, deve-se ter o Git instalado na máquina.  
- No Windows Explorer, deve-se ir até o diretório onde ficarão os arquivos do repositório local.
- Na guia onde consta o caminho do diretório, digitar 'cmd'.
- Isso fará com que abra o Command do Windows, já ná pasta selecionada, sem a necessidade de navegar até a mesma com comandos de diretório (cd).

#### Resumo dos principais comandos do Git:
- git --version
    - apresenta a versão instalada do Git.
- git init
    - para inicializar o Git na referida pasta.
- git status
    - verificar o status dos arquivos (untracked, tracked, ...).
- git add <filename>
    - para alterar o status do arquivo para 'tracked'.
- git add .
    - para alterar o status de todos os arquivos para 'tracked'.
- git commit -m "mensagem"
    - para fazer o commit no arquivo e gerar uma nove versão do mesmo; utilizar uma mensagem que traga uma fácil identificação da alteração.
- git config -global user.name (nome)
    - configurar o nome
- git config -global user.email (email)
    - configurar o email
- git log --oneline
    - mostra no log o histórico de commits
- git push 
    - enviar o conteúdo do repositório local para o repositório remoto
- git pull
    - atualizar o conteúdo do repositório remoto para o repositório local
- git clone (link)
    - efetuar o clone do repositório remoto para o repositório local




### MARKDOWN

#### Cabeçalhos
      h1 # ... até  h6 ######  


- parágrafos são separados por uma linha em branco
- quebra de linha, 2 espaços em branco no fim da linha
- evitar usar símbolo da tag <a> com conteúdo dentro (não aparece)

#### Texto com ênfase
*itálico* ou _itálico_  
**negrito** ou __negrito__  
```tachado```  
´´´tachado´´´  

#### Listas não ordenadas
- item a
- item b
    - sub item b1
        - sub sub item b1a

#### Listas ordenadas
2. primeiro item
2. segundo item
2. terceiro item
começa de acordo com o número do primeiro item

#### Lista de tarefas
- [X] tarefa 1
- [ ] tarefa 2
- [X] tarefa 3

#### Link
[texto do Link1](http://example.com/ "Propriedade title, opcional")  
<a href="http://example.com/" title ="Propriedade title, opcional" >Texto do link2</a>

#### Imagem
![Calculadora Windows](/assets/calculadora.png "Foto da Calculadora Win...")

#### Vídeo
[![Vídeo Markdown - YouTube]](https://youtu.be/vZaldeUg6D0)

#### Trecho de código
```
   if var > 0 then 
        display "Valor positivo"
   else
        display "Valor Negativo"
   and-if 
```

#### Tabela
Cod | Nome  | Nota | Aprov 
--- |:-----:|-----:|----
1   |Paulo  |6,0   | não
2   |Joana  |7,3   | sim


#### Emoji

##### VSCode
- Apenas dar copiar e colar emojis da Emojoipedia;

https://emojipedia.org/

🧐

##### GitHub
- Apenas usar os comandos demonstrados nesta pagina:

https://gist.github.com/rxaviers/7360908

:blush:  
:smirk:




## HTML
- Linguagem de marcação, fazendo uso de várias tags.
- Atualmente na versão 5.
- Utilizada em conjunto com CSS e JavaScript.
- Recomendável seguir uma estrutura básica:
```
<!DOCTYPE html>
<html>

<head>

</head>

<body>
  <header>
  </header>
  <main>
  </main>
  <footer>
  </footer>
</body>

</html>
```
- Algumas tags podem fazer uso de atributos, obrigatórios e opcionais.
- Algumas tags precisam da tag de fechamento </html>, outras não.




## CSS
- CSS, ou Cascading Style Sheets, são folhas de estilo em cascata, para formatar a apresentação dos documentos de marcação, layout, animações, efeitos.
- Atualmente na versão 3.
- Utilizada em conjunto com HTML e JavaScript.
- Pode ser aplicado de três maneiras:
1. 	CSS inline: estilos aplicados diretamente em um elemento HTML, dentro do documento.
```
<h1 style="color:blue;text-align:center;">This is a heading</h1>
<p style="color:red;">Este é um parágrafo.</p>
```

2. 	CSS Interno/Incorporado: o elemento style permite aplicar várias regras de uma vez no próprio documento HTML
```
<head>
<style>
body {
    background-color: green;
}

h1 {
    color: brown;
    margin-left: 40px;
}
</style>
</head>
```

3. 	CSS Externo: um documento com extensão .css permite aplicar regras a um website inteiro de uma vez.
```
<head>
<link rel="stylesheet" href="mystyle.css">
</head>
```

- Os estilos cascateados possuem prioridade de cascateamento:
    * estilo embutido dentro de um elemento html
    * folhas de estilo internas e externas (na seção principal)
    * padrão do navegador

- Seletores utilizados para serem aplicados ao html:
    * simples: universal(*), tag(p), id(#), classe(.)
    * combinadores: espaço em branco, ">" e "+"
    * de pseudoclasse:  :active  :focus  :hover
    * de pseudoelementos:  :first-line   :first-letter
    * de atributos:  [att~=val]  [att|=val]

**Observação:**
- Seletores mais específicos se sobrepõem aos menos estpecíficos

- Diversas aplicações do CSS:
    - Cor
    - Texto
    - Fonte
    - Background
    - etc

- Display: flex / grid




## Lógica de Programação

- Técnica de encadear pensamentos para atingir um determinado objetivo, em uma sequência lógica.

### Algoritmo
- Sequência finita de passos que levam à execução de uma tarefa.

#### Formas de representar um algoritmo
- descritivo
- fluxograma	(início, fim)
- pseudo-código		algoritmo em tópicos	início, fim (com indentação)
- notação matemática (expressões)

#### Sugestões
- somente um verbo por frase
- frases em 3a pessoa (infinitivo)
- ser objetivo
- evitar palavras com sentido dúbio

#### Fases do algoritmo
- entrada de dados
- processamento
- saída de dados




## JavaScript (JS)

- JavaScript é uma poderosa linguagem de programação que pode adicionar interatividade a um site. 
- A linguagem JS é fracamente tipada, e é aplicada juntamente com HTML e CSS.
- As variáveis JS podem ser declaradas:
    - automaticamente, onde o tipo é definido por inferência
    - usando let (escopo local)
    - usando var (escopo global)
    - const (valor constante, que não pode ser alterado)
- OBS: As palavras reservadas não podem ser usadas como nomes de variáveis.

### Operadores Relacionais
- atribuição (=)
- igualdade (==)
- diferente de (!=)
- menor que (<)
- menor ou igual (<=)
- maior que (>)
- maior ou igual (>=)

### Operações Lógicas
- and (&&)
- or (||)
- not 
