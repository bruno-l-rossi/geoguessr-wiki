---
title: "LINT Report — 2026-04-17"
date_created: 2026-04-17
type: output
---

# Relatório LINT — 2026-04-17

Verificação completa de qualidade de toda a base wiki: 136 arquivos em `wiki/countries/`, 22 arquivos em `wiki/concepts/`, `wiki/index.md`.

---

## Resumo Executivo

| Categoria | Problemas Encontrados | Corrigidos Automaticamente | Atenção Manual |
|---|---|---|---|
| Frontmatter incompleto (países) | 0 | — | — |
| Frontmatter incompleto (conceitos) | 20 sem `sources` | 0 | baixa prioridade |
| Wikilinks quebrados | 0 ativos | — | — |
| Páginas órfãs | 0 | — | — |
| Contradições entre páginas | 0 encontradas | — | — |
| Seções faltando (países) | 2 | 2 corrigidos | — |
| Qualidade do índice | OK | — | — |
| Consistência de nomes | OK | — | — |

**Total de problemas reais encontrados: 2** (ambos corrigidos automaticamente nesta sessão).

---

## 1. Frontmatter — Países

Todos os 136 arquivos em `wiki/countries/` possuem:
- `title`, `date_created`, `date_modified`, `summary`, `tags`, `type`, `status`: **presentes em todos**
- `sources`: **presente em todos** (adicionado em sessão anterior — sweep completo de geomastr.com em 2026-04-14)

**Status: OK.**

---

## 2. Frontmatter — Conceitos

Os 22 arquivos em `wiki/concepts/` não possuem `sources` field:

`alphabet-scripts`, `amazônia`, `araucária`, `architecture-styles`, `bollards-europa`, `bollards`, `caatinga`, `camera-altura`, `camera-generations`, `cerrado`, `chevrons`, `driving-side`, `gerações-de-câmera`, `guardrails`, `guia-iniciante`\*, `palmeiras-brasil`, `postes-brasil`, `road-lines`\*, `spillover-countries`, `trafego-esquerda`, `utility-poles`, `vegetation-zones`

\* `guia-iniciante.md` e `road-lines.md` têm `sources` — foram atualizados na sessão de 2026-04-17.

**Avaliação:** O template do CLAUDE.md não exige `sources` para conceitos. Inconsistência menor. **Não corrigido** — baixa prioridade.

---

## 3. Wikilinks Quebrados

Verificação via Grep em todos os arquivos de conceitos para wikilinks referenciando países sem arquivo correspondente.

**Resultado:** Nenhum wikilink quebrado encontrado nos arquivos ativos.

> Nota: A sessão de lint anterior (2026-04-10) reportou `[[georgia]]`, `[[maldives]]`, `[[saudi-arabia]]` como quebrados. Verificação confirmou que essas ocorrências estão apenas no arquivo `wiki/outputs/lint-report-2026-04-10.md` (documentação histórica) e em `wiki/log.md` — não nos arquivos de conceito. Já corrigidos em sessão anterior.

**Status: OK.**

---

## 4. Páginas Órfãs

Verificação de conceitos sem referências de entrada de páginas de país.

Conceitos principais (`bollards`, `road-lines`, `gerações-de-câmera`, `guia-iniciante`, `spillover-countries`) aparecem referenciados em múltiplas páginas de país.

Conceitos de bioma (`amazônia`, `cerrado`, `caatinga`, `araucária`) são referenciados em `brazil.md`.

**Status: OK** — nenhuma página órfã identificada.

---

## 5. Contradições entre Páginas

Verificação de pistas conflitantes entre páginas de países e conceitos.

**Casos verificados:**
- `road-lines.md` vs países individuais (México, Noruega, Filipinas, etc.): consistentes
- `driving-side.md` vs `trafego-esquerda.md`: complementares, sem contradição
- `gerações-de-câmera.md` vs `guia-iniciante.md`: consistentes

**Status: OK** — nenhuma contradição encontrada.

---

## 6. Seções Faltando — Países

### Problema 1: `canada.md` — ausência de seção "Vegetação e Paisagem"
**Identificado:** Arquivo seguia numeração não-padrão com seções 4 ("Bollards") e 5 ("Infraestrutura") — nenhuma seção de vegetação documentada.
**Corrigido:** Adicionada seção `## 4. Vegetação e Paisagem` com tabela de biomas (boreal/taiga, pradarias, BC temperada, Ontario/Québec folhosas, marítimo, PEI solo vermelho, ártico/tundra) e nota sobre maple trees. Seções subsequentes renumeradas (4→5 Bollards, 5→6 Infraestrutura, ..., 10→11 Resumo Rápido).
**Data da correção:** 2026-04-17

### Problema 2: `united-states.md` — seção de Arquitetura misturada com Vegetação
**Identificado:** Seção 5 ("Vegetação e Paisagem") continha itens de arquitetura/infraestrutura (casas móveis, igrejas batistas, torres de água, cadeias americanas). Nenhuma seção dedicada de "Arquitetura e Infraestrutura".
**Corrigido:** 
- Seção 5 limpa para conter apenas vegetação/paisagem por região
- Adicionada seção `## 6. Arquitetura e Infraestrutura` dedicada (casas móveis, igrejas batistas, torres de água, barris de construção, marcadores de gasoduto/fibra, postos de combustível, redes de fast food)
- Seções subsequentes renumeradas (7→8 Veículos, 8→9 Regiões, 9→10 Pegadinhas, 10→11 Resumo Rápido)
**Data da correção:** 2026-04-17

### Observação: `china.md`
O agente de análise reportou possível ausência de seção 8. Verificação confirmou que `china.md` possui `## 8. Regiões/Cobertura Disponível` — heading válido com nomenclatura adaptada. **Sem problema.**

**Status: 2 problemas corrigidos.**

---

## 7. Qualidade do Índice (`wiki/index.md`)

- Indexa todos os países com `date_modified: 2026-04-17` (atualizado em sessão anterior)
- Links para todas as páginas de conceito principais
- Contagem correta de países documentados

**Status: OK.**

---

## 8. Consistência de Nomes de Arquivo

Verificação de convenção kebab-case:
- Todos os arquivos em `wiki/countries/` seguem kebab-case minúsculo
- Todos os arquivos em `wiki/concepts/` seguem kebab-case (exceção: `gerações-de-câmera.md` usa caracteres acentuados — comportamento aceito, consistente com outros arquivos do projeto)

**Status: OK.**

---

## O Que Foi Corrigido Automaticamente

| Arquivo | Correção |
|---|---|
| `wiki/countries/canada.md` | Adicionada seção `## 4. Vegetação e Paisagem`; seções renumeradas 4→11 |
| `wiki/countries/united-states.md` | Seção 5 limpa; adicionada seção `## 6. Arquitetura e Infraestrutura`; renumeração |

---

## O Que Requer Atenção Manual

| Item | Prioridade | Descrição |
|---|---|---|
| `sources` em conceitos | Baixa | 20 arquivos de conceito sem campo `sources` — CLAUDE.md não exige, mas é inconsistente |
| `canada.md` vegetação | Média | Seção adicionada é básica — pode ser expandida com mais pistas visuais de bioma |
| `united-states.md` regiões | Baixa | Seção 9 (Regiões) tem nota `*(Muito vasto — ver raw para detalhes)*` — indica conteúdo pendente |

---

*Gerado por operação LINT em 2026-04-17.*
