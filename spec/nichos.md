# Dossiê dos 20 modelos (fonte de verdade)

Cada landing é independente. **Um arquivo por nicho**, em
`<slug>/index.html`, autossuficiente (CSS e JS inline, só Google Fonts de
fora). Volta pro hub com `../index.html`.

A tabela abaixo alimenta o hub. As seções seguintes detalham cada nicho.

| # | Nicho | slug | Cores (papel) | Fontes |
|---|---|---|---|---|
| 1 | Clínica Médica / Saúde | `clinica-medica` | bg `#E3F2FD`, superfície `#FFFFFF`, acento `#A5D6A7` | Lora + Nunito Sans |
| 2 | Academia / Fitness | `academia-fitness` | bg `#111111`, superfície `#2E2E2E`, acento `#FF6B00` | Anton + Barlow Condensed |
| 3 | Advocacia | `advocacia` | bg escuro `#0A1F44`, acento `#C9A227`, cinza `#4A4A4A` | Playfair Display + Inter |
| 4 | Moda / E-commerce | `moda-ecommerce` | bg `#000000`, acento `#D9BBA8`, texto `#FFFFFF` | Bodoni Moda + Jost |
| 5 | Cursos Online / EAD | `cursos-ead` | marca `#6A0DAD`, apoio `#2563EB`, acento `#FF8C00` | Outfit + Space Grotesk |
| 6 | Imobiliária | `imobiliaria` | tinta `#1E3A5F`, acento `#2E7D32`, fundo `#F5F5F5` | Spectral + Work Sans |
| 7 | Estética / Beleza | `estetica-beleza` | superfície `#FFF8F0`, rosa `#F8BBD0`, acento `#D4AF37` | Cormorant Garamond + Jost |
| 8 | Tecnologia / SaaS | `tech-saas` | bg `#0F172A`, apoio `#7C3AED`, acento `#22D3EE` | Space Grotesk + IBM Plex Sans |
| 9 | Restaurante / Delivery | `restaurante-delivery` | bg `#1A1A1A`, marca `#D32F2F`, acento `#FFC107` | Bebas Neue + DM Sans |
| 10 | Pet Shop / Veterinária | `pet-shop-vet` | fundo `#FFFFFF`, marca `#4CAF50`, apoio `#03A9F4` | Baloo 2 + Nunito |
| 11 | Finanças / Investimentos | `financas-investimentos` | bg `#004D40`, acento `#C9A227`, apoio `#1565C0` | Libre Baskerville + Inter |
| 12 | Educação Infantil | `educacao-infantil` | pastéis `#FFF59D`, `#90CAF9`, `#F8BBD0`, `#A5D6A7` | Fredoka + Nunito |
| 13 | Casamento / Eventos | `casamento-eventos` | rosa `#E8B4B8`, acento `#D4AF37`, eucalipto `#A3B18A` | Cormorant Garamond + Jost |
| 14 | Odontologia | `odontologia` | acento `#00BCD4`, fundo `#FFFFFF`, apoio `#B2DFDB` | Manrope + Source Serif 4 |
| 15 | Marketing Digital / Agência | `marketing-digital` | bg `#0F0F0F`, marca `#5B21B6`, acento `#F97316` | Archivo Black + Space Grotesk |
| 16 | Energia Solar | `energia-solar` | acento `#FFD600`, marca `#2E7D32`, apoio `#0277BD` | Barlow Condensed + Inter |
| 17 | Seguros | `seguros` | marca `#1565C0`, acento `#43A047`, fundo `#FAFAFA` | Figtree + Lora |
| 18 | Viagens / Turismo | `viagens-turismo` | acento `#00ACC1`, marca `#FF7043`, apoio `#FFD54F` | Poppins + Playfair Display |
| 19 | Construção Civil | `construcao-civil` | acento `#FFC107`, cinza `#616161`, tinta `#212121` | Oswald + Barlow |
| 20 | Criptomoedas / Web3 | `cripto-web3` | bg `#1A0B2E`, acento `#00E5FF`, preto `#0D0D0D` | Syne + JetBrains Mono |

** Papel das cores: `marca` é a cor de identidade (botões, header, destaques).
`apoio` é segunda cor, usada com parcimônia. `acento` é o gesto único da
página (CTA, faixa, hover). Tinta = cor do texto principal. Fundo = fundo.
Razão escrita: 3 cores por nicho, no máximo, por isso cada uma tem um papel
fixo e não vira arco-íris. **

A "animação assinatura" de cada nicho é só a do herói. Além dela, o pacote
mínimo de animação de `spec/regras-landing.md` vale para todas, e cada seção
precisa do seu próprio gesto.

---

## 1. Clínica Médica / Saúde · `clinica-medica`

- **Público**: quem precisa de consulta e quer confiança rápida.
- **Promessa**: clínica com horário que funciona e agendamento sem ligação.
- **Superfície**: Story/Scroll. Hero split assimétrico (texto 7 colunas,
  card de agendamento 5 colunas). Sem 3 cards iguais.
- **Cores**: fundo `#E3F2FD`, superfície `#FFFFFF`, acento `#A5D6A7`
  (menta), tinta `#10333F`. Texto escuro sobre menta, nunca branco.
- **Seções, na ordem**: hero com card de agendamento → especialidades em
  lista escalonada (linhas alternadas, não grid de cards) → "como funciona"
  em 2 passos → equipe com placeholders de foto inicial → convênios em faixa
  única → FAQ acordeão (4 perguntas) → contato.
- **Animação assinatura**: linha de ECG em SVG que desenha sozinha no hero
  (`stroke-dasharray`), e o card de agendamento com campos que validam.
- **CTAs**: "Agendar consulta", "Ver especialidades", "Falar no WhatsApp".
- **FAQ (reais do nicho)**: quais convênios atendem / precisa de
  encaminhamento / quanto tempo dura a primeira consulta / atendem
  emergência.
- **Evitar**: ícone de estetoscópio genérico, foto de banco de imagens,
  selo falso de "clínica certificada".

## 2. Academia / Fitness · `academia-fitness`

- **Público**: pessoa cansada de academia vazia de sentido, quer rotina.
- **Promessa**: treino com acompanhamento, horário que cabe na semana.
- **Superfície**: Story/Scroll escura, tipografia como hierarquia.
- **Cores**: fundo `#111111`, superfície `#2E2E2E`, acento `#FF6B00`,
  tinta `#F5F5F5`. Laranja com tinta escura por cima.
- **Seções, na ordem**: hero full-bleed com título condensado gigante →
  planos em **tabela comparativa real** (2 planos, linhas de benefício) →
  grade semanal em abas (seg a sáb, cada aba com horários) → modalidades em
  lista numerada vertical → estrutura (placeholders) → FAQ (4) → matrícula.
- **Animação assinatura**: abas da grade que trocam o conteúdo, e o hero com
  entrada escalonada do título. Contador de repetições é UI do plano, não
  dado de marketing.
- **CTAs**: "Quero me matricular", "Ver grade de aulas", "Teste uma aula".
- **FAQ**: tem taxa de matrícula / pode trancar / tem aula experimental /
  personal incluso.
- **Evitar**: "transforme seu corpo" com antes/depois fabricado, fotos de
  banco, resultado garantido.

## 3. Advocacia · `advocacia`

- **Público**: pessoa ou empresa com um problema jurídico concreto.
- **Promessa**: advogado que explica o caso em linguagem simples.
- **Superfície**: Story/Scroll, autoridade por tipografia serifada.
- **Cores**: fundo escuro `#0A1F44`, acento `#C9A227`, cinza `#4A4A4A`,
  tinta clara `#E8EAF0`. Seções claras em `#F5F3EE` com tinta escura.
- **Seções, na ordem**: hero (título serifado grande à esquerda, bloco de
  credenciais placeholder à direita) → áreas de atuação em **acordeão de
  lista** (5 áreas, cada uma abre com 2 linhas) → processo em timeline
  vertical de 4 etapas → artigos placeholder (3) → formulário de contato
  com validação → rodapé com OAB placeholder.
- **Animação assinatura**: linha dourada que se desenha sob o título no
  scroll, e o acordeão com transição de altura real.
- **CTAs**: "Agendar conversa", "Ver áreas de atuação".
- **FAQ**: primeira consulta é paga / atendem online / qual o prazo médio do
  meu caso / trabalham com êxito (honesto: explicar que não).
- **Evitar**: "vença sua causa", selo falso de excelência, foto de tribunal
  de banco.

## 4. Moda / E-commerce · `moda-ecommerce`

- **Público**: comprador que quer peça boa, não liquidação.
- **Promessa**: curadoria de peças com caixa que chega inteira.
- **Superfície**: Catalog / editorial.
- **Cores**: fundo `#000000`, tinta `#FFFFFF`, acento `#D9BBA8` (nude).
- **Seções, na ordem**: hero editorial full-bleed (título Bodoni, sem
  botão duplo) → faixa marquee com palavras da coleção → produtos em grid
  **masonry assimétrico** (6 itens, tamanhos diferentes) com hover que
  revela preço placeholder → "como comprar" em 3 linhas simples → lookbook
  em blocos → newsletter (form que valida e confirma) → rodapé.
- **Animação assinatura**: marquee infinito, hover dos produtos com
  escala/opacidade, e revelação escalonada do grid.
- **CTAs**: "Ver a coleção", "Assinar novidades".
- **FAQ**: troca e devolução / prazo de entrega / como descubro meu tamanho
  / peças sob encomenda.
- **Evitar**: seta em todo link, "must-have", "essencial da estação".

## 5. Cursos Online / EAD · `cursos-ead`

- **Público**: profissional que quer mudar de área com prova de que aprendeu.
- **Promessa**: projeto pronto no portfólio ao final de cada módulo.
- **Superfície**: Decide/Learn.
- **Cores**: fundo `#FAF8FF`, tinta `#1B1035`, marca `#6A0DAD`,
  apoio `#2563EB`, acento `#FF8C00`. Roxo é identidade da marca (permitido
  por direção do dono, não é gradiente azul-roxo de decoração). Laranja só
  no CTA principal.
- **Seções, na ordem**: hero com painel de aula mockado (lista de módulos) →
  trilha em passos horizontais (5 módulos, barra de progresso animada) →
  "o que você vai construir" em lista com lugar de projeto → instrutor
  placeholder → formato em 2 blocos grandes (aulas ao vivo e comunidade) →
  investimento com 2 opções → FAQ (5) → matrícula.
- **Animação assinatura**: barras de progresso do módulo que enchem no
  reveal, e o painel de aula com transição entre módulos.
- **CTAs**: "Quero me matricular", "Ver a trilha", "Baixar o programa".
- **FAQ**: quanto tempo por semana / serve para iniciante / certificado /
  posso assistir gravado / e se eu não gostar.
- **Evitar**: "aprenda do zero", "vaga por tempo limitado", depoimento com
  foto de gente que não existe.

## 6. Imobiliária · `imobiliaria`

- **Público**: quem quer comprar ou alugar sem abrir 30 abas.
- **Promessa**: filtro que acha o imóvel e simulação que cabe no bolso.
- **Superfície**: Explore (busca + resultados).
- **Cores**: fundo `#F5F5F5`, tinta `#1E3A5F`, superfície escura `#1E3A5F`,
  acento `#2E7D32`.
- **Seções, na ordem**: hero com **buscador funcional** (tipo, bairro,
  quartos, faixa) → grid de imóveis que **filtra de verdade** com a busca
  (estado vazio quando nada é encontrado) → simulador de financiamento
  funcional (entrada, parcelas, prazo, com estado de erro) → como funciona
  em 3 linhas → bairros em faixa → contato.
- **Animação assinatura**: cards que reordenam com transição, e o simulador
  que recalcula ao digitar.
- **CTAs**: "Buscar imóveis", "Simular financiamento", "Falar com corretor".
- **FAQ**: a imobiliária cobra do comprador / documentos necessários /
  funciona para aluguel / visita no fim de semana.
- **Evitar**: "o imóvel dos seus sonhos", selo falso, foto de banco.

## 7. Estética / Beleza · `estetica-beleza`

- **Público**: mulher que quer resultado e horário que respeite a rotina.
- **Promessa**: protocolo claro, preço à vista, sem venda casada.
- **Superfície**: Story/Scroll suave.
- **Cores**: superfície `#FFF8F0`, rosa `#F8BBD0`, acento `#D4AF37`,
  tinta `#4A2B33`.
- **Seções, na ordem**: hero suave (título Cormorant, bloco de boas-vindas) →
  serviços em **acordeão com preço placeholder** (6 serviços) → "sua rotina
  de cuidados" em passos → pacotes em 2 blocos → agenda semanal (escolha de
  dia e horário, UI real) → FAQ (4) → agendamento.
- **Animação assinatura**: pétalas que caem devagar no hero (CSS, poucas,
  discretas) e o acordeão revelando preço.
- **CTAs**: "Agendar horário", "Ver serviços", "Falar no WhatsApp".
- **FAQ**: dói / quantas sessões / homem pode fazer / cancelamento.
- **Evitar**: "autoestima em alta", antes/depois fabricado, promessa de
  resultado em prazo.

---

## 8. Tecnologia / SaaS · `tech-saas`

- **Público**: time técnico que já tentou três ferramentas e cansou.
- **Promessa**: uma ferramenta que o time usa sem treinamento.
- **Superfície**: Decide/Learn, escura.
- **Cores**: fundo `#0F172A`, apoio `#7C3AED`, acento `#22D3EE`,
  tinta `#F8FAFC`. Ciano é gesto único (CTA, linha de destaque). Glow só no
  painel do hero, no máximo 2 elementos.
- **Seções, na ordem**: hero escura com **painel de dashboard mockado em
  SVG animado** (linha que desenha, número que não é métrica de marketing,
  é UI do produto) → features em grid **irregular** (1 card grande, 2
  pequenos, repetido 2 vezes) → integrações em faixa → preço em **2 planos**
  (nunca 3 colunas) → migração em 3 linhas → FAQ (5) → teste grátis.
- **Animação assinatura**: linha do gráfico desenhando no reveal, e o grid
  irregular com reveal escalonado.
- **CTAs**: "Começar teste grátis", "Ver integrações", "Falar com vendas".
- **FAQ**: integra com o que a gente já usa / onde ficam os dados / tem
  limite de usuários / como cancela.
- **Evitar**: terminal falso como herói, bento grid, "escalável",
  "intelegível", selo SOC fabricado.

## 9. Restaurante / Delivery · `restaurante-delivery`

- **Público**: quem tem fome agora e quer saber o que vai chegar.
- **Promessa**: comida boa, quente, com horário honesto.
- **Superfície**: Catalog + ação.
- **Cores**: fundo `#1A1A1A`, marca `#D32F2F`, acento `#FFC107`,
  tinta `#FFF8F0`.
- **Seções, na ordem**: hero com faixa amarela e título Bebas → cardápio em
  **abas reais** (entradas, pratos, sobremesas, bebidas, cada aba com 4-5
  itens e preço placeholder) → bloco do delivery em 2 passos → **estado
  aberto/fechado calculado com hora real** → reserva (form com validação) →
  FAQ (4) → rodapé com endereço placeholder.
- **Animação assinatura**: troca de aba do cardápio com transição, e vapor
  subindo no hero (2 elementos, discreto).
- **CTAs**: "Ver cardápio", "Pedir delivery", "Reservar mesa".
- **FAQ**: taxa de entrega / tempo médio / faz evento / opção sem glúten.
- **Evitar**: "sabor inesquecível", prato de banco, estrelinha de avaliação
  falsa.

## 10. Pet Shop / Veterinária · `pet-shop-vet`

- **Público**: tutor que trata o bicho como gente e quer cuidado sério.
- **Promessa**: clínica que explica o que está fazendo com o animal.
- **Superfície**: Story/Scroll leve.
- **Cores**: fundo `#FFFFFF`, marca `#4CAF50`, apoio `#03A9F4`, acento
  `#FFEB3B` (só em detalhes pequenos, nunca como fundo de texto), tinta
  `#10361C`.
- **Seções, na ordem**: hero alegre com ícones desenhados à mão (pata, osso,
  coração) → serviços em grid com **ícones SVG próprios** (6) → "primeira
  visita" em 4 passos → **planos de assinatura em 2 opções** → equipe
  placeholder → FAQ (4) → agendamento com escolha de pet (cachorro, gato,
  outro).
- **Animação assinatura**: pata que caminha no hero e os cards de serviço
  com leve subida no hover.
- **CTAs**: "Agendar consulta", "Ver planos", "Falar no WhatsApp".
- **FAQ**: atendem emergência 24h / fazem cirurgia / vacina sem consulta /
  planos cobrem castração.
- **Evitar**: fala de bebê ("aumigo"), foto de banco de cachorro, selo
  falso.

## 11. Finanças / Investimentos · `financas-investimentos`

- **Público**: quem ganha bem e não sabe para onde o dinheiro vai.
- **Promessa**: plano escrito, sem produto de banco empurrado.
- **Superfície**: Operate (simulador é a ação principal).
- **Cores**: fundo `#004D40`, acento `#C9A227`, apoio `#1565C0`,
  tinta clara `#E6F2EF`. Seções claras em `#F4F7F6` com tinta escura.
- **Seções, na ordem**: hero escura com proposta e um número placeholder
  de clientes → **simulador funcional** (aporte inicial, aporte mensal,
  prazo, taxa: calcula e mostra; estado vazio e estado de erro) → serviços
  em lista → "para quem é" e "para quem não é" (2 colunas honestas) →
  processo em timeline → FAQ (5) → formulário.
- **Animação assinatura**: resultado do simulador que conta e uma linha que
  desenha. Nada de promessa de rentabilidade.
- **CTAs**: "Simular agora", "Agendar diagnóstico", "Falar no WhatsApp".
- **FAQ**: qual o mínimo / é assessoria ou gestão / tem conflito de interesse
  / encontro é online.
- **Evitar**: "fique rico", gráfico de rentabilidade garantida, selo de
  "assessor certificado" fabricado.

## 12. Educação Infantil · `educacao-infantil`

- **Público**: pai e mãe escolhendo a primeira escola.
- **Promessa**: criança que volta para casa contando o que fez.
- **Superfície**: Story/Scroll colorida.
- **Cores**: fundo `#FFFDF5`, tinta `#26221A`, pastéis rotativos por bloco:
  `#FFF59D`, `#90CAF9`, `#F8BBD0`, `#A5D6A7`. Razão do sistema: cada
  área da escola tem um pastel; o CTA é neutro escuro para não competir.
- **Seções, na ordem**: hero colorida com formas flutuando devagar →
  "um dia na escola" em **timeline vertical** com horários → atividades em
  blocos de pastel rotativo (6) → estrutura em lista → calendário de
  matrículas com **estados** (aberta, lista de espera, encerrada) → FAQ (4)
  → agendar visita.
- **Animação assinatura**: formas geométricas flutuando no hero (poucas,
  lentas) e a timeline revelando item a item.
- **CTAs**: "Agendar visita", "Ver calendário de matrículas".
- **FAQ**: a partir de que idade / período integral / alimentação inclusa /
  adaptação da criança.
- **Evitar**: fala de bebê forçada, desenho genérico de nuvem, "melhor
  escola da cidade".

## 13. Casamento / Eventos · `casamento-eventos`

- **Público**: casal com data marcada e orçamento curto.
- **Promessa**: evento que parece caro sem custar o que parece.
- **Superfície**: Story/Scroll.
- **Cores**: fundo `#FFFCFA`, rosa `#E8B4B8`, acento `#D4AF37`,
  eucalipto `#A3B18A`, tinta `#3A2E2E`.
- **Seções, na ordem**: hero com nome do casal em script e data →
  "o grande dia" em **timeline** (cerimônia, coquetel, jantar, festa) →
  galeria placeholder em grid assimétrico (blocos com "sua foto") → pacotes
  em 2 opções → quem assina (placeholder) → RSVP (form que confirma) → FAQ
  (4).
- **Animação assinatura**: pétalas caindo devagar (poucas) e a timeline
  revelando com atraso entre itens.
- **CTAs**: "Confirmar presença", "Ver pacotes", "Falar com a gente".
- **FAQ**: quantos convidados / pode levar outro fornecedor / chuva /
  pagamento.
- **Evitar**: "o dia mais feliz da sua vida", foto de casal de banco,
  contagem regressiva para data fabricada.

## 14. Odontologia · `odontologia`

- **Público**: quem evita dentista e quer parar de evitar.
- **Promessa**: consulta sem dor e preço combinado antes.
- **Superfície**: Decide/Learn clara.
- **Cores**: fundo `#FFFFFF`, acento `#00BCD4`, apoio `#B2DFDB`,
  tinta `#0A3A42`. Turquesa em faixas, sempre com tinta escura por cima.
- **Seções, na ordem**: hero com faixa turquesa e título → tratamentos em
  **lista técnica** (linhas com descrição e preço placeholder, não cards) →
  "primeira consulta" em 3 passos → antes e depois em blocos placeholder
  (sem imagem falsa) → equipe → convênios em faixa → FAQ (4) → agendamento.
- **Animação assinatura**: brilho que passa pelo hero (1 elemento) e a lista
  de tratamentos revelando linha a linha.
- **CTAs**: "Agendar avaliação", "Ver tratamentos", "Falar no WhatsApp".
- **FAQ**: dói / clareamento funciona em quantas sessões / atende criança /
  convênio.
- **Evitar**: sorriso de banco, "dentista sem dor" como bordão repetido,
  selo falso.

---

## 15. Marketing Digital / Agência · `marketing-digital`

- **Público**: dono de negócio que já queimou dinheiro em anúncio.
- **Promessa**: campanha com relatório que o cliente entende.
- **Superfície**: Story/Scroll escura.
- **Cores**: fundo `#0F0F0F`, marca `#5B21B6`, acento `#F97316`,
  tinta `#F5F3FF`. Laranja com tinta escura por cima.
- **Seções, na ordem**: hero escura com título grande → serviços em grid
  **irregular** (1 grande + 2 pequenos, com número de serviço) → casos em
  lista com **métricas placeholder** (`[REAL DATA]`, nunca inventado) →
  processo em 4 etapas → "como cobramos" em 2 modelos → diagnóstico (form
  de 4 campos que gera um próximo passo visível) → FAQ (5).
- **Animação assinatura**: grade irregular com reveal escalonado e o bloco
  de caso com barra que cresce.
- **CTAs**: "Pedir diagnóstico", "Ver casos", "Falar no WhatsApp".
- **FAQ**: qual o mínimo de mídia / contrato tem fidelidade / quem produz o
  criativo / relatório com que frequência.
- **Evitar**: "cresça 10x", painel de métrica falsa, logo de cliente famoso.

## 16. Energia Solar · `energia-solar`

- **Público**: conta de luz alta e vontade de parar de pagar tão caro.
- **Promessa**: economia estimada antes de fechar, com número do próprio
  consumo.
- **Superfície**: Operate (simulador).
- **Cores**: fundo `#F7FAF7`, acento `#FFD600`, marca `#2E7D32`,
  apoio `#0277BD`, tinta `#12261A`. Amarelo em faixa com tinta escura; verde
  com texto branco (contraste 5:1).
- **Seções, na ordem**: hero com faixa amarela e sol em SVG que gira devagar
  → **calculadora funcional** (consumo médio mensal, valor da conta, prazo:
  estima economia e payback; estado vazio e erro) → como funciona em 4
  passos → produtos em lista técnica → quem já instalou em blocos
  placeholder → FAQ (4) → orçamento.
- **Animação assinatura**: raios do sol girando devagar (1 elemento) e o
  resultado da calculadora contando.
- **CTAs**: "Calcular economia", "Pedir orçamento", "Falar no WhatsApp".
- **FAQ**: funciona em apartamento / quanto tempo dura a instalação /
  manutenção / e se chover.
- **Evitar**: "conta zero" como promessa absoluta, selo falso, telhado de
  banco.

## 17. Seguros · `seguros`

- **Público**: quem quer proteger a família e não entende o contrato.
- **Promessa**: cobertura explicada em português antes de assinar.
- **Superfície**: Decide (simule e compare).
- **Cores**: fundo `#FAFAFA`, marca `#1565C0`, acento `#43A047`,
  tinta `#10243A`. Verde com tinta escura (contraste 6.4:1), nunca branco.
- **Seções, na ordem**: hero com título e bloco de cotação rápida →
  coberturas em **acordeão** (auto, vida, residência, viagem: cada uma abre
  com o que cobre e o que não cobre) → "simule seu perfil" (form de 3
  campos que indica o tipo de seguro certo, com estado vazio) → como
  acionar o sinistro em 3 passos → FAQ (5) → contato.
- **Animação assinatura**: escudo que se desenha no hero e o acordeão de
  coberturas.
- **CTAs**: "Simular meu seguro", "Ver coberturas", "Falar com corretor".
- **FAQ**: seguro cobre terceiro / como aciona sinistro / pode parcelar /
  quem é o corretor.
- **Evitar**: "proteja sua família", selo de seguradora famosa sem direito,
  número de clientes inventado.

## 18. Viagens / Turismo · `viagens-turismo`

- **Público**: casal ou família querendo a próxima viagem sem pesquisar 40
  sites.
- **Promessa**: roteiro montado por quem conhece o destino.
- **Superfície**: Explore.
- **Cores**: fundo `#FFFFFF`, acento `#00ACC1`, marca `#FF7043`,
  apoio `#FFD54F`, tinta `#0A2E38`. Turquesa e coral sempre com tinta
  escura por cima.
- **Seções, na ordem**: hero com título e blocos de destino flutuando →
  destinos em grid com **hover que revela detalhe** (6) → "monte seu
  roteiro" (escolhe destino, dias, estilo: mostra um resumo; estado vazio) →
  pacotes em 2 opções → quem viaja com a gente (placeholder) → FAQ (4) →
  contato.
- **Animação assinatura**: parallax leve nas formas do hero e o grid de
  destinos com reveal escalonado.
- **CTAs**: "Ver destinos", "Montar meu roteiro", "Falar no WhatsApp".
- **FAQ**: parcelamento / documentos / baggage / cancelamento.
- **Evitar**: "viagem dos sonhos", praia de banco, preço que não existe.

## 19. Construção Civil · `construcao-civil`

- **Público**: dono de obra que quer prazo e preço respeitados.
- **Promessa**: orçamento fechado por escrito antes do primeiro tijolo.
- **Superfície**: Operate (orçamento).
- **Cores**: fundo `#FFFFFF`, acento `#FFC107`, cinza `#616161`,
  tinta `#212121`. Amarelo como faixa de segurança, sempre com tinta escura.
- **Seções, na ordem**: hero com faixa amarela e título Oswald → serviços
  em **lista técnica** (6, com escopo e prazo placeholder) → obras
  entregues em blocos placeholder (grid assimétrico) → **orçamento
  funcional** (tipo de serviço, metragem, padrão: calcula faixa; estado
  vazio e erro) → como trabalhamos em 4 passos → FAQ (4) → contato.
- **Animação assinatura**: faixa de segurança que desliza no hero e a lista
  de serviços revelando.
- **CTAs**: "Pedir orçamento", "Ver serviços", "Falar no WhatsApp".
- **FAQ**: visita técnica é paga / quem provê material / prazo / nota.
- **Evitar**: "qualidade garantida", canteiro de banco, capacete sem
  contexto.

## 20. Criptomoedas / Web3 · `cripto-web3`

- **Público**: quem já opera e está cansado de exchange que cai.
- **Promessa**: carteira e educação, sem promessa de ganho.
- **Superfície**: Decide/Learn escura.
- **Cores**: fundo `#1A0B2E`, preto `#0D0D0D`, acento `#00E5FF`,
  tinta `#F2EEFF`. Ciano é o gesto único. Glow em no máximo 2 elementos, com
  a razão escrita: identidade do nicho.
- **Seções, na ordem**: hero escura com título Syne e partículas discretas
  → como funciona em 3 passos reais (criar carteira, mover, proteger) →
  recursos em grid **irregular** (1 grande + 2 pequenos) → segurança em
  lista honesta (sem selo, explica o que faz) → roadmap em timeline →
  FAQ (5) → lista de espera.
- **Animação assinatura**: grade em perspectiva que se move devagar no hero
  (1 elemento) e o reveal irregular.
- **CTAs**: "Entrar na lista de espera", "Ver como funciona".
- **FAQ**: preciso experiência / onde ficam as chaves / tem suporte /
  é custódia ou não.
- **Evitar**: gráfico de moeda subindo, "lua", número de ganho, terminal
  falso.

---

## Regras de copy (valem para as 20)

1. Português do Brasil, com acento. Nunca inglês por frescura.
2. Nenhum travessão (—). Use vírgula, ponto ou parênteses.
3. Nenhum número inventado: clientes, notas, prazos, avaliações. Onde entra
   dado real, placeholder entre colchetes: `[+1.200 clientes]`,
   `[nota 4,9]`, `[prazo: 30 dias]`.
4. Nenhum depoimento inventado. Use `[depoimento real]` com nome placeholder.
5. CTA específico do nicho. Nada de "Saiba mais", "Comece agora",
   "Descubra".
6. Sem advérbio vazio: revolucionário, incrível, surpreendente,
   inovador, seamless.
7. Sem frase que promete o que o negócio não pode provar.
