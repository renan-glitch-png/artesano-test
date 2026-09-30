# Quando chegar no JavaScript: projeto Artesano

Para usar **depois** do módulo de HTML/CSS. A página foi construída de
propósito sem uma linha de JavaScript: tudo o que está aqui é uma camada
que se acrescenta a ela.

Nenhum exercício desta lista deve quebrar a página se o JavaScript falhar.
Esse é o critério que atravessa todos eles.

---

## Antes de começar

Crie `js/script.js` e ligue no fim do `<body>`:

```html
<script src="js/script.js"></script>
```

No fim do body, não no `<head>`: assim o HTML já existe quando o script roda.

---

## Nível 1: selecionar e mudar

### 1. Contador de caracteres no recado
No campo "Recado (opcional)", mostrar quantos caracteres foram digitados.

Conceitos: `querySelector`, evento `input`, `textContent`, `.value.length`.

Critério: o contador aparece só quando o usuário começa a digitar.

---

### 2. Ano automático no rodapé
Trocar "desde 2019" por "desde 2019 · hoje é 2026", com o ano vindo do
sistema.

Conceitos: `new Date().getFullYear()`.

Critério: nada de ano escrito à mão no HTML.

---

### 3. Botão "Voltar ao topo" que aparece ao rolar
O link do rodapé já funciona. Criar um botão flutuante que só aparece
depois de 400px de rolagem.

Conceitos: evento `scroll`, `window.scrollY`, `classList.toggle`,
`window.scrollTo({ behavior: 'smooth' })`.

Critério: o botão não pode cobrir o formulário no mobile.

---

## Nível 2: listas e eventos

### 4. Filtro da galeria
Acrescentar botões (Todas · Névoa · Ferro) acima da grade. Clicar filtra
as peças.

Conceitos: `data-*` no HTML, `querySelectorAll`, `forEach`, `classList`.

Critério: o botão ativo fica visualmente marcado, e "Todas" volta ao
estado inicial.

Dica: guarde a coleção de cada peça em `data-colecao="nevoa"` no `figure`.
O JavaScript só lê o atributo, não decide nada por conta.

---

### 5. Ordenar a tabela de coleções
Clicar no cabeçalho de uma coluna reordena as linhas.

Conceitos: `Array.from(tbody.rows)`, `sort`, `appendChild`,
`localeCompare` para texto, `parseInt` para números.

Critério: clicar de novo inverte a ordem. Mostrar uma seta indicando o
sentido.

Cuidado: "40 un." é texto. Extraia o número antes de comparar.

---

### 6. Menu que destaca a seção visível
Enquanto o usuário rola, o link da seção atual fica em destaque.

Conceitos: `IntersectionObserver`.

Critério: resolver com `IntersectionObserver`, não com evento `scroll`.
Vale comparar as duas abordagens em sala: a diferença de performance é
visível no inspetor.

---

## Nível 3: formulário

### 7. Validação com mensagens próprias
Substituir os avisos padrão do navegador por mensagens abaixo de cada campo.

Conceitos: `submit`, `preventDefault`, `checkValidity`, `setCustomValidity`,
manipulação de classe de erro.

Critério: os atributos `required` e `type="email"` continuam no HTML. O
JavaScript melhora a experiência, não substitui a validação nativa.

Acessibilidade: a mensagem de erro precisa de `aria-live="polite"` e o
campo inválido de `aria-invalid="true"`.

---

### 8. Confirmação sem sair da página
Ao enviar com tudo válido, esconder o formulário e mostrar uma mensagem
de confirmação com o nome digitado.

Conceitos: `preventDefault`, `FormData`, template string.

Critério: incluir um link "enviar outro pedido" que devolve o formulário.

---

### 9. Rascunho salvo
Guardar o que foi digitado e recuperar quando a página recarrega.

Conceitos: `localStorage.setItem`, `getItem`, `JSON.stringify/parse`.

Critério: limpar o rascunho depois do envio bem-sucedido.

---

## Nível 4: estrutura

### 10. Menu sanduíche no mobile
Abaixo de 480px, trocar a grade de links por um ícone que abre um painel.

Conceitos: `classList.toggle`, `aria-expanded`, fechar com `Escape`,
foco no primeiro link ao abrir.

Critério: funciona pelo teclado e o `aria-expanded` reflete o estado real.

---

### 11. Galeria vinda de um array
Tirar as três peças do HTML e gerar a grade a partir de uma lista de
objetos no JavaScript.

Conceitos: array de objetos, `map`, `innerHTML` ou
`createElement`/`append`.

Critério: comparar as duas técnicas. Discutir por que `innerHTML` com
dados de usuário é perigoso.

Observação honesta: para três peças fixas, isto é pior que o HTML direto.
O exercício vale como preparação para dados que vêm de fora, e vale dizer
isso à turma.

---

### 12. Peças de um arquivo JSON
Passo seguinte ao anterior: mover a lista para `dados/pecas.json` e buscar
com `fetch`.

Conceitos: `fetch`, `async/await`, `try/catch`, estados de carregando e
de erro.

Critério: mostrar algo enquanto carrega e uma mensagem se falhar. Precisa
de servidor local: `python3 -m http.server` resolve, e é uma boa
oportunidade para explicar por que `file://` não deixa.

---

## Regras que valem para tudo

1. **Sem `onclick` no HTML.** Todo evento é registrado no JavaScript com
   `addEventListener`.
2. **O JavaScript não cria estilo.** Ele adiciona e remove classes; a
   aparência continua no CSS.
3. **A página funciona sem o script.** Desative o JavaScript no navegador
   e verifique: o conteúdo tem que estar todo lá.
4. **Nenhuma biblioteca.** Nada de jQuery, nada de npm.
5. **`const` por padrão, `let` quando reatribuir.** `var` não aparece.
6. **Nomes em português, como no resto do projeto.** `botaoFiltro`,
   `listaPecas`.

---

## Correção sugerida

| Peso | Critério |
| --- | --- |
| 30% | Funciona como especificado |
| 25% | A página continua utilizável com JavaScript desativado |
| 20% | Código legível: nomes claros, funções curtas, sem repetição |
| 15% | Acessibilidade: teclado, `aria-*`, foco |
| 10% | Nenhum estilo escrito pelo JavaScript |
