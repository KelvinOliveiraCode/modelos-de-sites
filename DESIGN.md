# DESIGN.md — Modelos de Sites (mostruário)

> Direção de design do hub e dos 20 modelos de landing page.
> Este arquivo é a **fonte de verdade**. O hub e cada landing são construídos
> a partir daqui, não a partir de gosto pessoal do momento.

---

## 1. O que é este produto

Um **mostruário**. O cliente entra, vê 20 modelos de landing page, cada um de um
nicho diferente, e entende como o trabalho é feito. Depois faz o próprio site.

Consequências de desenho:

- O hub é **catálogo**, não landing. Superfície "Catalog" (Stage 1 do
  workflow): filtro + grid/lista, sem hero decorativo.
- Cada landing é **exemplo real de nicho**, com copy escrita para aquele
  nicho. Não é wireframe cinza.
- Nada aqui é produto final: **placeholders explícitos** onde entraria dado
  real do cliente (`Sua Marca`, `[LOGO]`, `[depoimento real]`).

## 2. Dials (hub)

```
Leitura: catálogo de modelos para donos de negócio, em linguagem de
mostruário de agência, dial ENERGY 2 / RHYTHM 2 / MOTION 2.
```

| Dial | Valor | Por quê |
|---|---|---|
| ENERGY | 2 | Vitrine precisa de personalidade, não de impacto de agência. |
| RHYTHM | 2 | Grid consistente com uma quebra: o destaque do modelo em foco. |
| MOTION | 2 | Reveal no scroll, hover nos cards, transição de filtro. |

## 3. Paleta do hub

Derivada do escuro do portfólio (`#050505`, `#f1f1ee`, dourado), para o hub
parecer continuação do mesmo trabalho, não um site à parte.

| Token | Valor | Papel |
|---|---|---|
| `--ink` | `#0B0B0C` | fundo |
| `--ink-2` | `#131315` | superfície elevada (card, header) |
| `--line` | `rgba(241,241,238,.12)` | borda sutil |
| `--paper` | `#F4F3EF` | texto principal |
| `--paper-dim` | `#A6A6A0` | texto secundário (4.6:1 sobre `--ink-2`) |
| `--accent` | `#E8B33A` | ação e destaque (um só) |
| `--accent-ink` | `#0B0B0C` | texto sobre o accent |

**Um acento só.** A cor do nicho aparece apenas como fita/swatch no card, nunca
como segunda cor de interface. Isso evita o hub virar arco-íris de 20 paletas.

## 4. Tipografia do hub

- Display: `Archivo` (700/800). Razão: neutra e firme, não grita, deixa o
  swatch de cor ser a única cor do card.
- Corpo: `Inter` (400/500). Leitura longa em 2 colunas.
- Mono: `JetBrains Mono` (400/500) só em rótulos técnicos: slug, contagem,
  `[LOGO]`. Razão: marca o que é metadado, não conteúdo.

## 5. Estrutura do hub

1. **Header fixo** — nome, contagem de modelos, filtro, botão de contato.
2. **Intro curta** (2 linhas) — o que é, e como pedir o seu.
3. **Filtro + busca** — por segmento (saúde, tech, comida...) e por texto.
4. **Grid de modelos** — card com preview de cor, nome, nicho, uma linha de
   proposta, link "Ver modelo".
5. **Como funciona** — 3 passos reais do processo (brief, build, publicação).
6. **Contato** — "Faça o seu site também", WhatsApp, e-mail, LinkedIn.
7. **Footer** — nota de que são modelos de demonstração, link pro portfólio.

## 6. Regras que valem para as 20 landings

Vêm de `antislop` (core) e são verificadas no gate de entrega:

- **Sem dado inventado.** Nenhum número, depoimento, cliente ou selo sem fonte.
  Onde entra dado real: placeholder marcado.
- **Sem seção template.** Nada de "hero + 3 cards iguais + depoimentos + FAQ +
  CTA" na mesma ordem em toda página. Cada nicho tem composição própria.
- **Placeholders visíveis.** `Sua Marca`, `Sua Logo`, `[depoimento real]`,
  `[preço]`. Nunca disfarçados de final.
- **CTA específico.** "Get Started" não existe aqui. É "Agendar avaliação",
  "Falar no WhatsApp", "Ver o cardápio".
- **Todo link funciona.** Navegação só com destino real (dentro da própria
  landing, `mailto:`, `wa.me` com número real, ou voltar pro hub).
- **Mobile primeiro.** 320px sem overflow, alvo de toque 44px, nav que vira
  menu de verdade.
- **Movimento com propósito.** Reveal no scroll, hover, accordion, aba,
  carrossel que realmente troca. Nada de fade-up em tudo ao mesmo tempo.
- **`prefers-reduced-motion`** respeitado em todas.
- **Contraste AA** (4.5:1 texto normal, 3:1 texto grande) nas cores do nicho.

## 7. Contrato de link

- Toda landing volta pro hub com `../index.html`.
- Links entre landings: proibidos (o hub é o único índice).
- Formulário: não envia para lugar nenhum, então **mostra estado** — validação
  no campo vazio, erro de e-mail, e sucesso com confirmação visível.
