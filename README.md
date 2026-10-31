# modelos-de-sites

[English](README.en.md) · **Português (Brasil)**

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](#) [![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)](#) [![Vanilla JS](https://img.shields.io/badge/Vanilla%20JS-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](#) [![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Deployed-222?style=flat-square&logo=githubpages)](#)

## O que é

**Mostruário de 20 landing pages**, uma para cada nicho (academia, advocacia, clínica médica, imobiliária, pet shop, e-commerce, etc.), com um hub em `index.html` que navega entre os modelos. Serve de vitrine do trabalho de construção de sites e como base pronta para um cliente escolher o segmento.

## Status

Em produção. Publicado em <https://kelvinoliveiracode.github.io/modelos-de-sites/> (HTTP 200 verificado).

## Funcionalidades

- **Hub** (`index.html`) que lista e navega para os 20 modelos por nicho.
- **20 landing pages individuais**, cada uma em sua pasta com `index.html` próprio (self-contained).
- **Design system centralizado** definido em `DESIGN.md` (fonte de verdade do estilo de todos os modelos).
- **Specs de construção** em `spec/` (nichos, regras de landing, revisão de layout e visual).

## Arquitetura

Cada nicho é uma pasta com uma página HTML independente; o hub agrega. Sem build, sem framework, sem dependências — só HTML/CSS/JS estático.

```mermaid
flowchart LR
    H[hub index.html] --> A[academia-fitness]
    H --> M[moda-ecommerce]
    H --> P[pet-shop-vet]
    H --> ... [...20 nichos]
    D[DESIGN.md - design system] -.-> H
    D -.-> A
```

## Stack

- HTML5, CSS3, JavaScript vanilla
- Hospedagem: GitHub Pages

## Estrutura do repositório

```
modelos-de-sites/
├── index.html            # hub do mostruário
├── DESIGN.md             # direção de design (fonte de verdade)
├── <nicho>/
│   └── index.html        # uma landing por nicho (20 no total)
├── spec/                 # specs: nichos, regras, revisão de layout/visual
├── .nojekyll
└── (sem LICENSE)
```

## Pré-requisitos e instalação

Nenhum. Basta servir a pasta estaticamente.

## Como executar

```bash
python -m http.server 8080
# acesse http://localhost:8080 (hub)
# e /<nicho>/ index.html para cada modelo, ex.: /moda-ecommerce/
```

Ou abra cada `index.html` direto no navegador.

## Testes e qualidade

Não há testes automatizados nem CI neste repositório (ausência de `package.json` e workflow confirmada). A consistência visual segue o `DESIGN.md` e as revisões documentadas em `spec/revisao-layout.md` e `spec/revisao-visual.md`.

## Decisões técnicas e trade-offs

- **Uma landing self-contained por pasta**: cada modelo pode ser servido/personalizado isoladamente e casa pronta para o cliente.
- **Hub simples + 20 páginas estáticas**: leve, indexável e fácil de publicar no GitHub Pages.
- **Regras de landing documentadas em `spec/`**: formato e padrões de cada seção são norma, não preferência.

## Limitações conhecidas e roadmap

- As landings são estáticas (sem CMS/backend); conteúdo é editado no HTML.
- Não há integração com formulários de captura que vá além do próprio modelo.

## Processo de desenvolvimento

Projeto individual de Kelvin Oliveira, construído com agentes de IA orquestrados e revisado pelo autor. O design system, as specs e a revisão são do autor.

## Licença e autor

Este repositório **não possui arquivo de licença** (sem `LICENSE`). Copyright (c) Kelvin Rebelo de Oliveira.

**Autor**: [Kelvin Oliveira](https://github.com/KelvinOliveiraCode) · [Portfólio](https://kelvinoliveiracode.github.io/portfolio/)
