# Artesano

Projeto individual de HTML e CSS. Você vai construir, do zero, a página de um
estúdio de objetos a partir de um guia de estilo, um documento de
comportamento e a imagem de referência `referencia-desktop.png`.

## Antes de começar

Faça o fork para a sua conta, clone o seu fork e só então comece a
desenvolver.

## O briefing

Artesano é um estúdio de objetos aberto em 2019. Três pessoas trabalham com
barro, madeira e vidro em edições curtas: cada peça sai numerada, assinada e
com o nome de quem a fez no verso. O estúdio não vende pela internet. Vende
por catálogo impresso, quatro vezes por ano, uma coleção por estação.

Hoje quem quer o catálogo precisa pedir por telefone, e o estúdio está
perdendo pedido porque ninguém atende. A dona
contratou você para fazer a primeira página do estúdio. O pedido dela foi
direto: "uma página só, que faça a pessoa pedir o catálogo. Nada de carrinho,
nada de loja, nada de blog".

O tom também veio decidido: "não quero parecer uma marca de tecnologia". Sem
gradiente colorido, sem emoji, sem animação chamativa, sem selo de desconto.
Fotografia grande, tipografia calma e muito espaço vazio.

A página precisa funcionar tanto no computador de quem está pesquisando com
calma quanto no celular de quem viu a foto de uma peça e quer o catálogo na
hora.

## O que a página precisa ter, nesta ordem

1. **Abertura** com o nome do estúdio sobre uma foto do ateliê, as três
   palavras do estúdio (Matéria, Luz, Espaço) e a edição atual.
2. **Menu** com atalho para cada seção, que acompanhe a rolagem.
3. **Estúdio** com a frase-manifesto e as quatro etapas do trabalho
   (Matéria, Desenho, Fôrma, Entrega), cada uma com um ícone de traço fino.
4. **Coleções** em fundo escuro, com uma tabela das edições abertas:
   coleção, peça, tamanho da edição e prazo.
5. **Depoimento** de uma cliente, em uma frase só.
6. **Galeria** com três peças recentes, foto e legenda.
7. **Contato** com formulário: nome, e-mail, o que interessa (três opções em
   escolha única) e um recado opcional.
8. **Rodapé** com a marca, o ano de fundação e um link para o topo.

## O que você recebe

```
artesano/
├── img/
│   ├── hero-atelie.jpg ............. foto de abertura da página
│   ├── peca-tigela.jpg ............. peça da galeria
│   ├── peca-assento.jpg ............ peça da galeria
│   ├── peca-secagem.jpg ............ peça da galeria
│   ├── icone-materia.svg ........... ícone da etapa Matéria
│   ├── icone-desenho.svg ........... ícone da etapa Desenho
│   ├── icone-forma.svg ............. ícone da etapa Fôrma
│   └── icone-entrega.svg ........... ícone da etapa Entrega
├── referencia-desktop.png .......... como o resultado final deve parecer
├── guia-de-estilo.md ............... cores, tipografia, medidas e componentes
├── comportamento-interativo.md ..... como a página deve reagir a clique, toque, foco e rolagem
└── README.md ....................... este arquivo
```

A pasta `docs/` traz o material estendido: briefing do cliente com todos os
textos aprovados e os dados da tabela. Os textos da página estão em
`docs/03-briefing-do-cliente.md` e devem ser usados exatamente como estão.

## O que você entrega

Um `index.html` e um CSS (ex: `style.css`), organizados como preferir, que
juntos reproduzam a imagem de referência e sigam o guia de estilo e o
documento de comportamento. Uma página só, responsiva: não existe arquivo
separado para celular.

## O que você vai desenvolver

Ao concluir este projeto você terá praticado:

**HTML**
- Estrutura semântica (`nav`, `section`, `figure`, `figcaption`, `footer`,
  um `h1` na abertura e um `h2` por seção)
- Tabela com `thead`, `tbody` e `th`
- Formulários nativos: `label` ligado por `for`/`id`, `input` de texto e
  e-mail, `textarea` e campo obrigatório
- Imagens e ícones vindos de arquivo, todos guardados na pasta `img/`
- Atributos de acessibilidade básicos, como `alt` descritivo e `aria-label`

**CSS**
- Variáveis (custom properties) para cor, fonte e medida
- Reset e `box-sizing: border-box`
- Flexbox
- Camadas com `position: absolute`, `z-index` e gradiente sobre a foto
- `position: sticky` no computador e `position: fixed` no celular
- `object-fit`
- Media queries com pontos de quebra bem escolhidos
- `scroll-margin-top` para a âncora não parar atrás do menu
- Pseudo-classes de interação (`:hover`, `:focus`, `:focus-visible`) e
  pseudo-elementos como
- Tabela com rolagem horizontal em tela estreita

**Conceitos gerais**
- Ler uma especificação visual (guia de estilo, imagem de referência) e
  traduzir isso em código, decidindo você mesmo nomes de classe, variável e
  organização de arquivo
- Ler o pedido de um cliente e identificar o que ele precisa de fato, não só
  o que ele descreveu com palavras técnicas
- Sustentar um tom visual
