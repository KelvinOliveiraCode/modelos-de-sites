# Regras de execução (valem para cada uma das 20 landings)

Leia junto com a sua seção em `spec/nichos.md`. O que está aqui não é
sugestão.

## Arquivo

- Um único arquivo: `<slug>/index.html`. Autossuficiente.
- CSS no `<style>`, JS no `<script>` no fim do `<body>`. Nada de build,
  nada de npm, nada de framework.
- Única dependência externa: Google Fonts (`<link>` no `<head>`).
- `<html lang="pt-BR">`, `<meta name="viewport">`, `<title>` descritivo,
  `<meta name="description">` com uma frase real do nicho.
- Links relativos: voltar ao hub é `../index.html`.

## Semântica e acessibilidade

- `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`, `<article>`.
- Um `<h1>` só. Hierarquia de headings sem pular nível.
- Todo link e botão têm texto acessível. Ícone sozinho: `aria-label`.
- Foco visível em tudo que é interativo (`:focus-visible`). Nunca
  `outline: none` sem substituto.
- Botões com 44px de altura mínima no toque.
- Imagens: `alt` descritivo, ou vazio se decorativa. Sem `<img>` externo:
  o que seria foto é um bloco placeholder com `role="img"` e `aria-label`,
  ou SVG inline.
- Contraste AA: texto normal 4.5:1, texto grande (18px+ ou 14px negrito)
  3:1. Texto sobre cor de nicho sempre conferido.
- `@media (prefers-reduced-motion: reduce)` desligando animação.

## Mobile (320px primeiro)

- Um único breakpoint principal em 760px, mais um em 480px se precisar.
- Nada de overflow horizontal. Grade vira coluna única.
- Nav vira menu que abre e fecha de verdade (botão, `aria-expanded`,
  fecha com Escape, fecha ao clicar em link).
- Nada de `position: absolute` em texto que dependa de largura fixa.
- Nada de `100vh` isolado para herói em mobile (use `min-height` com
  `dvh` ou padding).

## Interações obrigatórias (todas de verdade)

Toda landing precisa de, no mínimo:

1. **Menu mobile** funcional.
2. **Scroll reveal** com `IntersectionObserver`, escalonado por
   `--i` nos filhos. Nunca animar tudo ao mesmo tempo.
3. **Header que reage ao scroll** (fundo aparece, sombra sutil).
4. **Duas interações próprias do nicho** (as que estão no dossiê: acordeão,
   abas, calculadora, filtro, formulário...).
5. **Formulário** com validação por campo, mensagem de erro e estado de
   sucesso visível. Não envia para lugar nenhum, e não finge que envia:
   confirma na tela.
7. **Estado vazio** onde há lista que pode ficar vazia (busca, simulador,
   seletor).

## Animação (pacote mínimo obrigatório por landing)

"Bem animado" aqui é requisito de entrega, não enfeite. Toda landing entrega
este pacote completo:

1. **Entrada de página**: escalonada, com `opacity` + `translateY`, via
   classe no `<body>` depois do load. Nada de piscar.
2. **Scroll reveal** em `IntersectionObserver`, com `--i` por filho
   (atraso de 60 a 90ms entre irmãos). Nada de animar a seção inteira de uma
   vez.
3. **Um gesto por seção**: cada `<section>` tem UMA animação própria, e os
   gestos se repetem o mínimo possível entre seções.
4. **Uma animação de herói contínua**, lenta (8s ou mais por ciclo), em
   `transform`/`opacity`/`stroke`. É a assinatura do nicho.
5. **Um SVG animado**: linha que desenha (`stroke-dasharray`), forma que
   gira, caminho que preenche, ou partícula que flutua.
6. **Parallax leve** em pelo menos um elemento (0.1 a 0.3 de fator), com
   `requestAnimationFrame` e nunca em mobile (`matchMedia`).
7. **Hover com transição** em todo card, botão e link de navegação.
8. **Troca de estado animada**: acordeão, aba, carrossel ou filtro com
   transição de altura/opacidade, não corte seco.
9. **Header que reage ao scroll** (fundo, sombra, encolhimento sutil).
10. **`scroll-behavior: smooth`** para âncoras internas.

Critérios de suavidade (obrigatórios):

- Só `transform`, `opacity`, `filter`, `stroke-*` em animação contínua.
  Nada de `width`, `top`, `left`, `margin` em loop.
- `will-change` só no que está animando agora, e sem exagero.
- Easing: `cubic-bezier(.22,1,.36,1)` para entrada, `cubic-bezier(.4,0,.2,1)`
  para estado. Nunca `linear` em movimento de interface.
- Duração: 450 a 900ms para reveal, 150 a 250ms para hover, 6s ou mais para
  loop de herói. Nada acima de 1s exceto loop.
- `animation-fill-mode: both` onde precisa, e `@media (prefers-reduced-motion:
  reduce)` desligando tudo que não for essencial.
- `requestAnimationFrame` para scroll, nunca handler de `scroll` solto.

## Movimento

- Propósito por animação, anotado em comentário curto no CSS ou JS quando
  não for óbvio.
- Nunca `transition: all`. Sempre propriedade nomeada.
- Nunca animar `top/left/width/height` em loop. Use `transform` e
  `opacity`.
- Nada de fade-up em tudo. Cada seção tem UM gesto, e os gestos variam.
- Respeitar `prefers-reduced-motion`.

## Proibido (vai reprovar no gate)

- Travessão (—) em qualquer texto.
- `linear-gradient` azul para roxo, azul para ciano, roxo para rosa, como
  cor de decoração. Só com razão de marca escrita.
- Glassmorphism em navbar, cards, modal e sidebar ao mesmo tempo.
- Card com tarja colorida na esquerda.
- Três cards iguais (mesmo tamanho, ícone, padding) como grid de features.
- Bento grid, terminal falso como herói, "confiado por" com logo genérico.
- Número, nota, depoimento, cliente ou selo sem fonte real. Use placeholder
  entre colchetes.
- CTA genérico: Saiba mais, Comece agora, Descubra, Experimente.
- Emoji como ícone de interface.
- Seta (→ ↗) em todo link.
- Ícone de biblioteca genérica colado sem relação com o conteúdo.
- `outline: none`, `user-scalable=no`, texto com `font-size` menor que 14px
  em corpo.
- Lorem ipsum.

## Placeholders (como escrever)

- Marca: `Sua Marca` (nunca um nome inventado que pareça real).
- Logo: bloco com `[LOGO]` em mono, ou o nome em tipografia.
- Foto: bloco com `aria-label="espaco para foto: descricao"` e rótulo
  visível curto (`Sua foto aqui`).
- Dado real: `[+1.200 clientes atendidos]`, `[nota 4,9 de 5]`.
- Depoimento: `[depoimento real]` + `[nome do cliente]`.
- Preço: `[R$ 00]` ou `R$ 00 (definir)`.
- Endereço, telefone, e-mail: `[endereco]`, `[(00) 00000-0000]`,
  `[seu@email.com]`. O WhatsApp e o e-mail do dono (Kelvin) são reais e
  estão no bloco de contato do hub, não aqui.

## Contato dentro da landing

A landing é do cliente, então o contato é do cliente (placeholder). No
rodapé, uma linha única: "Modelo de demonstração por Kelvin Oliveira" com
link para `../index.html`.

## Entrega

Antes de dizer que terminou:

1. Confirme que o arquivo existe e o tamanho.
2. Grep no próprio arquivo por `—` (travessão): não pode retornar nada.
3. Grep por `lorem`: não pode retornar nada.
4. Confira que todo `href="#x"` tem um `id="x"` no mesmo arquivo.
5. Confira que todo botão tem handler.
6. Reporte: arquivo, seções, interações, o que verificou.
