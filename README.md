<<<<<<< HEAD
# Modelos de Sites · 20 landing pages de mostruário, uma por nicho

![HTML5](https://img.shields.io/badge/HTML5-e34f26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572b6?style=flat-square&logo=css3&logoColor=white)

Mostruário de 20 landing pages, uma por nicho de negócio. Cada modelo é um arquivo HTML único, sem build, sem npm, sem framework: abra no navegador e veja como o site do cliente fica antes de pedir o seu próprio.

## Problema / Por que existe
=======
# Modelos de Sites — Mostruário de 20 Landing Pages

![linguagem: HTML](https://img.shields.io/badge/linguagem-HTML-blue)  
![status: concluido](https://img.shields.io/badge/status-concluido-green)  
![licenca: MIT](https://img.shields.io/badge/licenca-MIT-blue)

### Descrição
Mostruário de 20 landing pages, uma para cada segmento de negócio. HTML/CSS estático, pronto para clonar e adaptar.

### O que faz
Mostruário de 20 landing pages, uma para cada segmento de negócio. HTML/CSS estático, pronto para clonar e adaptar.

### Tecnologias
- HTML5
- CSS3

### Como usar
Abra o arquivo `index.html` no navegador.

### Estrutura
Consulte a árvore do repositório para a organização exata de pastas e arquivos.

### Testes
Não há contagem de testes registrada nesta metadata. Adicione e execute testes apropriados à linguagem (pytest para Python, ./mvnw test para Java, npm test para JavaScript/TypeScript).

### Licença
MIT

### Autor
Kelvin Oliveira — github.com/KelvinOliveiraCode
>>>>>>> 195485ec38dcdcc30e3d8eaaaf97b5cae130a593

O dono de negócio precisa ver o que vai receber antes de pagar por um site. Um wireframe cinza não mostra isso. Este mostruário reúne 20 modelos prontos por nicho — clínica médica, academia, advocacia, moda, cursos online, imobiliária, estética, tecnologia SaaS, restaurante, pet shop, finanças, educação infantil, casamento, odontologia, marketing digital, energia solar, seguros, viagens, construção civil e criptomoedas — para que o cliente escolha o mais parecido com o seu negócio e peça o seu no mesmo padrão. Textos, preços e imagens são espaços reservados para os dados reais de cada cliente.

<<<<<<< HEAD
## O que faz

O hub (index.html) é o único índice: não há links entre landings. Ele reúne os 20 modelos em um grid filtrável por segmento e busca por texto. Cada card mostra o nome do nicho, uma linha do que o modelo faz e a paleta de cores usada. Clicando, abre a landing do nicho: uma página completa e autocontida com navegação, seções específicas do nicho, formulário com validação e interações reais (cardápio em abas, simulador de financiamento, calculadora de energia solar, agendamento etc.), além de um link de volta ao hub. Todas as páginas abrem direto no navegador, sem instalação.

## Stack

- HTML5 — semântica, foco visível, navegação por teclado, prefers-reduced-motion
- CSS3 — variáveis de CSS, grid, flexbox, animações em transform e opacity, responsividade mobile-first
- JavaScript — IntersectionObserver para reveal de rolagem, filtros e busca no hub, validação de formulários e interações por nicho
- Sem dependências externas além do Google Fonts

## Como funciona

O visitante filtra por segmento, busca por termo, escolhe um modelo e abre o arquivo `<slug>/index.html`. Cada landing é um arquivo único com CSS e JS inline. O menu funciona em mobile, o formulário valida campos e mostra estado de sucesso sem enviar nada para lugar nenhum, e todos os modelos respeitam contraste WCAG AA e redução de movimento.

## Como rodar

Não há build. Abra `index.html` no navegador, ou sirva a pasta com qualquer servidor estático:

```
python -m http.server
npx serve .
```

Para abrir um modelo específico, navegue até a pasta dele, por exemplo `restaurante-delivery/index.html`.

## Estrutura do projeto

```
index.html           hub: filtro por segmento, busca, 20 cards de modelos, processo e contato
<slug>/index.html    landing completa e autocontida de um nicho (20 pastas)
spec/nichos.md       dossiê dos 20 modelos: cores, fontes, seções e animação de cada nicho
spec/regras-landing.md regras de execução valendo para todas as landings (acessibilidade, mobile, animação, proibidos)
spec/revisao-layout.md revisão de layout
spec/revisao-visual.md revisão visual
DESIGN.md            direção de design do hub e contrato das landings
.nojekyll            publicação direta no GitHub Pages
```

## Trade-offs e decisões

- Uma landing por nicho, cada um um arquivo único. Vantagem: o cliente abre e vê o resultado real no navegador sem instalar nada. Custo: repetição de CSS entre páginas; nenhuma mudança global se propaga sozinha.
- CSS e JS inline. Sem build, sem npm, sem framework — zero dependência de ferramenta. O único link externo é o Google Fonts.
- Nenhum link entre landings; o hub é o único índice. O cliente entra pelo hub, escolhe o nicho e volta. Simplifica a navegação, mas exige voltar pelo botão do navegador ou pelo link de retorno em cada landing.
- A cor de nicho aparece apenas como fita no card do hub, nunca como cor de interface do hub, evitando efeito arco-íris de 20 paletas.
- Textos, preços, imagens e depoimentos são placeholders explícitos (`Sua Marca`, `[LOGO]`, `[depoimento real]`). Nunca se passa dado inventado por real.

## Limitações conhecidas

- Não há backend: formulários não enviam nada; mostram apenas estado de sucesso na tela.
- A busca do hub busca nome e segmento do modelo; não há busca por conteúdo dentro das landings.
- Cada modelo carrega fontes do Google Fonts; sem conexão à internet, a página usa a fonte fallback do sistema.
- Todo o conteúdo está em português do Brasil; não há versão em inglês.
- Não é um site pronto para publicar como está: é um mostruário de demonstração com dados de placeholder.

## Licença

Distribuído sob a licença MIT. Consulte o arquivo de licença do repositório para detalhes.

## Autor

Kelvin Oliveira

- GitHub: https://github.com/KelvinOliveiraCode
- LinkedIn: https://www.linkedin.com/in/kelvin-oliveira-code/
- Portfólio: https://kelvinoliveiracode.github.io/portfolio/
- WhatsApp: (91) 98613-4599
=======
# Website Models — Showcase of 20 Landing Pages

![language: HTML](https://img.shields.io/badge/language-HTML-blue)  
![status: concluido](https://img.shields.io/badge/status-concluido-green)  
![license: MIT](https://img.shields.io/badge/license-MIT-blue)

### Description
Showcase of 20 landing pages, one per business segment. Static HTML/CSS, ready to clone and adapt.

### What it does
Showcase of 20 landing pages, one per business segment. Static HTML/CSS, ready to clone and adapt.

### Technologies
- HTML5
- CSS3

### How to use
Open `index.html` in the browser.

### Structure
Check the repository tree for the exact folder and file organization.

### Tests
No test count recorded in this metadata. Add and run tests appropriate for the language (pytest for Python, ./mvnw test for Java, npm test for JavaScript/TypeScript).

### License
MIT

### Author
Kelvin Oliveira — github.com/KelvinOliveiraCode
>>>>>>> 195485ec38dcdcc30e3d8eaaaf97b5cae130a593
