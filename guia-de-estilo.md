# Guia de estilo - Artesano

Referência visual do projeto: cores, tipografia, medidas e componentes.
Este guia descreve a aparência, não o código. Nenhum nome de variável, classe
ou atributo aparece aqui de propósito: quem for reconstruir a página decide
como nomear as coisas.

## 1. Cores

A paleta é quase toda em cinzas. O verde-sálvia é o único acento e aparece
pouco, sempre em texto pequeno.

### Fundos

| Cor | Valor | Onde aparece |
| --- | --- | --- |
| Branco | `#ffffff` | fundo padrão da página e dos cartões da galeria |
| Cinza bem claro | `#f4f4f5` | fundo das seções de estúdio, galeria e contato |
| Grafite | `#1f2124` | fundo escuro da seção de coleções e do rodapé |
| Breu | `#16181a` | fundo atrás da foto de abertura, enquanto a imagem carrega |

### Texto

| Cor | Valor | Onde aparece |
| --- | --- | --- |
| Tinta | `#1c1c1c` | títulos, texto corrido, ícones e o botão principal |
| Cinza médio | `#6a6a6a` | parágrafos de apoio |
| Cinza tênue | `#9a9a9a` | rótulos de formulário, aviso do formulário e rodapé |
| Neve | `#ededed` | todo o texto sobre a abertura escura |
| Tinta suave | `#3a3a3a` | citação do depoimento |
| Cinza de hover | `#8a8a8a` | qualquer link com o mouse em cima |

### Linhas e traços

| Cor | Valor | Onde aparece |
| --- | --- | --- |
| Cinza de linha | `#ededed` | borda de baixo do menu |
| Cinza de campo | `#dcdcdc` | borda dos campos de formulário em repouso |
| Cinza de traço | `#c4c4c4` | tracinho decorativo sob os títulos de seção |
| Bronze | `#9d938c` | tracinho menor sob cada ícone |
| Grafite claro | `#2c2f33` | divisórias entre as linhas da tabela |
| Grafite mais claro | `#3a3d41` | divisória sob o cabeçalho da tabela |
| Cinza de risco | `#6f7276` | risco ao lado das três palavras da abertura |
| Cinza de barra | `#85888c` | barras entre as três palavras da abertura |

### Verde-sálvia, o acento

| Cor | Valor | Onde aparece |
| --- | --- | --- |
| Sálvia claro | `#e7ebdf` | texto da tabela sobre o fundo escuro e o botão de contorno |
| Sálvia médio | `#68764f` | assinatura do depoimento |
| Sálvia escuro | `#2f3524` | legendas das peças na galeria |

Nenhuma cor nova fora desta lista. Se precisar de um tom intermediário, use
um dos que já existem antes de inventar outro.

## 2. Tipografia

Duas famílias. Uma serifada, em peso leve, para títulos e para a citação do
depoimento. Uma sem serifa, em pesos leve e normal, para todo o resto: menu,
texto corrido, tabela, formulário e rodapé. Sem conexão à internet o
navegador usa as fontes do sistema no lugar delas, sem quebrar o layout.

Nada no projeto passa do peso 400. O texto leve é a voz da marca.

A página tem quatro degraus de tamanho. Cada coluna abaixo vale para uma
faixa de largura de tela:

- **Computador**: acima de 1024px
- **Notebook**: até 1024px
- **Tablet**: até 768px
- **Celular**: até 480px

| Onde | Fonte | Computador | Notebook | Tablet | Celular |
| --- | --- | --- | --- | --- | --- |
| Nome do estúdio na abertura | sem serifa, 400 | 84px | 68px | 50px | 40px |
| Título de cada seção | serifada, 300 | 44px | 38px | 32px | 30px |
| Citação do depoimento | serifada, 300, itálica | 23px | 21px | 19px | 19px |
| Texto corrido | sem serifa, 300 | 16px | 15px | 15px | 15px |
| Corpo da tabela | sem serifa, 300 | 14px | 14px | 14px | 13px |
| Notas abaixo da tabela | sem serifa, 300 | 14px | 14px | 14px | 14px |
| Nome da peça na galeria | sem serifa, 300, caixa alta | 13px | 13px | 13px | 13px |
| Material da peça | sem serifa, 300, caixa alta | 12px | 12px | 12px | 12px |
| Links do menu | sem serifa, 300, caixa alta | 11px | 11px | 11px | 10px |
| Rótulos, legendas, cabeçalho de tabela, botões e rodapé | sem serifa, 300, caixa alta | 10px | 10px | 10px | 10px |
| Campos de formulário | sem serifa, 300 | 15px | 15px | 15px | 16px |

Onde a linha repete o mesmo número nas quatro colunas, o tamanho não muda em
tela nenhuma. Onde os números diferem, a mudança acontece de uma vez, no
ponto de quebra, e não aos poucos.

### Espaçamento entre letras

Todo texto pequeno em caixa alta recebe espaçamento entre letras. É a
assinatura visual do projeto: sem isso os rótulos de 10px ficam apertados e
ilegíveis.

São três valores para a página inteira, não um por elemento:

| Valor | Onde |
| --- | --- |
| `0.14em` | nome do estúdio na abertura |
| `0.26em` | todo texto pequeno em caixa alta |
| `0.40em` | os dois acentos largos: o ano na abertura e a marca do rodapé |

O valor do meio cobre menu, rótulos, legendas, títulos de grupo do
formulário, cabeçalho e título da tabela, nome das quatro etapas, nome e
material das peças, botões, assinatura do depoimento e as três palavras da
abertura. Nenhum deles tem valor próprio.

Duas observações sobre os outros dois valores. O nome do estúdio é texto de
exibição, muito maior que o resto, e texto grande precisa de
proporcionalmente menos respiro entre as letras. O ano e a marca do rodapé
são largos de propósito: é o único lugar onde o espaçamento vira ornamento.

Uma exceção fora da escala: a inicial dentro do quadro do menu usa `0.04em`,
quase nada, porque é uma letra sozinha e o espaçamento normal só empurraria
ela para fora do centro do quadro.

**Por que `em` e não `px`:** o `em` mede em relação ao tamanho da letra do
próprio elemento. Os links do menu têm `0.26em`: isso vale 2,86px enquanto a
fonte é de 11px e vira 2,6px sozinho quando ela cai para 10px no celular. O
mesmo acontece com todo rótulo e legenda que muda de tamanho de uma faixa
para outra. Em pixel, cada tamanho de fonte precisaria do seu próprio valor
de espaçamento, e a lista voltaria a ter um número por elemento, repetido
dentro de cada media query.

O `em` também mantém a mesma proporção entre elementos de tamanhos
diferentes. É por isso que o rótulo de 10px e o nome do estúdio de 84px
pertencem à mesma página: o respiro entre as letras é proporcional, não
igual em pixel.

### Altura de linha

- Parágrafos: `1.85`, bem arejado, de propósito.
- Títulos: `1.2`.
- Citação do depoimento: `1.7`.

## 3. Medidas, bordas e espaçamento

- Largura máxima do conteúdo: `1080px`, centralizado.
- Larguras de leitura menores dentro das seções: `780px` no manifesto,
  `880px` nas coleções, `720px` no depoimento, `620px` no formulário.
- Nenhum parágrafo passa de cerca de 60 caracteres por linha.
- Respiro nas laterais: `64px` no computador, `48px` no notebook, `32px` no
  tablet e `24px` no celular.
- Distância entre o topo e o fim de cada seção, por faixa de largura:

| Seção | Computador | Notebook | Tablet | Celular |
| --- | --- | --- | --- | --- |
| Abertura | `120px` | `112px` | `96px` | `96px` |
| Estúdio | `128px` | `104px` | `68px` | `64px` |
| Demais seções | `104px` | `88px` | `62px` | `60px` |
| Rodapé | `54px` | `48px` | `40px` | `40px` |

- Altura mínima da abertura: `640px` no computador e `560px` no celular.
- Altura da barra do menu: `68px` no computador e `70px` no celular.
- Espessura das bordas: `1px` sempre. Não existe borda de 2px no projeto.
- Cantos: retos em tudo, menos nos campos de formulário, que têm `2px`, e nos
  botões, que são pílulas completamente arredondadas.
- Espaço entre os cartões da galeria: `26px` no computador, `22px` no
  notebook e `18px` do tablet para baixo.
- Espaço entre campos do formulário: `34px` no computador, `32px` no
  notebook, `26px` no tablet e `24px` no celular.
- Sem sombra em lugar nenhum. A separação vem do fundo e da linha fina.

## 4. Botões e links

Dois tipos de botão, os dois em pílula, com texto de 10px em caixa alta:

- **Botão principal**: fundo escuro, texto branco. É o de enviar o
  formulário.
- **Botão de contorno**: só a borda, em sálvia claro, usado sobre o fundo
  escuro das coleções.

Fora deles existe apenas um link de texto sublinhado, no rodapé, para voltar
ao topo. Os links do menu ficam na cor do texto comum e sem sublinhado.

## 5. Campos de formulário

- Campo de texto de uma linha, para nome e para e-mail.
- Grupo de escolha única com três opções, uma marcável por vez, dentro de um
  bloco com título próprio.
- Área de texto de várias linhas, redimensionável só na vertical.

Todos os campos têm a mesma borda, o mesmo canto e o mesmo espaçamento
interno. O rótulo fica acima do campo, em 10px caixa alta, na cor mais tênue.
O texto de exemplo dentro de um campo vazio aparece mais claro que o texto
digitado. Nome e e-mail ficam lado a lado quando cabem; o bloco de opções e a
área de texto ocupam sempre a linha inteira.

## 6. Componentes

**Abertura**: foto do ateliê ocupando toda a área, com duas camadas de
escurecimento por cima para o texto branco ter contraste garantido em
qualquer foto. O conteúdo fica centralizado na vertical e na horizontal: nome
do estúdio, as três palavras separadas por barras e ladeadas por um risco
fino, a linha da edição atual e o ano. As três palavras ficam sobre uma
faixa branca bem translúcida, quase imperceptível, que as descola da foto.

**Menu**: os links ficam centralizados na barra, em caixa alta e sem
sublinhado, com o quadro da inicial do estúdio no meio deles: um quadrado de
`42px` só com borda fina, que clareia junto com a letra quando o mouse
passa por cima. No celular o quadro passa para a ponta esquerda da
barra, com `36px`, e os links se organizam ao lado dele.

**Tracinho**: um traço horizontal de `48px` por `1px`, sob os títulos de
seção. É o único elemento decorativo da página, e aparece em versão menor,
de `26px`, sob cada ícone do estúdio.

**Etapas do estúdio**: quatro blocos iguais, cada um com um ícone de traço
fino, o tracinho menor e o nome em caixa alta. Os ícones vêm prontos, como
arquivos SVG na pasta `img/`: são desenhos de 34px, 30px no celular, em
traço de 1px sem preenchimento. Eles são decorativos, e o nome escrito
abaixo já diz o que cada etapa é.

**Tabela de coleções**: fundo escuro, cabeçalho em caixa alta e tamanho
reduzido, uma linha fina separando cada linha de conteúdo e a última linha
sem divisória. Um título curto em caixa alta aparece acima da tabela,
centralizado. As colunas de quantidade e prazo nunca quebram no meio.

**Cartão de peça**: foto em proporção `4 / 3`, cortada para preencher, e
abaixo dela, centralizados, o nome da peça e o material, os dois em caixa
alta. Fundo branco sobre a seção cinza.

**Fotos**: a foto da abertura e as fotos da galeria recebem um leve ajuste de
contraste; a da abertura também escurece um pouco, para o texto por cima
continuar legível.

**Rodapé**: fundo escuro, tudo centralizado em coluna, com a marca em cima, a
linha de assinatura no meio e o link de voltar ao topo embaixo, sublinhado.
