---
title: "LINT Report — 2026-04-10 (v2)"
date_created: 2026-04-10
date_modified: 2026-04-10
summary: "Segunda edição do relatório de qualidade. Cobre 136 países, 20 conceitos e 2 outputs. Corrigidos: contradição crítica da Namíbia (driving side), 3 wikilinks com barra invertida. Pendentes: 3 links para países sem página, 2 conceitos candidatos (chevrons, guardrails)."
tags: [output, lint, qualidade]
type: output
---

# LINT Report — 2026-04-10 (v2)

> Segunda execução do LINT. Cobre 136 arquivos de países + 20 conceitos + 2 outputs, após a criação dos 8 conceitos transversais e do guia de estudo.

---

## Estatísticas Gerais

| Métrica | Valor |
|---|---|
| Arquivos em wiki/countries/ | 136 |
| Arquivos em wiki/concepts/ | 20 |
| Arquivos em wiki/outputs/ | 2 |
| Wikilinks quebrados encontrados | 6 reais + 1 falso positivo |
| Páginas órfãs (sem links de entrada) | 0 |
| Frontmatter incompleto | 0 |
| Seções padrão ausentes | 0 |
| Resumo Rápido com ≠ 5 bullets | 0 |
| Países ausentes do index.md | 0 |
| Contradições factuais | 1 crítica — **corrigida** |

---

## 1. Wikilinks Quebrados

### 1a. Barras Invertidas — CORRIGIDOS ✅

Três wikilinks com barra invertida (`\`) no lugar do pipe (`|`), tornando os links inválidos.

| Arquivo | Link com erro | Correção aplicada |
|---|---|---|
| `wiki/countries/brazil.md` | `[[postes-brasil\|Postes em escada]]` | `[[postes-brasil|Postes em escada]]` |
| `wiki/concepts/trafego-esquerda.md` | `[[japan\|Japão]]` | `[[japan|Japão]]` |
| `wiki/concepts/trafego-esquerda.md` | `[[south-africa\|África do Sul]]` | `[[south-africa|África do Sul]]` |

**Status:** corrigidos nesta sessão.

---

### 1b. Links para Países sem Página — PENDENTE ⚠️

Três wikilinks apontam para países sem página em `wiki/countries/`:

| Link | Arquivo de origem | Nota |
|---|---|---|
| `[[georgia]]` | `wiki/concepts/alphabet-scripts.md` | Geórgia não tem cobertura Street View no GeoGuessr — mencionada como exemplo de script georgiano |
| `[[saudi-arabia]]` | `wiki/concepts/alphabet-scripts.md` | Arábia Saudita sem cobertura oficial |
| `[[maldives]]` | `wiki/concepts/vegetation-zones.md` | Maldivas: cobertura muito limitada/duvidosa |

**Ação recomendada:** converter os três para texto plano (remover `[[` e `]]`), pois esses países não têm e provavelmente não terão páginas no wiki por ausência de cobertura Street View.

---

### 1c. Falso Positivo (OK)

| Link | Arquivo | Motivo |
|---|---|---|
| `[[wikilink]]` | `wiki/outputs/lint-report-2026-04-10.md` | Exemplo de sintaxe no relatório da v1 — não é link navegável |

---

## 2. Contradição Factual Crítica — CORRIGIDA ✅

### Namíbia: lado de condução

**Fato correto:** A Namíbia dirige pela **esquerda** (herança sul-africana/britânica). Confirmado por `namibia.md` e pela entrada correta em `driving-side.md` linha 64.

**Erros encontrados e corrigidos:**

| Arquivo | Texto incorreto | Correção |
|---|---|---|
| `wiki/concepts/driving-side.md` (linha 102) | `[[namibia]] *(direita)* — confirmado` na tabela de países de direita — linha editoriamente contraditória | Linha reescrita: Namíbia movida para o grupo correto com nota sobre Angola/Zâmbia ao norte |
| `wiki/outputs/study-guide.md` (linha 630) | `"Trânsito **direita** = Namíbia"` na regra mnemônica do cluster Sul-africano | Substituído por `"árido extremo + pickup branco antena esquerda = Namíbia"` |
| `wiki/outputs/study-guide.md` Part 1, seção 7 | Afirmava "Único país do cluster Sul-africano que dirige pela **direita**" | Reescrito com fatos corretos: trânsito esquerda, árido, pickup branco, topônimos alemães |

---

## 3. Páginas Órfãs

**Resultado: nenhuma.**

Todos os 136 países e 20 conceitos têm ao menos 1 link de entrada. A criação dos 8 conceitos transversais e sua inclusão no `index.md` eliminou o problema de orphans que existia na v1 deste relatório (onde `bollards-europa`, `camera-altura` e `trafego-esquerda` não tinham links de entrada).

---

## 4. Frontmatter

**Resultado: sem problemas.**

Todos os 156 arquivos de `wiki/countries/` e `wiki/concepts/` têm os 7 campos obrigatórios completos: `title`, `date_created`, `date_modified`, `summary`, `tags`, `type`, `status`.

---

## 5. Estrutura Padrão de Páginas de País

**Resultado: sem problemas.**

Todos os 136 arquivos de países contêm:
- As 10 seções obrigatórias (`## 1.` a `## 10.`) ✅
- Resumo Rápido com exatamente 5 bullet points ✅

---

## 6. Índice (wiki/index.md)

**Resultado: sem inconsistências.**

- 136 países em `wiki/countries/` = 136 entradas no `index.md` ✅
- 20 conceitos em `wiki/concepts/` = 20 entradas no `index.md` ✅
- 2 outputs em `wiki/outputs/` = 2 entradas no `index.md` ✅
- Contagem de estatísticas: 136 países / 20 conceitos / 2 outputs ✅

---

## 7. Termos Muito Mencionados sem Conceito Próprio

Termos que aparecem centenas de vezes no wiki mas não têm página de conceito dedicada. Alguns são cobertos parcialmente; outros são candidatos claros.

| Termo | Frequência | Cobertura atual | Prioridade |
|---|---|---|---|
| "trekker" | 284x | [[gerações-de-câmera]] e [[camera-generations]] | Baixa — já coberto |
| "chevrons" | 180x | Mencionado em dezenas de países sem unificação | **Alta** |
| "guardrails" | 127x | Mencionado em dezenas de países sem unificação | **Alta** |
| "shitcam" | 97x | [[gerações-de-câmera]] e [[camera-generations]] | Baixa — já coberto |
| "smallcam" | 66x | [[gerações-de-câmera]] e [[camera-generations]] | Baixa — já coberto |
| "lowcam" | 37x | [[gerações-de-câmera]] e [[camera-generations]] | Baixa — já coberto |
| "stobie poles" | 9x | [[utility-poles]] | Baixa — já coberto |
| "bird poles" | 10x | [[utility-poles]] e [[south-africa]] | Baixa — já coberto |

### Conceito candidato: `chevrons.md`

Chevrons (setas de curva na beira da estrada) são mencionados 180x com clues diagnósticos claros:

| País | Design | Exclusividade |
|---|---|---|
| [[brazil]] | Amarelo sobre fundo **preto** | Alta — exclusivo na América do Sul |
| [[argentina]] | **Branco + vermelho** | Alta — exclusivo na América do Sul |
| [[germany]] | Preto + branco | Média |
| [[france]] | Preto + branco + marcadores bandeira austríaca | Média-alta |
| [[spain]] | Preto + branco + refletor **azul** | Média |
| [[portugal]] | Branco + preto ou branco + vermelho | Média |
| [[united-kingdom]] | Amarelo sobre preto | Média |

### Conceito candidato: `guardrails.md`

Guardrails (barreiras laterais de proteção) são mencionados 127x com clues diagnósticos:

| País | Design | Exclusividade |
|---|---|---|
| [[uruguay]] | Refletores amarelos/vermelhos alternados | Alta |
| [[brazil]] | Metálico prata, normalmente sem refletores coloridos | Média |
| [[argentina]] | Metálico prata simples | Média |
| [[france]] | Com marcadores bandeira austríaca integrados | Média |

---

## 8. Conceitos Legado — Status

Três conceitos criados na sessão anterior foram marcados como "(legado)" no `index.md` porque foram substituídos por conceitos mais completos:

| Conceito legado | Supercedido por | Situação |
|---|---|---|
| [[bollards-europa]] | [[bollards]] (cobertura global) | Mantido por compatibilidade de links |
| [[camera-altura]] | [[camera-generations]] (mais completo) | Mantido por compatibilidade de links |
| [[trafego-esquerda]] | [[driving-side]] (mais completo) | Mantido por compatibilidade de links; 3 wikilinks com barra invertida corrigidos |

**Ação recomendada:** adicionar no topo de cada um uma nota de redirecionamento (`> Ver versão completa em [[driving-side]]` etc.) para evitar que futuras consultas levem ao conteúdo desatualizado.

---

## 9. Plano de Ação Priorizado

| Prioridade | Ação | Status |
|---|---|---|
| 🔴 Crítica | Corrigir Namíbia driving-side em `driving-side.md` e `study-guide.md` | ✅ Feito |
| 🔴 Crítica | Corrigir 3 wikilinks com barra invertida | ✅ Feito |
| 🟠 Alta | Converter `[[georgia]]`, `[[saudi-arabia]]`, `[[maldives]]` para texto plano | Pendente |
| 🟡 Média | Criar `wiki/concepts/chevrons.md` | Pendente |
| 🟡 Média | Criar `wiki/concepts/guardrails.md` | Pendente |
| 🟢 Baixa | Adicionar nota de redirecionamento nos 3 conceitos legado | Pendente |

---

## 10. Metodologia

- **Script:** Python com regex `\[\[([^\]|]+?)(?:\|[^\]]+)?\]\]` para extração de links
- **Cobertura:** todos os arquivos em `wiki/countries/`, `wiki/concepts/`, `wiki/outputs/`, `wiki/index.md`, `wiki/log.md`
- **Contradições:** verificação pontual para 5 pares críticos — Namíbia (driving side), Sri Lanka (lowcam), Uruguai (Gen3/4), Tailândia e Laos (trânsito). Apenas Namíbia apresentou contradição. Os outros quatro estavam consistentes entre todos os arquivos.
- **Termos candidatos:** contagem via `re.findall()` case-insensitive em todo o corpus textual do wiki

---

Relacionados: [[study-guide]] | [[driving-side]] | [[bollards]] | [[camera-generations]] | [[utility-poles]]
