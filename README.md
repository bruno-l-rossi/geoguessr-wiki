# 🌍 GeoScout Wiki

Base de conhecimento para identificação de países no GeoGuessr, construída para servir como material de estudo e consulta durante o jogo.

---

## O que é

Uma coleção estruturada de guias por país com foco em pistas visuais do Google Street View — o tipo de informação que você precisa para identificar rapidamente onde está no mapa. Cada página cobre câmera, vegetação, arquitetura, placas, bollards, regiões e pegadinhas comuns.

O wiki alimenta o **GeoScout**, um agente de IA que, dado o que você descreve na tela, consulta a base e indica o país mais provável com raciocínio e alternativas.

---

## Cobertura

- **+140 países** com guias individuais
- **Conceitos transversais**: gerações de câmera, lado de direção, tipos de bollards, alfabetos, vegetação por bioma, estilos arquitetônicos regionais
- **Guias gerais**: introdução ao GeoGuessr, países de spillover

---

## Metodologia

O conteúdo foi construído em três etapas:

**1. Coleta de fontes**
Páginas de referência da comunidade GeoGuessr foram capturadas via [Obsidian Web Clipper](https://obsidian.md/clipper) e armazenadas em `raw/countries/`. A fonte primária é o [Plonk It](https://www.plonkit.net), principal guia colaborativo da comunidade.

**2. Compilação automatizada**
Os arquivos brutos foram processados pelo [Claude Code](https://claude.ai/code) usando um schema de instruções (`CLAUDE.md`) que define a estrutura de cada página, convenções de nomenclatura e operações de ingestão. O agente lê as fontes, extrai as informações relevantes e gera páginas padronizadas em Markdown com wikilinks entre países e conceitos relacionados.

**3. Manutenção contínua**
Novas fontes são adicionadas a `raw/` e processadas incrementalmente — sem reescrever o que já existe. Health checks periódicos identificam lacunas, contradições e conteúdo desatualizado.

---

## Estrutura

```
wiki/
├── countries/     # Um arquivo .md por país
├── concepts/      # Conceitos transversais (câmera, bollards, etc.)
├── outputs/       # Respostas a consultas e relatórios
└── index.md       # Índice mestre
raw/
└── countries/     # Fontes brutas antes da compilação
CLAUDE.md          # Schema de instruções para o agente
```

---

## Como usar com o GeoScout

1. Acesse [claude.ai](https://claude.ai) e crie um **Project** chamado `GeoScout`
2. Cole o prompt do agente nas instruções do Project
3. Faça upload dos arquivos de `wiki/countries/`, `wiki/concepts/` e `wiki/index.md`
4. Inicie uma nova conversa e descreva o que você vê na tela

O Claude consulta apenas os arquivos do wiki — sem conhecimento externo.

---

## Fontes

- [Plonk It](https://www.plonkit.net) — guia principal por país
- [GeoTips](https://geotips.net) — dicas da comunidade competitiva
- [GeoHints](https://geohints.com) — referência de metas visuais

---

*Conteúdo das fontes licenciado sob [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) conforme Plonk It. Uso não-comercial.*
