# Comportamento esperado na tela - Artesano

Este documento descreve como a página deve reagir à interação: o que muda ao
passar o mouse, clicar, navegar pelo teclado ou reduzir a largura da tela.
Tudo isso é resolvido só com HTML e CSS, sem nenhum JavaScript.

## 1. Rolagem da página

- **No computador**, o menu fica logo abaixo da foto de abertura e acompanha
  a rolagem: assim que a página sobe até ele, ele gruda no topo da tela e
  continua visível, sempre por cima do restante do conteúdo.
- **No celular**, o menu fica preso no topo desde o começo, por cima da foto
  de abertura, e nunca sai da tela.
- Ao clicar em um link que aponta para um ponto da própria página, a rolagem
  até lá é suave, não instantânea.
- A seção de destino para logo abaixo da barra do menu. O título nunca fica
  escondido atrás dela, nem no computador nem no celular, onde a barra é mais
  alta.

## 2. Links

- Os links do menu ficam na cor do texto comum, sem sublinhado, e clareiam
  para um cinza médio ao passar o mouse.
- O quadrado com a inicial do estúdio, no menu, é um link para o topo: um
  quadrado de borda fina, sem preenchimento. Ao passar o mouse, a letra e a
  borda clareiam juntas, no mesmo cinza dos outros links. A borda nunca fica
  para trás, escura, enquanto a letra clareia.
- O único link sublinhado da página é o "voltar ao topo" do rodapé, com o
  sublinhado afastado do texto.

## 3. Botões

- **Botão principal** (enviar o formulário): em repouso tem fundo escuro e
  texto branco; ao passar o mouse ele inverte, ficando com fundo branco,
  texto escuro e a borda visível. A troca é suave, em cerca de dois décimos
  de segundo.
- **Botão de contorno** (pedir o catálogo, sobre o fundo escuro): em repouso
  é só a borda clara; ao passar o mouse ganha fundo branco e texto grafite,
  com a mesma transição.

## 4. Campos de formulário

- Ao clicar em um campo de texto ou a área de texto, a borda
  escurece, indicando que ele está ativo.
- Clicar no rótulo do campo também dá foco ao campo correspondente, e clicar
  no texto de uma opção marca a opção, não só o círculo.
- As opções de escolha única usam a cor de texto do projeto quando marcadas,
  não o azul padrão do navegador.
- O nome e o e-mail são obrigatórios; o recado é opcional. A validação é a
  nativa do navegador, sem mensagem personalizada.
- A área de texto pode ser esticada pelo usuário, mas só na vertical.

## 6. Galeria, tabela e fotos

- Não existe nenhum efeito ao passar o mouse sobre as fotos, os cartões da
  galeria ou as linhas da tabela. A página é silenciosa de propósito: quem
  passa o mouse não vê nada acontecer fora dos links e dos botões.
- As fotos das peças ficam todas do mesmo tamanho, mesmo vindo de arquivos de
  proporções diferentes: elas são cortadas para preencher o espaço, nunca
  esticadas.

## 7. Comportamento ao redimensionar a tela

Texto e respiro mudam em três pontos de quebra: 1024px, 768px e 480px. A
mudança acontece de uma vez, no ponto exato, e não aos poucos: entre um
ponto e outro os tamanhos ficam parados. Os valores de cada faixa estão no
guia de estilo.

- **Largura ampla (computador)**: o menu ocupa uma linha só, com os seis
  links centralizados e o quadro da inicial no meio deles. As quatro etapas
  do estúdio ficam lado a lado; a galeria mostra as três peças em uma linha;
  nome e e-mail dividem a mesma linha do formulário.
- **Largura intermediária (tablet)**: os espaços do menu diminuem e, quando
  os links deixam de caber, eles quebram para uma segunda linha, sempre
  centralizados. As etapas do estúdio passam para duas colunas e a galeria
  vai reduzindo o número de colunas sozinha, conforme o espaço. A tabela
  deixa de espremer as colunas e passa a rolar de lado dentro da própria
  caixa, sem afetar o restante da página.
- **Largura estreita (celular)**: galeria e formulário passam para uma única
  coluna. O menu vira uma grade: o quadro da inicial vai para a ponta
  esquerda, ocupando a altura toda da barra, e os seis links se organizam em
  duas linhas de três, e a barra passa a ficar fixa no topo. Os botões
  ocupam a largura toda, as opções de escolha única se empilham separadas
  por linhas finas, e cada opção, campo e botão tem pelo menos 48px de
  altura, para o dedo acertar sem esforço. Os campos de formulário chegam a
  16px, porque abaixo disso o navegador do iPhone dá zoom sozinho ao focar
  o campo.
- Em nenhuma largura, de 320px a 1440px, a página inteira rola de lado. A
  única rolagem horizontal permitida é a da tabela, dentro da caixa dela.
