# Guia do professor: projeto Artesano

Material para o módulo de HTML e CSS. O projeto está pronto e funcional:
serve como referência de chegada, como base de leitura de código e como
ponto de partida para os desafios.

---

## O que tem na pasta

```
projeto-06-artesano/
├── index.html                    a página inteira, uma só, responsiva
├── css/
│   └── estilo.css                folha única, 11 blocos comentados
├── img/
│   ├── hero-atelie.jpg
│   ├── peca-tigela.jpg
│   ├── peca-assento.jpg
│   ├── peca-secagem.jpg
│   ├── icone-materia.svg
│   ├── icone-desenho.svg
│   ├── icone-forma.svg
│   └── icone-entrega.svg
├── referencia-desktop.png        captura da página no computador
├── README.md                     enunciado entregue ao aluno
├── guia-de-estilo.md             especificação visual, sem nome de classe
├── comportamento-interativo.md   como a página reage a mouse, teclado e tela
├── LEIA-ME.md                    mapa da solução pronta (este material)
└── docs/
    ├── 01-guia-de-estilo.md      o mesmo guia, com os valores exatos do CSS
    ├── 02-guia-do-professor.md   (este arquivo)
    ├── 03-briefing-do-cliente.md
    └── 04-guia-javascript.md
```

Os três arquivos da raiz (`README.md`, `guia-de-estilo.md` e
`comportamento-interativo.md`) são o que o aluno recebe para reconstruir a
página do zero, e a pasta `docs/` é o material de bastidor.

Nenhum documento entrega nome de variável nem de classe, nem mesmo o guia
detalhado da pasta `docs/`. Nomear as coisas e montar o `:root` é parte do
exercício: os guias dizem quanto vale cada medida, não como chamá-la. Os
nomes usados na solução estão só no `css/estilo.css`.

Abrir `index.html` com dois cliques funciona. Não há build, não há
dependência instalada, não há JavaScript. As fontes vêm do Google Fonts,
então a primeira abertura pede internet. Sem ela a página cai para as
fontes do sistema e continua utilizável.

---

## O que o projeto exercita

| Assunto | Onde aparece |
| --- | --- |
| Estrutura semântica | `section`, `nav`, `figure`, `figcaption`, `footer` |
| Hierarquia de títulos | um `h1` no herói, `h2` por seção |
| Âncoras internas | menu com `href="#id"` + `scroll-margin-top` |
| Imagens responsivas | `object-fit`, `aspect-ratio`, `alt` descritivo |
| Ícones em SVG | quatro arquivos em `img/`, carregados com `img` e `alt` vazio |
| Tabela | `caption`, `thead`, `tbody`, `th scope="col"` |
| Formulário | `label for`, `input required`, `fieldset`, `legend`, radios |
| Variáveis CSS | bloco 01 do `estilo.css` |
| Flexbox | menu, cabeçalhos de seção, ações do formulário |
| Grid | pilares, galeria, formulário, quadro da marca no menu |
| `position: sticky` e `fixed` | menu que acompanha a rolagem no desktop e fica preso no topo no telefone |
| Camadas com `z-index` | herói: imagem, véu, texto |
| Filtros | `contrast()`, `brightness()` |
| Responsividade sem media query | `auto-fit` nos grids, `flex-wrap` nas listas |
| Media queries | bloco 11 do `estilo.css`, três pontos de quebra |
| Estados | `:hover`, `:focus`, `:focus-visible`, `::selection` |

---

## Sugestão de sequência (8 aulas)

**Aula 1. Ler antes de escrever.**
Abrir `index.html` e o inspetor lado a lado. Pedir que identifiquem cada
`section` na página. Nenhum código escrito nesta aula.

**Aula 2. Estrutura.**
Refazer o esqueleto do zero, só HTML sem CSS: herói, menu, cinco seções,
rodapé. O resultado é feio de propósito.

**Aula 3. Variáveis e base.**
Escrever o bloco 01 e 02 do CSS: `:root`, reset, `body`, links.
Comparar com o arquivo entregue.

**Aula 4. Flexbox.**
Menu e pilares. Introduzir `gap`, `justify-content`, `flex-wrap`.

**Aula 5. Grid.**
Galeria e formulário. `repeat(auto-fit, minmax(240px, 1fr))` merece uma
aula inteira: é o que faz a página se adaptar sem media query.

**Aula 6. Tabela e formulário.**
Marcação acessível: `scope`, `label for`, `fieldset`. Testar navegação
só com Tab.

**Aula 7. Herói.**
Camadas com `position: absolute` e `z-index`, gradientes, filtros.

**Aula 8. Responsividade.**
Estreitar a janela e acompanhar o que muda sozinho, por causa do `auto-fit`
e do `flex-wrap`, e o que só muda dentro do bloco 11. São três pontos de
quebra: 1024px, 768px e 480px. Vale abrir o inspetor no ponto exato da
quebra e ver os valores trocarem de uma vez.

---

## Ideias de desafio

Da mais simples para a mais difícil. Cada uma pode virar uma tarefa
individual com prazo de uma semana.

1. **Trocar a paleta.** Mexer só no bloco 01 do `estilo.css` e produzir
   uma versão em tons de terra. Critério: nenhuma cor fora do `:root`.

2. **Nova seção.** Acrescentar "Onde encontrar" com endereço e horários,
   usando os mesmos componentes existentes. Critério: nada de classe nova
   se uma existente resolve.

3. **Trocar as fontes.** Escolher outro par no Google Fonts e ajustar a
   escala. Critério: a página tem que continuar legível em 320px.

4. **Card de peça.** Criar um quarto item na galeria com imagem própria,
   mantendo `aspect-ratio` e legendas.

5. **Menu sanduíche em CSS puro.** Abaixo de 480px, substituir a grade
   de links por um ícone que abre um painel, usando `input:checked` com
   seletor irmão. Sem JavaScript. É o desafio mais difícil da lista.

6. **Modo escuro.** Duplicar as variáveis dentro de
   `@media (prefers-color-scheme: dark)`. Critério: contraste mínimo de
   4.5:1 no texto de corpo.

7. **Página interna.** Criar `colecao-nevoa.html` reaproveitando o mesmo
   CSS, com uma lista de peças da coleção.

8. **Auditoria.** Rodar o Lighthouse e entregar um relatório de uma página
   com o que melhorou e o que não deu para resolver só com CSS.

---

## Critérios de correção sugeridos

| Peso | Critério |
| --- | --- |
| 25% | HTML válido e semântico, títulos em ordem |
| 25% | CSS sem repetição, usando as variáveis do `:root` |
| 20% | Funciona de 320px a 1440px sem rolagem horizontal |
| 15% | Acessibilidade: `alt`, `label`, foco visível, contraste |
| 15% | Fidelidade ao guia de estilo |

Descontos usuais: estilo inline no HTML, `!important` sem justificativa,
cor escrita em hex direto na regra em vez da variável, `div` onde cabia
`section` ou `figure`.

---

## Pontos de atenção na correção

- **`scroll-margin-top`.** Sem isso, o menu fixo cobre o título da seção
  ao clicar na âncora. É o erro mais comum e o mais fácil de não perceber.
- **Fonte de 16px em campos.** Abaixo disso o Safari do iPhone dá zoom
  sozinho ao focar. Está resolvido no bloco 11, na media query de 480px.
- **`overflow-x` no `body`.** Tentação comum para matar rolagem lateral, e
  o projeto não usa: qualquer valor diferente de `visible` no `body` quebra
  o `position: sticky` do menu. Quando aparecer rolagem lateral, o certo é
  achar o elemento largo demais, não escondê-lo.
- **A tabela.** Em 430px ela não cabe. A solução do projeto é rolagem
  lateral com `min-width: 460px`. Vale discutir a alternativa (virar
  lista empilhada) e por que as duas são defensáveis.
- **Alt de imagem decorativa.** O herói é ilustrativo mas informa o
  contexto do ateliê, então tem `alt` descritivo. Se fosse pura textura,
  o correto seria `alt=""`.
