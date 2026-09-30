# Guia de estilo do projeto Artesano

Referência de cores, fontes, medidas e componentes da landing page, com os
valores exatos usados na solução.

Nome de variável e nome de classe não aparecem aqui de propósito. Criar as
variáveis e decidir como chamar cada coisa é parte do trabalho do aluno.
Este documento diz **quanto**, não **como chamar**.

---

## 1. Cores

### Fundos

| Cor | Valor | Onde é usada |
| --- | --- | --- |
| Branco | `#ffffff` | fundo padrão da página, cartões da galeria |
| Cinza bem claro | `#f4f4f5` | seções Estúdio, Galeria e Contato |
| Grafite | `#1f2124` | seção Coleções e rodapé |
| Breu | `#16181a` | fundo do herói, sob a imagem |

### Texto

| Cor | Valor | Onde é usada |
| --- | --- | --- |
| Tinta | `#1c1c1c` | texto principal, títulos, ícones |
| Cinza médio | `#6a6a6a` | parágrafos de apoio |
| Cinza tênue | `#9a9a9a` | rótulos de formulário, rodapé |
| Neve | `#ededed` | texto sobre o herói escuro |
| Tinta suave | `#3a3a3a` | citação do depoimento |
| Cinza de hover | `#8a8a8a` | qualquer link com o mouse em cima |

### Linhas e traços

| Cor | Valor | Onde é usada |
| --- | --- | --- |
| Cinza de linha | `#ededed` | borda inferior do menu |
| Cinza de campo | `#dcdcdc` | borda dos campos do formulário |
| Cinza de traço | `#c4c4c4` | tracinho de 48px sob os títulos |
| Bronze | `#9d938c` | tracinho de 26px sob os ícones |
| Grafite claro | `#2c2f33` | divisórias das linhas da tabela |
| Grafite mais claro | `#3a3d41` | divisória do cabeçalho da tabela |
| Cinza de risco | `#6f7276` | risco ao lado das palavras do herói |
| Cinza de barra | `#85888c` | barras entre as palavras do herói |

### Verde-sálvia (acento)

| Cor | Valor | Onde é usada |
| --- | --- | --- |
| Sálvia claro | `#e7ebdf` | texto da tabela sobre o grafite, botão vazado |
| Sálvia médio | `#68764f` | assinatura do depoimento |
| Sálvia escuro | `#2f3524` | legendas das peças na galeria |

**Regra:** nenhuma cor nova sem entrar nesta lista, e nenhum hex escrito
direto na regra. Toda cor da lista vira uma variável no `:root`, e o resto
do CSS só usa a variável. Se precisar de um tom intermediário, use um dos
existentes antes de inventar outro.

---

## 2. Tipografia

Duas famílias, carregadas do Google Fonts:

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;1,300&family=Jost:wght@300;400;500&display=swap">
```

| Papel | Família | Pesos |
| --- | --- | --- |
| Títulos e citação | Cormorant Garamond (serifada) | 300, mais o itálico 300 na citação |
| Texto, menu, formulário | Jost (sem serifa) | 300 e 400 |

Cada família também vira uma variável, com a pilha de reserva junto: a
serifada cai em Georgia, a sem serifa cai na fonte do sistema. Sem internet
a página continua legível.

### Escala

São quatro degraus, um por faixa de largura: acima de 1024px, até 1024px,
até 768px e até 480px.

| Elemento | Computador | Notebook | Tablet | Celular |
| --- | --- | --- | --- | --- |
| Nome da marca no herói | 84px | 68px | 50px | 40px |
| Título de seção (`h2`) | 44px | 38px | 32px | 30px |
| Citação | 23px | 21px | 19px | 19px |
| Parágrafo | 16px | 15px | 15px | 15px |
| Corpo da tabela | 14px | 14px | 14px | 13px |
| Links do menu | 11px | 11px | 11px | 10px |
| Rótulos e legendas | 10px | 10px | 10px | 10px |
| Campos do formulário | 15px | 15px | 15px | 16px |

Os quatro títulos de seção têm sempre o mesmo tamanho, então mudam juntos,
em uma regra só com os quatro seletores separados por vírgula.

Todos os tamanhos são fixos, em pixel. Quem escreve o CSS declara o valor
cheio na regra normal e reduz dentro das media queries. O texto muda de
tamanho de uma vez, no ponto de quebra, em vez de crescer aos poucos junto
com a janela.

### Espaçamento entre letras

Todo texto pequeno em caixa alta recebe `letter-spacing`. É a
assinatura visual da página: sem isso os rótulos de 10px ficam apertados e
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

- Parágrafos: `1.85` (bem arejado, é intencional)
- Títulos: `1.2`
- Citação: `1.7`

---

## 3. Bordas e cantos

| Elemento | Raio |
| --- | --- |
| Campos de formulário | `2px`, quase reto |
| Botões | `999px`, pílula completa |

Os dois raios também merecem variável, porque se repetem. Tudo o mais tem
canto reto: cartões da galeria, seções, tabela. A página é geométrica de
propósito.

Bordas são sempre de **1px**. Não existe borda de 2px ou 3px no projeto.

---

## 4. Medidas e espaçamento

| Medida | Valor | Uso |
| --- | --- | --- |
| Largura máxima do conteúdo | `1080px` | menu, galeria e rodapé |
| Altura da barra do menu | `68px`, e `70px` no telefone | a mesma medida vale para o `scroll-margin-top` das seções |

A altura do menu precisa ser variável, não número solto: ela aparece na
barra e de novo no `scroll-margin-top` de cada seção. Trocar em um lugar só
faz a âncora parar no lugar errado.

Larguras de leitura menores por seção: 780px no manifesto, 880px nas
coleções, 720px no depoimento, 620px no formulário. Parágrafos usam
`max-width` em `ch` (46ch a 62ch) para nunca passar de cerca de 60
caracteres por linha.

### Padding vertical das seções

| Seção | Computador | Notebook | Tablet | Celular |
| --- | --- | --- | --- | --- |
| Herói | 120px | 112px | 96px | 96px |
| Estúdio | 128px | 104px | 68px | 64px |
| Demais seções | 104px | 88px | 62px | 60px |
| Rodapé | 54px | 48px | 40px | 40px |

Padding lateral: 64px no computador, 48px no notebook, 32px no tablet e
24px no celular.

O herói também tem `min-height`: 640px no computador e 560px no celular.
Altura fixa, não fração da janela, para o menu não sair da tela em um
notebook de tela baixa.

---

## 5. Imagens

As fotos ficam coloridas, com um leve ajuste de contraste e brilho:

```css
filter: contrast(1.04);                  /* galeria */
filter: contrast(1.06) brightness(.82);  /* herói */
```

As peças da galeria usam `aspect-ratio: 4 / 3` com `object-fit: cover`,
então todas ficam do mesmo tamanho independente do arquivo original.

O herói tem duas camadas de gradiente escuro por cima da foto, em um
elemento próprio, para o texto branco ter contraste garantido.

Os quatro ícones das etapas do estúdio são arquivos SVG na pasta `img/`,
carregados com `img` e `alt` vazio, porque são decorativos. Cada arquivo
mede 34px, tem traço de 1px, sem preenchimento, e leva a cor de tinta
dentro dele. No celular o CSS reduz os quatro para 30px. Consequência de
usar arquivo em vez de SVG escrito no HTML: o CSS da página não alcança o
traço, então trocar a cor do ícone quer dizer editar o arquivo.

---

## 6. Componentes

### Botão cheio
Fundo de tinta, texto branco, pílula. No `:hover` inverte: fundo branco,
texto escuro. Altura mínima 48px.

### Botão vazado
Só borda, sobre fundo escuro, em sálvia claro. No `:hover` fica com fundo
branco e texto grafite.

### Tracinho
48px × 1px em cinza de traço. Aparece sob os títulos de seção. É o único
elemento decorativo da página, e volta menor, com 26px, sob cada ícone.

### Campo de formulário
Rótulo acima, campo abaixo, `gap: 9px`. Borda de 1px que passa para a cor
de tinta no `:focus`.

### Quadro da inicial no menu
Quadrado de 42px, 36px no telefone, só com borda fina. A borda usa
`currentColor` para clarear junto com a letra no `:hover`.

---

## 7. Estados de interação

| Estado | Regra |
| --- | --- |
| Link `:hover` | cor passa ao cinza de hover (`#8a8a8a`) |
| Botão `:hover` | inverte fundo e texto, transição de `.2s` |
| Campo `:focus` | borda passa à cor de tinta, `outline: none` |
| Teclado `:focus-visible` | `outline: 1px solid` na cor de tinta, com `offset: 3px` |
| Seleção de texto | fundo de tinta, texto branco |

Nunca deixe o contorno azul padrão do navegador sumir. Ele existe por
acessibilidade: troque a aparência dele à vontade, mas nunca remova sem
colocar outra indicação de foco no lugar.

---

## 8. O que não fazer

- Não usar cantos arredondados fora dos botões e campos.
- Não usar sombras. A página é plana; a separação vem de fundo e linha fina.
- Não usar mais de duas fontes.
- Não usar negrito acima de 400. O peso 300 é a voz do projeto.
- Não usar mais de dois fundos escuros por página.
- Não colocar texto pequeno em caixa alta sem `letter-spacing`.
