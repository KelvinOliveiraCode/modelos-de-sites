# Contrato de revisão — layout, sobreposição e acabamento

Landing pages de demonstração, uma por nicho. Já funcionam: responsivas,
animadas, com formulários. Esta rodada é **defeito de layout**, não redesenho.

## 0. Regra de ouro

**Não redesenhe.** Não troque paleta, não troque fonte, não reescreva copy,
não mude a estrutura de seções. Conserte o defeito e pare.

Cada defeito abaixo tem uma causa local. Ache a causa, corrija a causa.

---

## 1. LEI DO DONO — a página ocupa a largura toda

> *"Sites and landing pages occupy the entire browser width: sections,
> backgrounds, grids, and media run edge to edge, and the gutter is inner
> padding, not a floating margin that leaves the page sitting in the middle of
> the screen. A centered column narrower than the viewport is a defect to fix,
> not a layout choice; only a measured text column (45–75ch) stays narrow,
> inside a full-bleed section."*

Container: `max-width: min(94vw, 1560px)` + `padding: 0 clamp(20px, 3.6vw, 60px)`.
**Já aplicado nas 21 páginas. Não mexa nisso.**

## 2. Classes de defeito a caçar

Você vai receber bugs específicos do seu arquivo. **Além deles, caçe estas
classes nos outros arquivos seus** — o dono pediu re-análise completa porque os
mesmos defeitos aparecem onde ele não apontou.

### 2.1 Sobreposição (elemento invade texto)
Elemento `absolute`/`fixed`, ou card com altura fixa, cobrindo texto.
Sinais: `.classe{height:...px}` com conteúdo maior, `position:absolute`
sem `z-index` coerente, `transform` que desloca o elemento sobre o vizinho.

**Como achar:** no navegador, compare `getBoundingClientRect()` do elemento
decorativo com o do texto. Ou procure no CSS por `height:` fixo em card e por
`position:absolute` sem `position:relative` no pai.

### 2.2 Fuga do pai
Elemento estourando o container. Sintoma clássico: `position:absolute` num
filho cujo pai **não tem `position:relative`** — o filho se posiciona contra um
ancestral mais acima e sai do lugar.

**Regra:** todo pai de `position:absolute` tem `position:relative`, ou o
absoluto é reposicionado com `left/right` calculados para o container.

### 2.3 Alvo gigante
Botão com mais de ~300px de largura ou 90px de altura. Ultra-esticado,
`width:100%` herdado, ou flex que estica.

**Regra:** botão de CTA tem largura natural (`inline-flex`) ou no máximo
`min(420px, 100%)`. Nunca `width:100%` num desktop. Alvo de toque mínimo 44×44px.

### 2.4 Texto achatado
`font-stretch`, `scaleX`, `transform: scaleX(...)`, ou `letter-spacing`
muito negativo em título grande. Títulos saem "espremidos".

**Regra:** remova `font-stretch` e `scaleX` de texto. Se o título precisa de
peso, use `font-weight` e `letter-spacing` normais.

### 2.5 Linha órfã
Linha horizontal ou vertical absolute, sem conteúdo, que não liga nada:
- a barra do hamburger solta no meio da página
- a linha tracejada ao lado de um botão
- um conector de timeline que não chega no último item
- um pseudo-elemento `::after` com `height:1px;width:60px`

**Regra:** conector de timeline é legítimo **se** tem marcador (bolinha/
número) em cada etapa **e** vai do primeiro ao último. Linha que existe só
para enfeite sai. Se remover a linha, remova o elemento e o CSS dele.

### 2.6 SVG sem sentido
Ilustração que não pode ser explicada em uma frase ligada ao nicho.
Círculos concêntricos, grades soltas, cruzes, arcos sem função, "planeta"
com pontos aleatórios.

**Regra:** cada ilustração se explica em uma frase ligada ao nicho, ou sai.
SVG decorativo de fundo precisa de `aria-hidden="true"`; SVG que carrega
informação precisa de `role="img"` + `aria-label` descrevendo **o que é**.

### 2.7 Texto mal posicionado
Parágrafo espremido (`max-width` baixo demais), bloco desalinhado do título,
item de lista que não alinha com o resto, caixa com altura muito maior que o
conteúdo.

**Regra:** linha de texto entre 45ch e 75ch. Card com altura fixa deve usar
`min-height` + padding, nunca `height`. Bloco de lista alinha pelo mesmo eixo.

### 2.8 Repetição de palavra
A mesma palavra repetida em sequência (ex.: "Energia solar" em faixa, título e
logo). Isso é repetição, não identidade.

**Regra:** a palavra do nicho pode aparecer **uma** vez como identidade (logo
ou selo). Elsewhere, escreva o texto.

---

## 3. O que NÃO pode quebrar

Rode ao final, antes de reportar. Se uma mudança quebrar um destes, desfaça
a mudança.

1. **`node --check` no JS.** Extraia o conteúdo de todos os `<script>` para um
   `.js` e rode `node --check`. Tem que passar.
   *Cuidado:* acento em identificador JS é SyntaxError. `var formulario` quebra.
2. **Âncora casa com id.** Todo `href="#x"` tem `id="x"` no mesmo arquivo.
   Todo `getElementById("x")` tem `id="x"`. Todo `aria-controls="x"` tem
   `id="x"`.
3. **Classe de reveal casa com o JS.** Se o CSS usa `.ativo` e o JS faz
   `classList.add("in")`, o conteúdo fica **invisível para sempre**. Confira o
   seletor do CSS e a chamada do JS: precisam ser a mesma palavra.
4. **Tags balanceadas:** `div`, `section`, `header`, `footer`, `main`, `nav`,
   `article`, `form`, `ul`, `li`, `style`, `script`.
5. **Nenhum travessão (—) no texto.**
6. **`prefers-reduced-motion`** presente e desligando as animações.
7. **Rodapé com `../index.html`** para o hub.
8. **Sem `transition: all`, sem `outline: none`** sem substituto visível.
9. **Sem mojibake** (`Ã§`, `Ã£`, `tÃ©cnica`). Acento perdido é bug.
10. **Sem `overflow-x:hidden`** escondendo bug. Se removeu a causa, remova
    também a máscara.

---

## 4. Como trabalhar

1. Leia o CSS e o markup do arquivo **antes** de editar.
2. Para cada defeito listado: encontre a regra CSS exata que causa.
3. Edite pequeno e preciso. Não reescreva o arquivo inteiro.
4. Se remover um elemento, remova também o CSS que existia só para ele
   (regra, media query, `@keyframes`). CSS órfão acumula.
5. Rode as 10 verificações da seção 3.
6. Confira no navegador em **1440×900** e **390×844**.

## 5. Armadilhas conhecidas deste repositório

- Subagente que grava arquivo parcial. **Sempre leia de volta o disco** para
  confirmar que a edição está lá. Nunca confie no relato próprio.
- `node --check` passando **não** prova que a página funciona: prova só que o
  JS é sintaticamente válido. Um `getElementById` que retorna `null` mata o
  resto do script **sem erro visível**.
- Console deste host é CP1252. Texto acentuado sai com `?`. Meça acento por
  code point (`[int][char]`), nunca pelo que aparece no terminal.