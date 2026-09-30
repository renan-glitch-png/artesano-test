# Briefing do cliente: Artesano

Documento de entrada do projeto. Serve para o aluno reconstruir a página
sem copiar o código pronto: o briefing descreve o que o cliente pediu, e
`referencia-desktop.png`, na raiz do projeto, mostra o resultado esperado.

---

## O cliente

Artesano é um estúdio de objetos aberto em 2019. Três pessoas trabalham
com barro, madeira e vidro em edições curtas. Cada peça sai numerada,
assinada e com o nome de quem a fez no verso.

Não vendem pela internet. Vendem por catálogo impresso, quatro vezes por
ano, uma coleção por estação.

## O pedido

Uma página única que faça o visitante pedir o catálogo. Nada de carrinho,
nada de loja, nada de blog.

## Tom

Silencioso. O cliente foi explícito: "não quero parecer uma marca de
tecnologia". Sem gradientes coloridos, sem emoji, sem animação chamativa,
sem selo de desconto. Fotografia grande e sóbria, sem cor saturada. Muito
espaço vazio.

## Seções pedidas, nesta ordem

1. **Abertura** com o nome do estúdio sobre uma foto do ateliê, as três
   palavras do estúdio (Matéria, Luz, Espaço) e a edição atual.
2. **Menu** que acompanhe a rolagem, com atalho para cada seção.
3. **Estúdio** com a frase-manifesto e as quatro etapas do trabalho
   (Matéria, Desenho, Fôrma, Entrega), cada uma com um ícone de traço fino.
4. **Coleções** em fundo escuro, com uma tabela das edições abertas:
   coleção, peça, tamanho da edição e prazo.
5. **Depoimento** de uma cliente, em uma frase só.
6. **Galeria** com três peças recentes, foto e legenda.
7. **Contato** com formulário: nome, e-mail, o que interessa (três opções)
   e um recado opcional.
8. **Rodapé** com a marca, o ano de fundação e um link para o topo.

## Textos aprovados

Usar exatamente como está. O cliente revisou palavra por palavra.

**Manifesto:**
> Fazemos objetos que duram mais que nós.
>
> Um estúdio pequeno em uma rua sem saída: barro, madeira e vidro
> trabalhados devagar, em edições curtas. Cada peça sai numerada, assinada
> e com o nome de quem a fez no verso.

**Coleções, título:**
> Quatro coleções, uma por estação

**Coleções, notas:**
> Abrimos as encomendas quatro vezes por ano e fechamos quando a edição
> acaba. Nada é refeito depois: o molde é quebrado e a coleção seguinte
> começa do papel em branco.
>
> Os prazos acima contam a partir da confirmação. O frete é combinado
> peça a peça, porque nenhuma delas viaja igual.

**Depoimento:**
> "Comprei uma peça pensando em decorar uma prateleira. Ela virou a coisa
> que eu pego todos os dias, e é a única da casa que eu saberia descrever
> de olhos fechados."
> Marina Álvares, coleção Névoa

**Contato:**
> Peça o catálogo
>
> A edição de inverno abre em 14 de setembro. Deixe seu contato e enviamos
> o catálogo impresso, com as medidas e os preços de cada peça.
>
> Escrevemos de volta em até dois dias úteis.

## Dados da tabela

| Coleção | Peça | Edição | Prazo |
| --- | --- | --- | --- |
| Névoa | Vaso baixo | 40 un. | 3 semanas |
| Névoa | Prato fundo | 60 un. | 3 semanas |
| Sal | Luminária de mesa | 25 un. | 5 semanas |
| Sal | Espelho oval | 18 un. | 6 semanas |
| Ferro | Banco de canto | 12 un. | 8 semanas |
| Ferro | Cabideiro alto | 20 un. | 7 semanas |
| Vento | Móbile de vidro | 30 un. | 4 semanas |

## Ícones das etapas

Vêm prontos, em traço fino, um para cada etapa do estúdio:
`img/icone-materia.svg`, `img/icone-desenho.svg`, `img/icone-forma.svg` e
`img/icone-entrega.svg`.

## Galeria

| Peça | Material | Arquivo |
| --- | --- | --- |
| Tigela funda | Névoa · grês | `img/peca-tigela.jpg` |
| Assento de três pés | Ferro · madeira | `img/peca-assento.jpg` |
| Tigelas em secagem | Névoa · ateliê | `img/peca-secagem.jpg` |

## Requisitos técnicos

- Uma página HTML e uma folha de estilo. Sem framework.
- Sem JavaScript nesta etapa.
- Funcionar de 320px a 1440px sem rolagem horizontal.
- Todas as imagens com `alt`.
- Formulário navegável só pelo teclado, com foco visível.
- Contraste mínimo de 4.5:1 no texto de corpo.