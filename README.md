# Modelos de Sites

Mostruário de 20 landing pages, uma por nicho. Cada página é um modelo
completo e independente, feito para o cliente ver como eu trabalho antes de
fechar o próprio site.

**Ver o mostruário:** https://kelvinoliveiracode.github.io/modelos-de-sites/

## Como isto está organizado

```
index.html           hub: filtro, busca, os 20 modelos e contato
<slug>/index.html    uma landing por nicho, autocontida
spec/                direção de design e regras de execução (documentação)
DESIGN.md            direção do hub e contrato das landings
```

O hub é o único índice. As landings não linkam entre si: o cliente entra pelo
hub, escolhe um nicho e volta.

## Os 20 nichos

| Nicho | Pasta | Paleta |
|---|---|---|
| Clínica Médica / Saúde | `clinica-medica` | `#E3F2FD` `#FFFFFF` `#A5D6A7` |
| Academia / Fitness | `academia-fitness` | `#111111` `#FF6B00` `#2E2E2E` |
| Advocacia | `advocacia` | `#0A1F44` `#C9A227` `#4A4A4A` |
| Moda / E-commerce | `moda-ecommerce` | `#000000` `#FFFFFF` `#D9BBA8` |
| Cursos Online / EAD | `cursos-ead` | `#6A0DAD` `#2563EB` `#FF8C00` |
| Imobiliária | `imobiliaria` | `#1E3A5F` `#2E7D32` `#F5F5F5` |
| Estética / Beleza | `estetica-beleza` | `#F8BBD0` `#D4AF37` `#FFF8F0` |
| Tecnologia / SaaS | `tech-saas` | `#0F172A` `#7C3AED` `#22D3EE` |
| Restaurante / Delivery | `restaurante-delivery` | `#D32F2F` `#FFC107` `#1A1A1A` |
| Pet Shop / Veterinária | `pet-shop-vet` | `#4CAF50` `#03A9F4` `#FFEB3B` |
| Finanças / Investimentos | `financas-investimentos` | `#004D40` `#C9A227` `#1565C0` |
| Educação Infantil | `educacao-infantil` | `#FFF59D` `#90CAF9` `#F8BBD0` `#A5D6A7` |
| Casamento / Eventos | `casamento-eventos` | `#E8B4B8` `#D4AF37` `#A3B18A` |
| Odontologia | `odontologia` | `#00BCD4` `#FFFFFF` `#B2DFDB` |
| Marketing Digital / Agência | `marketing-digital` | `#5B21B6` `#F97316` `#0F0F0F` |
| Energia Solar | `energia-solar` | `#FFD600` `#2E7D32` `#0277BD` |
| Seguros | `seguros` | `#1565C0` `#43A047` `#FAFAFA` |
| Viagens / Turismo | `viagens-turismo` | `#00ACC1` `#FF7043` `#FFD54F` |
| Construção Civil | `construcao-civil` | `#FFC107` `#616161` `#212121` |
| Criptomoedas / Web3 | `cripto-web3` | `#1A0B2E` `#00E5FF` `#0D0D0D` |

## Sobre os modelos

São demonstração. Textos, preços, números, fotos e depoimentos são
placeholder de propósito: `Sua Marca`, `[LOGO]`, `[+1.200 clientes]`,
`[depoimento real]`, `Sua foto aqui`. Nada inventado passa por dado real.

Cada página é um arquivo único, sem build, sem npm, sem framework. A única
dependência externa é o Google Fonts. CSS e JS ficam inline.

Todas são mobile-first, com contraste WCAG AA, navegação por teclado,
`prefers-reduced-motion` respeitado e animação em `transform`/`opacity`.

## Rodar local

Não há build. Abra `index.html` no navegador, ou suba a pasta em qualquer
servidor estático:

```
npx serve .
python -m http.server
```

## Contato

Kelvin Oliveira
WhatsApp: (91) 98613-4599
LinkedIn: https://www.linkedin.com/in/kelvin-oliveira-code/
Portfólio: https://kelvinoliveiracode.github.io/portfolio/
