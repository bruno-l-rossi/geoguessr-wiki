---
title: "GeoGuessr Wiki — Log de Operações"
---

# Log de Operações

---

## 2026-04-10 — CORREÇÕES PÓS-LINT: Pendências do relatório v2

**Operação:** Correção de todos os itens pendentes identificados no LINT v2

**Links para países sem cobertura — convertidos para texto plano:**
- `alphabet-scripts.md`: `[[georgia]]` → "Georgia" + `[[saudi-arabia]]` → "Arábia Saudita"
- `vegetation-zones.md`: `[[maldives]]` → "Maldivas"

**Conceitos legado — notas de redirecionamento adicionadas:**
- `bollards-europa.md` → redireciona para [[bollards]]
- `camera-altura.md` → redireciona para [[camera-generations]]
- `trafego-esquerda.md` → redireciona para [[driving-side]]

**Novos conceitos criados:**
- `wiki/concepts/chevrons.md` — setas de curva por país: tabela fundo×seta, pares confusos (SE=azul+amarelo exclusivo; PT=preto+amarelo exclusivo; AR=branco+vermelho exclusivo nas Américas; FR/ES=azul+branco grupo de 2; NO/FI/IS=preto+amarelo grupo de 3)
- `wiki/concepts/guardrails.md` — barreiras de proteção por país: tipos de viga, refletores diagnósticos (PT=vermelho, ES=amarelo, PE=preto+amarelo alternado), postes de madeira Noruega, ponte Uruguai spill Gen 4

**Atualizado:** `wiki/index.md` (conceitos 20→22); `wiki/log.md`

**Resultado final do LINT:** 0 wikilinks quebrados, 0 orphans, 0 frontmatter incompleto, 0 seções ausentes, 0 contradições abertas.

---

## 2026-04-10 — LINT v2: Relatório de qualidade completo (segunda edição)

**Operação:** LINT  
**Escopo:** 136 países + 20 conceitos + 2 outputs  
**Output gerado:** `wiki/outputs/lint-report-2026-04-10.md` (sobrescrito — v2)

**Problemas encontrados e corrigidos:**
- ❌→✅ `brazil.md`: `[[postes-brasil\|...]]` → barra invertida corrigida
- ❌→✅ `trafego-esquerda.md`: `[[japan\|...]]` e `[[south-africa\|...]]` → barras invertidas corrigidas
- ❌→✅ `driving-side.md` linha 102: Namíbia listada erroneamente na tabela de "países de direita" → reescrita com fato correto (esquerda)
- ❌→✅ `study-guide.md` linha 630: "Trânsito direita = Namíbia" → corrigido
- ❌→✅ `study-guide.md` Part 1 seção 7: afirmação "único de direita no cluster" → reescrita

**Problemas identificados mas NÃO corrigidos (ver relatório):**
- `[[georgia]]` em `alphabet-scripts.md` → país sem página; converter para texto plano
- `[[saudi-arabia]]` em `alphabet-scripts.md` → idem
- `[[maldives]]` em `vegetation-zones.md` → idem
- "chevrons" mencionado 180x sem conceito próprio → candidato a `wiki/concepts/chevrons.md`
- "guardrails" mencionado 127x sem conceito próprio → candidato a `wiki/concepts/guardrails.md`
- 3 conceitos legado sem nota de redirecionamento (bollards-europa, camera-altura, trafego-esquerda)

**Resultado limpo:**
- 0 páginas órfãs
- 0 frontmatter incompleto
- 0 seções padrão ausentes
- 0 Resumo Rápido com ≠ 5 bullets
- 0 países ausentes do index.md

---

## 2026-04-10 — QUERY: Guia de Estudo Estratégico

**Operação:** QUERY  
**Fonte:** Leitura de todos os 136 arquivos de países + 20 conceitos  
**Arquivo gerado:** `wiki/outputs/study-guide.md`

**Conteúdo produzido:**
- **Parte 1 — 20 países mais difíceis:** Nepal, Camboja, Laos, Botswana, Lesoto, Eswatini, Namíbia, Sri Lanka, Equador, Colômbia, Moldávia, Hungria, Bulgária, Liechtenstein, Suíça, Taiwan, Albânia, Macedônia do Norte, Mongólia, Hong Kong — cada um com âncora diagnóstica
- **Parte 2 — 10 pares mais confundidos:** Japão/Suíça, ZA/BW/LS/SZ, AU/NZ, ES/PT/FR, RO/BG/HU, TH/LA/KH, BR/CO/EC/MX, CA/US, AR/UY/PE, FR/BE/NL — tabelas de diferenças + regra mnemônica por par
- **Parte 3 — 15 pistas mais universais:** lado de condução, script, câmera, bollards, postes, linhas de estrada, sinais/velocidade, vegetação, arquitetura, topografia, veículos, placas, palavras-chave, cor da linha externa, vending machines — com confiabilidade e quando falha
- **Parte 4 — Plano de estudo em 4 estágios:** Estágio 1 (fundação: condução+script+bollards+linhas), Estágio 2 (especialização por continente), Estágio 3 (pares difíceis), Estágio 4 (pinpoint regional: Brasil por estado, Japão por região, África do Sul por província, Índia por script); cada estágio com checkpoint e meta de desempenho

**Atualizado:** `wiki/index.md` (output adicionado, contagem 1→2); `wiki/log.md`

---

## 2026-04-10 — INGEST: 8 Conceitos Gerais (câmera, condução, bollards, estradas, postes, scripts, vegetação, arquitetura)

**Operação:** INGEST (criação de conceitos transversais a partir de todos os 136 países)  
**Fonte:** Leitura e síntese de todos os arquivos em `wiki/countries/`

**Arquivos criados:**
- `wiki/concepts/camera-generations.md` — países por geração de câmera (Gen 2/3/4, shitcam, lowcam, smallcam, trekker, tripod); carros Google diagnósticos por país
- `wiki/concepts/driving-side.md` — todos os países que dirigem pela esquerda organizados por continente; pares confusos (AU/NZ, JP/TH/ID, UK/IE, ZA/BW/LS, USVI/PR); regra histórica de herança britânica
- `wiki/concepts/bollards.md` — catálogo por continente: Europa (FR 3 variantes, DE, ES, UK, PT, FI, NO, LT, SE, DK, HU, AT, NL, BE, CH, LI, RO), Américas (MX, UY, PE, CL, GT, EC), Ásia (JP, KG, IL, QA, TR), África (ZA, BW, SN, RW), Oceania (AU, NZ), Ilhas (MN pino de boliche); tabela de pares confusos
- `wiki/concepts/road-lines.md` — linha externa amarela (África Austral, Oriente Médio, Bermudas); designs exclusivos (Linha-Z França, tripla África do Sul, quadrados Dinamarca, entrada localidade França); padrões por região; qualidade e material da estrada
- `wiki/concepts/utility-poles.md` — Europa (FR escada/waffle/losango/flecha+isolador, DE adesivos brancos, LT concreto quadrado+diagonal, GR madeira+frame metálico+5 fios, RO concreto+5 buracos longos), Ásia (JP 10 regiões de transformador, TH concreto quadrado, PH octogonal, IN caótico), Américas (BR [[postes-brasil]], AR duplo paralelo, GT pintado rosa+verde, EC escada, BO madeira curvada), África (ZA bird poles+tabela por província), Oceania (AU Stobie poles), Ilhas (HI amarelo+guitarra, LB malha metálica)
- `wiki/concepts/alphabet-scripts.md` — scripts únicos (JP 3 sistemas, KR hangul, LK sinhala, TH tailandês, KH khmer, LA lao); cirílico por país com letras exclusivas (BY=Ў/І, MN=Ɵ/Ү, UA=Ї/І, RS=biscript); árabe por país; devanagari+scripts sul-asiáticos por estado indiano; diacríticos latinos de alta confiança; palavras diagnósticas (ALTO/PARE/DUR/ARRÊT/Rue/-gade/karrika)
- `wiki/concepts/vegetation-zones.md` — 10 zonas (taiga, temperada, mediterrânea, estepe, deserto, savana, cerrado, tropical densa, costeira, alpina); espécies diagnósticas (araucária, baobá, palmeira de óleo, moriche, feto arborescente, bétula); pares confusos
- `wiki/concepts/architecture-styles.md` — Europa Ocidental (FR ardósia/enxaimel/pedra bege, DE fachwerk, UK tijolo geminado, PT azulejos, ES telha árabe+caiação), Europa Oriental (RU isba+soviético, RO portões entalhados, LT soviético), Oriente Médio (LB arcos triplos), África (ZA Cape Dutch gable, MN ger/yurt), Américas (BO tijolos grandes vermelhos, CL adobe+triângulo, PE varões expostos), tabela de muros e cercas por material; elementos diagnósticos de alta confiança

**Atualizado:**
- `wiki/index.md` — 8 novos conceitos adicionados à tabela; conceitos legado marcados; contagem 12 → 20
- `wiki/log.md` — este registro

---

## 2026-04-10 — INGEST: Beginner's Guide + Spillover Countries

**Operação:** INGEST (guias gerais → wiki/concepts/)
**Fontes:**
- `raw/countries/Beginner's Guide to Geoguessr.md` (plonkit.net/beginners-guide)
- `raw/countries/Spillover countries.md` (plonkit.net/spillover-countries)

**Arquivos criados:**
- `wiki/concepts/guia-iniciante.md` — mecânicas, modos de jogo, tipos de pistas (sol, lado de condução, idioma, arquitetura, vegetação, infraestrutura, meta de câmera), estratégias por região, glossário completo (17 termos)
- `wiki/concepts/spillover-countries.md` — 8 locais de spillover com pistas visuais diagnósticas por ponto

**Páginas de países atualizadas com informação de spillover:**
- `wiki/countries/tanzania.md` — detalhes dos 2 pontos de spill do Quênia (Rongai: terra→asfalto+meios-fios P&B+pinheiros; Namanga: casinha branca+follow car) + wikilinks adicionados
- `wiki/countries/belarus.md` — seção "9b. Spillover da Rússia" com P21 (linha amarela+entardecer) e E30 (placa ВИЦЕБСКАЯ ВОБЛ.) + wikilinks
- `wiki/countries/monaco.md` — Gen 3 spill da França documentado em Seção 2 (noroeste+nordeste, antena curta) + aviso em Seção 9 + wikilinks
- `wiki/countries/uruguay.md` — Gen 4 spill em Seção 2 (ponte guardrail branco+rotatória octogonal) + wikilink

**Conceito atualizado:**
- `wiki/concepts/gerações-de-câmera.md` — adicionados Shitcam (Índia, Nigéria, Camboja, Líbano, Equador), Lowcam (Japão, Suíça, Liechtenstein + Sri Lanka Gen 4) e Tripod; atualizado Smallcam com mais países

**Países spillover sem wiki própria (documentados no spillover-countries mas sem página):**
- Gâmbia (spill do Senegal)
- Guiana (spill do Brasil)
- Venezuela (spill da Colômbia e Brasil)
- Paraguai (gen spill do Brasil)

---

## 2026-04-10 — LINT: Relatório de qualidade completo

**Operação:** LINT  
**Output gerado:** `wiki/outputs/lint-report-2026-04-10.md`

**Problemas encontrados e corrigidos:**
- ❌→✅ `czechia.md` ausente do index.md → adicionado na seção Europa Oriental
- ❌→✅ Contagem "118 países" no index.md → corrigido para 136
- ❌→✅ 3 wikilinks quebrados em brazil.md e palmeiras-brasil.md:
  - `[[amazônia]]` → criado `wiki/concepts/amazônia.md`
  - `[[caatinga]]` → criado `wiki/concepts/caatinga.md`
  - `[[cerrado]]` → criado `wiki/concepts/cerrado.md`
- ✅→📋 index.md atualizado com 3 novos conceitos e 1 output

**Problemas identificados mas NÃO corrigidos (ver relatório):**
- 3 conceitos órfãos (bollards-europa, camera-altura, trafego-esquerda) — 0 links de entrada
- 133/136 países sem wikilinks internos
- Candidatos a novos conceitos: low-cam, shitcam, eucaliptos, betulas, postes-escada, bird-poles

---

## 2026-04-10 — RE-INGEST: França, Japão, África do Sul (dual-source)

**Operação:** RE-INGEST (reescrita com ambas as fontes raw)  
**Arquivos reescritos:** `wiki/countries/france.md`, `wiki/countries/japan.md`, `wiki/countries/south-africa.md`

**Motivação:** As versões originais foram compiladas apenas com os arquivos `-plonkit.md` (notas de web search), ignorando os clippings diretos do plonkit.net (`France.md`, `Japan.md`, `South Africa.md`) que foram adicionados ao raw depois.

**Conteúdo novo incorporado — França:**
- 3 variantes de bollard (cônico, duas ranhuras, cunha achatada)
- Postes escada/waffle, topo em losango, topo em flecha+isolador (exclusivo)
- Linha-Z (blocos duplos deslocados — exclusivo)
- Marcadores de estrada bandeira austríaca (exclusivos)
- Cores regionais dos postes (verde, marrom em Seine-et-Marne, bordô em Haute-Garonne)
- Arquitetura regional detalhada (ardósia Bretanha, tijolo laranja Toulouse, pedra creme Paris, etc.)
- 6 idiomas regionais com sufixos diagnósticos (bretão Plou-, alsaciano -heim/-gasse, occitano carrièra, basco karrika, catalão carrer, corso -u/-iu)
- Asfalto avermelhado em Borgonha

**Conteúdo novo incorporado — Japão:**
- Detalhes do low-cam (borrão maior, estrada mais larga)
- Carro preto e branco; Suíça = único outro low-cam (mas borrrado)
- Três sistemas de escrita explicados (kanji/hiragana/katakana)
- Refletores: verticais/curtos (Japão) vs. diagonais ao chão (Taiwan) vs. diagonais grossos (Coreia)
- Linhas de estrada: nunca linha externa amarela
- Bollards: brancos com refletor circular no topo
- Guardrails brancos simples
- Escudos hexagonais de prefeitura
- Sinal de PARE único; faixa de pedestres escolar distinta
- Transformadores por 10 regiões (Hokkaido, Tohoku, Kanto, Hokuriku, Chubu, Kansai, Chugoku, Shikoku, Kyushu, Okinawa)
- Acessórios regionais (seta laranja Chugoku, bandas laranja+preto Shikoku, acessórios 120° Kansai, 90° Shikoku)
- Blocos cinzas de isolador (Chubu/Kansai/Chugoku/Shikoku)

**Conteúdo novo incorporado — África do Sul:**
- Gen 2 = único na África → confirma África do Sul
- Gen 4 smallcam detalhado
- Bird poles (1-5 barras horizontais com isoladores brancos finos)
- Linha externa amarela; linha central tripla única
- Sistema N/R (exclusivo ZA) vs. A/B (Botswana/Lesoto/Namíbia) vs. MR (Eswatini)
- Sinais de aviso triangulares (vs. losango amarelo AU/NZ)
- Placas por província: Free State (verde), KZN (azul)
- Topos de poste por região (A = Western Cape, tridente = KZN, '<' = Limpopo/NW, 3 horizontais = norte, braços = Mpumalanga)
- Adesivos nos sinais (vermelho = Eastern Cape; branco = Cape provinces)
- Asfalto rosado em Limpopo; ninhos no Northern Cape; usinas em Mpumalanga
- Cook pine trees (East London–Durban)

---

## 2026-04-10 — BATCH INGEST: 38 países (sessões 2 e 3)

**Operação:** BATCH INGEST (continuação de sessão anterior)  
**Fonte:** `raw/countries/` (arquivos clipados de plonkit.net)  
**Sessão 2 (países H–O):** hawaii, hong-kong, iraq, israel-and-the-west-bank, jordan, kazakhstan, kyrgyzstan, laos, lebanon, lesotho, macau, madagascar, mali, martinique, mongolia, namibia, nepal, northern-mariana-islands, oman  
**Sessão 3 (países P–V):** pakistan, panama, pitcairn-islands, puerto-rico, qatar, reunion, rwanda, saint-pierre-and-miquelon, sao-tome-and-principe, senegal, south-georgia-and-sandwich-islands, sri-lanka, tanzania, tunisia, uganda, united-arab-emirates, us-minor-outlying-islands, us-virgin-islands, vanuatu

**Total de arquivos criados nessas sessões:** 38 páginas wiki em `wiki/countries/`

**Notas metodológicas:**
- Arquivos raw grandes (>150 linhas) lidos parcialmente (primeiras 150 linhas), que contêm as pistas de Step 1 mais importantes
- Estrutura padrão do CLAUDE.md seguida em todos os arquivos: 10 seções + frontmatter YAML
- Todos os níveis de confiança indicados (alta/média/baixa)
- Avisos ⚠️ adicionados para pistas que se sobrepõem com países vizinhos
- Resumo Rápido com exatamente 5 bullet points em cada página
- Países que contam como outro país para streaks indicados claramente (ex: Porto Rico = EUA, Martinica = França)

**Atualizado:** `wiki/index.md` com todas as 118 entradas organizadas por região

---

---

## 2026-04-09 — INGEST: raw/countries/Brazil.md (Plonk It)

**Operação:** INGEST  
**Fonte:** `raw/countries/Brazil.md` (clipado de https://www.plonkit.net/brazil)  
**Arquivos modificados:** `wiki/countries/brazil.md`  
**Arquivos criados:** `wiki/concepts/postes-brasil.md`, `wiki/concepts/palmeiras-brasil.md`, `wiki/concepts/araucária.md`

**Novidades incorporadas ao brazil.md:**
- **Câmera:** Detalhes do Gen 3 (antena stubby com espiral vs. sem antena); confirmação do smallcam Gen 4 (único na SA junto com Peru e Argentina); borrão fixo no Amapá (Gen 4); rifts no Alagoas (Gen 3).
- **Infraestrutura — Postes:** Tipos de poste por estado (redondo = SP/sul, madeira = RS/RO/AM/RJ); topos de poste por estado (8 configurações mapeadas); isoladores por estado (12 tipos mapeados); códigos de identificação pintados/placas por estado (7 padrões mapeados); lâmpadas por cidade (15+ cidades com características únicas).
- **Vegetação:** Palmeiras detalhadas por espécie (carnaúba, babaçu, açaí, moriche/buriti, macaw, coqueiro); planta de hastes longas do Nordeste; eucalipto, cana, soja, café por estado.
- **Paisagem regional:** Acre (colinas pequenas + estradas onduladas), Roraima (planície + montanhas distantes + grama fina), Uiramuta (montanhas dobradas), RS costeiro (planície úmida), MG/RJ/ES (colinas onduladas), ES (rocha exposta).
- **Sinais/estradas:** Tipos de pavimento por estado (paralelepípedo no NE e RS; hexagonal em SC/MG; tijolo em AC; pedras irregulares em RS/SC; cascalho vermelho no Piauí); CEP e DDD como pistas de localização; siglas de estado nos marcadores.
- **Pegadinhas novas:** Paraguai (postes + fundo preto similares), RS vs. Uruguai, moriche em Colômbia/Peru, paralelepípedo quadrado em Misiones/Argentina.
- **Wikilinks adicionados:** [[gerações-de-câmera]], [[postes-brasil]], [[palmeiras-brasil]], [[araucária]], [[caatinga]], [[cerrado]], [[amazônia]].

**Conceitos criados:**
- `postes-brasil.md` — guia completo de postes por estado
- `palmeiras-brasil.md` — guia de palmeiras por espécie e região
- `araucária.md` — ficha da araucária como pista diagnóstica

---

## 2026-04-09 — RESEARCH: França, Japão, África do Sul (web search)

**Operação:** RESEARCH  
**Alvos:** [[france]], [[japan]], [[south-africa]]  
**Arquivos criados:**
- `raw/countries/france-plonkit.md`
- `raw/countries/japan-plonkit.md`
- `raw/countries/south-africa-plonkit.md`
- `wiki/countries/france.md`
- `wiki/countries/japan.md`
- `wiki/countries/south-africa.md`
- `wiki/concepts/bollards-europa.md`
- `wiki/concepts/camera-altura.md`
- `wiki/concepts/trafego-esquerda.md`

**Notas:** plonkit.net retornou 403; conteúdo obtido via WebSearch + geopinning.space + geodummy.com + geotips.net.

**Pistas principais incorporadas:**
- **França:** poste com placa azul (99%), bollard cilíndrico branco+refletor vermelho, linha central quadrados unidos, sinais "Rue", regiões por topônimos (~heim, ~ac)
- **Japão:** câmera baixa, kanji inconfundível, vending machines onipresentes, espelhos circulares nas curvas, telhados por região (preto sul / laranja-vermelho Chugoku / sem telhas Hokkaido)
- **África do Sul:** trânsito esquerda+marcações amarelas, cercas em todos edifícios, van táxi com bandeira, bollard simples, inglês/afrikáans

**Conceitos criados:**
- `bollards-europa.md` — bollards por país europeu
- `camera-altura.md` — altura de câmera como pista de identificação
- `trafego-esquerda.md` — lista de países com trânsito pela esquerda

---

## 2026-04-09 — RESEARCH: Brasil (web search)

**Operação:** RESEARCH  
**Alvo:** [[brazil]]  
**Arquivo criado:** `wiki/countries/brazil.md` (versão inicial)

**Fontes consultadas:**
- GeoTips — South America (geotips.net/south-america)
- Plonk It — Brazil (plonkit.net/brazil) — via busca web (403 no acesso direto)
- Geodummy — Brazil (geodummy.com/brazil)
- Geomastr — Coverage, Bollards (geomastr.com)
- GeoHints — Camera Gens (geohints.com)
- Geopinning Space — Brazil (geopinning.space)

---
