# Brief de revisão visual — landing page

Você vai revisar ** UMA landing page** (uma só, caminho informado no briefing)
com três objetivos. Nada de refazer o design: é limpeza.

## Contexto

São 20 landing pages de demonstração, uma por nicho, num mostruário
(`modelos-de-sites`). Elas já funcionam: são responsivas, animadas, têm
formulários com validação e tudo abre. O dono pediu uma **varredura de
acabamento** nesta rodada.

## Os três objetivos

### 1. SVG e arte sem sentido

Some com SVG decorativo que não quer dizer nada. Culpados comuns:

- Linhas, ondas, arcos, círculos concêntricos e "grades" decorativos no hero.
- Formas geométricas abstratas (estrela de N pontas, triângulos, cruzes).
- Ondas/"curvas" sem rótulo nem relação com o conteúdo.
- Ícones de biblioteca genérica: sparkle, raio, cubo, diamante, robô, "AI".

Regra: **cada ilustração tem que poder explicada em uma frase ligada ao
nicho.** Se não consegue, ela sai.

O que **se mantém**: ícones que representam uma ação ou serviço real da
página (agenda, carrinho,shield de seguro, grifo de dental, curto de
academia, fio de cabelo), gráficos que são dados de verdade (painel de
produto no SaaS, linha de valor nas finanças), e ilustração que tem
`role="img"` com `aria-label` descrevendo o que é.

Se remover um SVG, remova também o CSS que_existia só para ele
(`.hero-flower`, `.hero-pulse .ring`, `@keyframes` órfã, `.credenciais__deco`).

### 2. Sobreposição e composição

- Elemento absolute/fixed que invade o texto de outro (checar em 390px).
- Coluna estreita que deixa o resto da tela vazio demais. Alvo: o conteúdo
  ocupa a largura, com respiro nas bordas.
- `max-width` pequeno demais em seção de texto (abaixo de ~52ch).
- Card, badge ou botão pulando para fora do card.
- Título colidindo com o header fixo ao rolar.
- `overflow-x` escondido escondendo bug em vez de resolver.

### 3. Acabamento

- Adicionar/remover numeração decorativa do tipo `01`, `02` — o dono pediu
  para tirar. some com `<span class="num">01</span>`, `passo__num`, `tl-num`,
  `kicker` que só serve de número. **Atenção**: numeração que é conteúdo
  real (uma lista ordenada de passos de um processo que o texto referencia
  como "passo 1") pode ficar. Na dúvida, remova.
- Linha horizontal solta que não divide nada (borda de seção sem conteúdo
  dos dois lados). Mantenha apenas as que organizam algo real.
- Gradiente de caixa de contato ou de destaque. Use cor sólida.
- Emoji como ícone. Trocar por nada ou por SVG relevante.
- Seta decorativa (`→`, `↗`) repetida em todo botão.

## O que NÃO pode quebrar

Verifique ao final, antes de reportar:

1. `node --check` no JS: extraia o conteúdo de todos os `<script>` para um
   `.js` e rode `node --check`. Tem que passar.
2. Toda âncora `href="#x"` tem `id="x"` no mesmo arquivo.
3. Toda `<button>` tem handler no JS.
4. Tags balanceadas: `<div>`, `<section>`, `<header>`, `<footer>`, `<main>`,
   `<nav>`, `<article>`, `<form>`, `<style>`, `<script>`.
5. Nenhum travessão (—) no texto.
6. `prefers-reduced-motion` ainda presente e desligando as animações.
7. O rodapé ainda tem o link `../index.html` para o hub.
8. Sem `transition: all`, sem `outline: none` sem substituto visível.

Se uma mudança quebrar um desses, desfaz essa mudança.

## Como trabalhar

1. Abra o arquivo e leia o CSS e o markup.
2. Liste mentalmente: SVG decorativos, linhas soltas, numeração, gradientes
   de caixa, sobreposições prováveis.
3. Edite com a ferramenta de edição, precisa e pequena por vez.
4. Rode a verificação final.

## Relatório

Máximo 8 linhas:
- arquivo
- o que removeu (SVG/linhas/numeração/gradiente), com contagem
- o que ajustou na composição
- resultado das 8 verificações
