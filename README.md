# 🌍 GeoScout Wiki

Base de conhecimento para identificação de países no GeoGuessr, combinada com um agente interativo no estilo Akinator que faz perguntas progressivas para adivinhar onde você está no mapa.

---

## O que é

Dois produtos complementares:

**1. Wiki de países** — 136 países documentados com foco em pistas visuais do Google Street View: câmera, vegetação, arquitetura, placas, bollards, linhas de pista, scripts e muito mais.

**2. GeoScout App** — aplicativo web estático que faz perguntas progressivas ao usuário e vai eliminando países até chegar numa previsão com nível de confiança. Zero API, zero backend, 100% gratuito.

---

## GeoScout App

O app roda inteiramente no navegador — sem servidor, sem API key, sem custo. Basta abrir o arquivo `geoscout-akinator.html`.

**Como funciona:**
- 28 perguntas organizadas em 2 fases: geral (10 perguntas) e específica (18 perguntas)
- Cada resposta pontua todos os 136 países simultaneamente via sistema de scoring
- A previsão e o nível de confiança atualizam em tempo real após cada resposta
- Os países candidatos ainda em jogo ficam visíveis abaixo da previsão
- Alertas automáticos para combinações de altíssima confiança (ex: "DUR = Turquia 99%")
- Botão de desfazer em cada resposta e reset para nova rodada

**Fase geral** cobre os atributos mais eliminatórios: script das placas, sinal de PARE, qualidade da câmera, lado de direção, linhas de pista, vegetação, bollards, solo.

**Fase específica** aprofunda com: chevrons, postes de utilidade, guardrails, diacríticos latinos, variante cirílica, script asiático, tipo e cor do carro Google, vegetação exclusiva, contexto geográfico, postos de combustível e arquitetura.

---

## Wiki — Estrutura e Cobertura

```
wiki/
├── countries/      # 136 países — um arquivo .md por país
├── concepts/       # Conceitos transversais (câmera, bollards, scripts, etc.)
├── outputs/        # Análises, relatórios e outputs do agente
│   ├── countries-attributes.json   # Dataset com 30 atributos por país
│   ├── questions-extended.json     # Banco de perguntas do app
│   └── attribute-analysis.md      # Análise estratégica de atributos
└── index.md        # Índice mestre
raw/
└── countries/      # Fontes brutas antes da compilação
CLAUDE.md           # Schema de instruções para o agente
```

**Campos por país no dataset:**
`driving_side` · `scripts` · `latin_diacritics` · `stop_sign` · `camera_special` · `camera_blur` · `google_car_type` · `google_car_color` · `road_line_outside` · `road_line_center` · `road_line_exclusive` · `bollard_type` · `chevron` · `utility_pole_type` · `guardrail_color` · `vegetation_dominant` · `vegetation_exclusive` · `soil_color` · `continent` · `is_island` · `is_microstate` · `is_spillover` · `exclusive_features` · `confusable_with` · `fuel_brands_exclusive` · `confidence_score`

---

## Metodologia de construção

**1. Coleta de fontes**
Páginas de referência capturadas via Obsidian Web Clipper e armazenadas em `raw/countries/`.

**2. Compilação automatizada**
Processamento via [Claude Code](https://claude.ai/code) usando o schema `CLAUDE.md` — o agente lê as fontes, extrai informações e gera páginas padronizadas em Markdown com wikilinks entre países e conceitos.

**3. Extração de atributos**
Script de varredura que lê todos os arquivos `wiki/countries/*.md` e gera o `countries-attributes.json` com atributos estruturados por país, priorizados por poder de eliminação.

**4. Manutenção contínua**
Novas fontes são adicionadas a `raw/` e processadas incrementalmente. Health checks periódicos identificam lacunas e contradições.

---

## Usar com Claude Projects (alternativa ao app)

Para uma experiência de chat livre com o wiki como contexto:

1. Acesse [claude.ai](https://claude.ai) e crie um **Project** chamado `GeoScout`
2. Cole nas instruções do projeto:

```
Você é o GeoScout, um especialista em GeoGuessr. Sua ÚNICA fonte de conhecimento são os arquivos do wiki anexados a este projeto — não use conhecimento externo.

Quando o usuário descrever o que vê na tela do GeoGuessr, responda SEMPRE neste formato:

🌍 **País mais provável:** [Nome] — confiança: alta / média / baixa
**Por quê:** [quais pistas do wiki confirmam essa escolha]
**Alternativas:** [2-3 outros candidatos e o que os diferencia]
**Para confirmar:** [1-2 pistas adicionais que resolveriam a dúvida]

Responda sempre em português.
```

3. Faça upload dos arquivos de `wiki/countries/`, `wiki/concepts/` e `wiki/index.md`

---

## Fontes

- [Plonk It](https://www.plonkit.net) — guia principal por país (fonte primária)
- [GeoTips](https://geotips.net) — dicas da comunidade competitiva
- [GeoHints](https://geohints.com) — referência de metas visuais
- [Geomastr](https://geomastr.com) — dados factuais por país
- [GeoDummy](https://geodummy.com) — repositório histórico

---

*Conteúdo das fontes licenciado sob [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) conforme Plonk It. Uso não-comercial.*
