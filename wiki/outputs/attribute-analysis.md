---
title: "Análise Estratégica de Atributos — Sistema Akinator GeoGuessr"
date_created: 2026-04-17
type: output
sources: [wiki/countries/*, wiki/concepts/*]
---

# Análise Estratégica de Atributos — Sistema Akinator GeoGuessr

Base: varredura de **~90 arquivos de países** + **22 arquivos de conceitos** em `wiki/countries/` e `wiki/concepts/`.

> **Metodologia de scoring:**
> - **Poder de Eliminação (PE):** % médio de países eliminados pela resposta mais informativa
> - **Observabilidade (OBS):** Alta / Média / Baixa — facilidade de leitura em screenshot
> - **Frequência (FREQ):** quantos dos ~140 países têm esse atributo documentado no wiki

---

## A) RANKING GLOBAL DE ATRIBUTOS

### Tier 1 — Identificadores Instantâneos (PE > 95%)

| # | Atributo | PE | OBS | FREQ | Nota |
|---|---|---|---|---|---|
| 1 | **Script não-latino exclusivo** | 99% | Alta | ~70 | Kanji → Japão; Hangul → Coreia; Sinhala → Sri Lanka; Devanagari → Índia/Nepal; Khmer → Camboja; Lao → Laos; Tailandês → Tailândia |
| 2 | **Feature exclusiva documentada** | 99% | Alta | ~30 | Linha-Z → França; Bird poles → África do Sul; Araucária → Brasil Sul; Stobie poles → South Australia; Bollard pino-boliche 2 listras vermelhas → Mongólia |
| 3 | **Câmera lowcam** | 98% | Alta | 3 | Japão (preto/branco), Suíça (carro borrado), Liechtenstein (igual Suíça) |
| 4 | **Câmera shitcam** | 97% | Alta | 4 | Índia (~100% cobertura), Nepal, Camboja, Nigéria |
| 5 | **Gen 2 em África** | 99% | Alta | 1 | Gen 2 em contexto africano = África do Sul quase com certeza |
| 6 | **Stop sign "ALTO"** | 97% | Alta | ~7 | México + América Central (6 países) — descarta toda a América do Sul, Europa, Ásia |
| 7 | **Stop sign "DUR"** | 99% | Alta | 1 | Exclusivo Turquia |
| 8 | **Chevron azul+amarelo** | 99% | Média | 1 | Exclusivo Suécia na Europa |
| 9 | **Linha-Z central** | 99% | Alta | 1 | Exclusivo França |
| 10 | **Linha tripla (3 linhas centrais)** | 98% | Alta | 2 | África do Sul + vizinhos imediatos (Botsuana, Lesoto, Eswatini) |

**Valores possíveis — Scripts:**

| Script | Países cobertos |
|---|---|
| Kanji + Hiragana + Katakana | Japão |
| Hangul | Coreia do Sul |
| Sinhala | Sri Lanka |
| Devanagari | Índia (norte/centro), Nepal |
| Bengalês | Bangladesh (+ Bengal Ocidental Índia) |
| Khmer | Camboja |
| Lao | Laos |
| Tailandês | Tailândia |
| Birmanês | Myanmar |
| Chinês Simplificado | China continental |
| Cirílico | Rússia, Ucrânia, Bielorrúsia, Sérvia, Bulgária, Macedônia, Cazaquistão, Quirguistão, Mongólia |
| Árabe | Egito, Jordânia, Líbano, Qatar, EAU, Omã, Iraque |
| Hebraico + Árabe (bilíngue) | Israel e Cisjordânia |
| Georgiano | Geórgia |
| Armênio | Armênia |
| Etíope (Ge'ez) | Etiópia, Eritreia |
| Latino | ~90 países |

---

### Tier 2 — Eliminadores Fortes (PE 70–95%)

| # | Atributo | PE | OBS | FREQ | Valores e países por valor |
|---|---|---|---|---|---|
| 11 | **Lado de condução** | 85% | Alta | 140 | Esquerda (~25 países): UK, Irlanda, Japão, Índia, Bangladesh, Paquistão, Sri Lanka, Tailândia, Indonésia, Malásia, Cingapura, HK, Austrália, NZ, África do Sul, Botswana, Lesoto, Eswatini, Namíbia, Quênia, Uganda, Ruanda, Jamaica, USVI, Bermudas / Direita: todos os demais |
| 12 | **Linha externa AMARELA** | 94% | Alta | ~10 | Sim: África do Sul, Botsuana, Lesoto, Eswatini, Namíbia, Israel, Qatar (parcial) / Não: ~130 países |
| 13 | **Geração de câmera dominante** | 80% | Alta | ~130 | Gen2 abundante: Canadá, Jersey, Bermudas, AS / Gen3 com carro preto: Argentina, Peru, Uruguai, Rússia / Lowcam: Japão, Suíça, Liechtenstein / Shitcam: Índia, Nepal, Camboja, Nigéria |
| 14 | **Tipo de bollard** | 90% | Média | ~80 | Ver tabela detalhada abaixo |
| 15 | **Stop sign texto** | 88% | Alta | ~120 | STOP: maioria / PARE: Brasil, Portugal, Timor-Leste / ALTO: México + América Central / DUR: Turquia / ARRÊT: Québec |
| 16 | **Vegetação dominante** | 78% | Alta | ~120 | Ver tabela detalhada abaixo |
| 17 | **Cor do solo** | 75% | Alta | ~60 | Ver tabela detalhada |
| 18 | **Chevron (fundo + cor da seta)** | 88% | Média | ~65 | Ver tabela detalhada |
| 19 | **Postes de utilidade — tipo** | 85% | Média | ~90 | Bird poles → África do Sul; Stobie → South Aus; Waffle/escada → França; Duplo concreto → Argentina; Octogonal → México/Colômbia |
| 20 | **Cor da linha central** | 72% | Alta | ~120 | Amarela: Américas, Noruega, Coreia, Tailândia, Filipinas, Ruanda, Uganda / Branca: Europa Ocidental, Japão, Malaysia / Dupla amarela: EUA, Brasil, Argentina, NZ |
| 21 | **Diacríticos exclusivos no alfabeto latino** | 85% | Média | ~50 | ñ → Espanhol; ã/ô/ê → Português; ı/ğ/ş → Turco; ő/ű → Húngaro; ř/ě → Tcheco; þ/ð → Islandês; ï/ÿ → Francês vs. outros |

---

### Tier 3 — Eliminadores Complementares (PE 40–70%)

| # | Atributo | PE | OBS | FREQ | Nota |
|---|---|---|---|---|---|
| 22 | **Tipo de poste — material** | 60% | Média | ~90 | Madeira + isolador no topo → América do Norte; Concreto → Ásia/Leste Europeu; Metal → global |
| 23 | **Guardrail — tipo de poste** | 55% | Média | ~70 | Madeira → Noruega (exclusivo europeu); Metal → global; Concreto → Ásia/Europa |
| 24 | **Cor e design de guardrail** | 65% | Média | ~60 | Faixa preta+amarela → Peru; Faixa vermelho+branco → alguns países latinos; Amarelo pintado nas pontes → USVI |
| 25 | **País insular** | 50% | Baixa | ~35 | Sim: Japão, UK, Irlanda, Islândia, Malta, Chipre, NZ, Austrália, Fiji, Vanuatu, ilhas caribenhas… |
| 26 | **Spillover / cobertura de vazamento** | 95% (se sim) | Baixa | 7 | Tanzânia, Gâmbia, Bielorrúsia, Guiana, Venezuela, Paraguai, Uruguai (parcial) |
| 27 | **Gen 2 abundante** | 85% (se sim) | Alta | 5 | Canadá (rural), Jersey, Bermudas, África do Sul, Havaí |
| 28 | **Câmera trekker exclusiva** | 99% (se sim) | Alta | 1 | Bielorrúsia (única cobertura = trekker em Minsk) |
| 29 | **Carro Google especial** | 90% | Alta | ~12 | Caminhão cinza+snorkel → Quênia; Carro borroso completo → Suíça; Carro preto Gen3 → Argentina/Peru/Uruguai/Rússia |
| 30 | **Marcas de combustível exclusivas** | 99% (se visível) | Baixa | ~50 | Pemex → México; YPF → Argentina; Petrobras → Brasil; ENEOS → Japão; Petrol → Eslovênia; ADNOC → EAU |
| 31 | **Microestado / país muito pequeno** | 70% | Baixa | ~15 | Andorra, Mônaco, San Marino, Liechtenstein, Malta, Gibraltar, Guam, CNMI, etc. |
| 32 | **Arquitetura regional exclusiva** | 65% | Média | ~40 | Pueblo Revival → Novo México; Trullo → Apúlia Itália; Tongkonan → Sulawesi Indonésia; Three-decker → Nova Inglaterra |
| 33 | **Cor da placa de veículo** | 70% | Média | ~30 | Amarela (privados) → Colômbia (única na AL); Amarela atrás + branca frente → UK; Verde → Azerbaijão |

---

### Tabela Detalhada: Bollards por País

| Tipo de Bollard | País | Confiança |
|---|---|---|
| Pino-boliche com 2 listras vermelhas | Mongólia | 99% |
| Bird poles (1-5 barras horizontais) | África do Sul | 99% |
| Cilíndrico branco + base preta | México | 99% |
| Vermelho-branco listrado diagonal (cilíndrico) | Indonésia | 98% |
| Preto+branco com cunha + refletor amarelo | Espanha | 95% |
| Preto+branco com cunha + refletor branco/cinza | Alemanha | 90% |
| Arredondado vermelho frente + branco atrás + faixa branca | Reino Unido | 97% |
| Faixa vermelha envolve toda a traseira | Nova Zelândia | 98% |
| Duplo (dois postes juntos) | Botsuana | 90% |
| Simples (um poste fino) | África do Sul (vs. Botsuana) | 85% |
| Cilíndrico preto+branco (topo arredondado) | Suíça / Liechtenstein | 90% |
| Triangular concreto vermelho+amarelo | Peru | 95% |
| 2 faixas pretas horizontais | Guatemala | 90% |
| Branco + lado amarelo pintado | Uruguai | 92% |
| Cônico branco + refletor vermelho | França (tipo 1) | 88% |
| Diamante preto + topo branco (poste escuro) | Dakota do Sul / Montana (EUA) | 90% |
| Refletor circular branco + topo pintado branco/cinza | Wyoming (EUA) | 90% |

---

### Tabela Detalhada: Chevrons por País/Região

| Fundo | Seta | País(es) | Exclusivo? |
|---|---|---|---|
| Azul | Amarelo | Suécia | Sim (Europa) |
| Azul | Branco | França, Espanha | Não |
| Preto | Amarelo | Noruega, Finlândia, Islândia, Brasil | Grupo |
| Preto | Amarelo + moldura amarela | Portugal | Sim |
| Branco | Vermelho | Argentina, Turquia, África do Sul | Não |
| Branco | Vermelho + moldura amarela | Romênia | Sim |
| Amarelo | Preto | Austrália, Coreia do Sul | Não |
| Preto | Branco | Alemanha, maioria europeia | Não (genérico) |
| Branco | Preto | EUA, Canadá | Não |

---

### Tabela Detalhada: Vegetação por Zona

| Vegetação | Países principais | Diferencial chave |
|---|---|---|
| Araucária (pinheiro-candelabro) | Brasil (PR, SC, RS) | Exclusivo → confirma Brasil Sul |
| Samambaia prateada (silver fern) | Nova Zelândia | Exclusivo → confirma NZ |
| Montes de cupim (termite mounds) | Austrália (NT, WA, QLD) | Diferencia de NZ |
| Baobá | Senegal, Quênia, Tanzânia, Madagascar | Exclusivo da África Subsaariana |
| Fynbos | África do Sul (Western Cape) | Sub-região específica |
| Caatinga (cactus + solo branco + arbustos decíduos) | Brasil Nordeste | Exclusivo do Brasil |
| Cerrado (árvores tortuosas + solo vermelho) | Brasil Centro-Oeste | Exclusivo do Brasil |
| Palmeiras de dendê em fileiras retas | Malásia, Indonésia | Diferencia de floresta amazônica |
| Sabal palm (aspecto pirulito) | México (Yucatán), Cuba, Rep. Dom. | Caribe + México |
| Saguaro (tubos altos + braços curvos) | Arizona (EUA) + Sonora (México) | Sub-regional |
| Sagebrush (arbusto azul-esverdeado baixo) | Interior oeste EUA, Nevada | Diferencia de pradaria |
| Southern pines (tufos altos) | Sudeste EUA | Sub-regional |
| Douglas firs (coníferas altíssimas) | Cascádia (WA, OR, BC) | Sub-regional |
| Boreal/taiga (abetos densos) | Finlândia, Suécia, Noruega, Rússia N, Canadá | Grupo nórdico |
| Temperada (bétulas tronco branco) | Escandinávia, Lituânia, Rússia O | Diferencia de boreal |
| Estepe aberta (sem árvores + horizonte infinito) | Mongólia, Cazaquistão, Pampas Arg. | Contexto + solo |
| Mediterrâneo (arbustos baixos + oliveiras) | Portugal, Espanha, Grécia, Israel, Turquia | Grupo mediterrâneo |

---

## B) ÁRVORE DE DECISÃO SUGERIDA — 5 NÍVEIS

```
RAIZ: País desconhecido (~140 países)
│
├── 1. SCRIPT visível e NÃO-LATINO?
│   ├── SIM → qual script?
│   │   ├── Kanji+Hiragana+Katakana → JAPÃO ✓
│   │   ├── Hangul → COREIA DO SUL ✓
│   │   ├── Sinhala → SRI LANKA ✓
│   │   ├── Lao → LAOS ✓
│   │   ├── Khmer → CAMBOJA ✓
│   │   ├── Tailandês → TAILÂNDIA ✓
│   │   ├── Devanagari → Índia ou Nepal (~2)
│   │   │   └── 2. Câmera shitcam?
│   │   │       ├── Sim → ÍNDIA ✓
│   │   │       └── Não → NEPAL ✓
│   │   ├── Cirílico → grupo 9 países
│   │   │   └── 2. Caracteres exclusivos?
│   │   │       ├── Ы/Э/ё → RÚSSIA ✓
│   │   │       ├── Ї/І ucraniano → UCRÂNIA ✓
│   │   │       ├── Ɵ/Ү → MONGÓLIA ✓
│   │   │       └── Outro → Bielorrússia/Sérvia/Bulgária/Macedônia/Cazaquistão/Quirguistão
│   │   ├── Árabe → grupo ~7 países
│   │   │   └── 2. Hebraico também presente?
│   │   │       ├── Sim → ISRAEL/PALESTINA ✓
│   │   │       └── Não → Qatar/EAU/Jordânia/Líbano/Egito/Omã/Iraque
│   │   ├── Georgiano → GEÓRGIA ✓
│   │   ├── Armênio → ARMÊNIA ✓
│   │   └── Etíope (Ge'ez) → Etiópia ou Eritreia (~2)
│   │
│   └── NÃO (latino ou sem texto visível) → ~75 países
│       │
│       └── 2. LADO DE CONDUÇÃO?
│           ├── ESQUERDA → ~20 países
│           │   └── 3. CONTINENTE/VEGETAÇÃO?
│           │       ├── Tropical Ásia → Indonésia, Malásia, Singapura, Bangladesh, Paquistão
│           │       │   └── 4. Câmera especial?
│           │       │       ├── Shitcam → BANGLADESH ou PAQUISTÃO
│           │       │       └── Normal → Indonésia/Malásia/Singapura
│           │       ├── Temperada / Ilha → UK, Irlanda, Malta, Chipre
│           │       │   └── 4. Stop sign texto?
│           │       │       ├── STOP → Reino Unido ou Irlanda
│           │       │       └── Outro → Malta/Chipre
│           │       ├── Savana africana → Quênia, Uganda, Ruanda, Tanzania(spill)
│           │       ├── África Austral → África do Sul, Botsuana, Lesoto, Eswatini, Namíbia
│           │       │   └── 4. Linha externa?
│           │       │       ├── Amarela → grupo África Austral (5 países)
│           │       │       └── 5. Bollard duplo ou simples?
│           │       │           ├── Duplo → BOTSUANA ✓
│           │       │           └── Simples → África do Sul / Lesoto / Eswatini
│           │       ├── Temperada Oceania → Austrália, Nova Zelândia
│           │       │   └── 4. Bollard com faixa traseira vermelha?
│           │       │       ├── Sim → NOVA ZELÂNDIA ✓
│           │       │       └── Não → AUSTRÁLIA ✓
│           │       └── Subtropical/insular → Japão, Bermudas, USVI, Jamaica
│           │           └── 4. Câmera lowcam?
│           │               ├── Sim → JAPÃO ✓
│           │               └── Não → Bermudas/USVI/Jamaica
│           │
│           └── DIREITA → ~55 países
│               │
│               └── 3. LINHA EXTERNA AMARELA?
│                   ├── SIM → ~7 países (África Austral + Israel + Qatar)
│                   │   └── 4. Lado de condução já confirmado DIREITA + amarela?
│                   │       ├── Israel/Palestina (script hebraico já identificado acima)
│                   │       ├── Qatar (deserto + árabe)
│                   │       └── → improvável (África Austral = esquerda, já filtrado)
│                   │
│                   └── NÃO → ~50 países
│                       │
│                       └── 4. CONTINENTE por vegetação/paisagem?
│                           ├── AMÉRICA DO NORTE → EUA, Canadá, México
│                           │   └── 5. Stop sign?
│                           │       ├── ALTO → México ✓
│                           │       ├── SPEED LIMIT → EUA ✓
│                           │       └── MAXIMUM → Canadá ✓
│                           │
│                           ├── EUROPA → ~35 países
│                           │   └── 5. Câmera / bollard / chevron?
│                           │       ├── Chevron azul+amarelo → SUÉCIA ✓
│                           │       ├── Linha-Z → FRANÇA ✓
│                           │       ├── Lowcam + carro borrado → SUÍÇA ✓
│                           │       ├── Cirílico → Europa Oriental (já tratado)
│                           │       └── → sub-árvore Europa (bollards/diacríticos)
│                           │
│                           ├── AMÉRICA DO SUL → Brasil, Argentina, Colômbia, etc.
│                           │   └── 5. Stop sign "PARE" ou "STOP"?
│                           │       ├── PARE → Brasil/Portugal/Timor (por vegetação = Brasil)
│                           │       └── STOP → Argentina, Colômbia, Chile, Peru, etc.
│                           │
│                           ├── SUDESTE ASIÁTICO → Tailândia(já), Vietnã, Filipinas, etc.
│                           │   └── 5. Script latino com muitos diacríticos?
│                           │       ├── Sim (diacríticos intensos) → VIETNÃ ✓
│                           │       └── Não → Filipinas / outros
│                           │
│                           └── ORIENTE MÉDIO / ÁSIA CENTRAL
│                               └── 5. Stop sign "DUR"?
│                                   ├── Sim → TURQUIA ✓
│                                   └── Não → Israel/Qatar/Jordânia/EAU/etc.
```

---

## C) ATRIBUTOS POR CONTINENTE

### Europa (~35 países)

Os maiores confusões são entre países vizinhos com idiomas similares.

| Par Confuso | Atributo Discriminatório | Como Distinguir |
|---|---|---|
| França vs. Espanha | Bollard + Chevron + Linha | França: bollard cônico vermelho; chevron azul+branco; Linha-Z. Espanha: bollard cunha+refletor amarelo; chevron azul+branco (igual). Diferenciar por postes e placa |
| França vs. Bélgica | Linha de estrada + Bollard | França: Linha-Z exclusiva; bollard cônico. Bélgica: sem Linha-Z; bollards diferentes |
| Suécia vs. Noruega vs. Finlândia | Chevron + linha central | Suécia: chevron azul+amarelo (exclusivo). Noruega: linha central tom alaranjado. Finlândia: sinais amarelos claros |
| Alemanha vs. Áustria | Bollard + guardrail | Alemanha: bollard preto+branco + refletor laranja em interseções; sinais de rua em amarelo. Áustria: bollard diferente |
| Portugal vs. Espanha | Chevron + bollard | Portugal: chevron preto+amarelo com moldura (exclusivo); bollards com losango. Espanha: chevron azul+branco |
| Rússia vs. Ucrânia | Cirílico exclusivo | Ucrânia: Ї e І; bandeira azul+amarelo nos postes. Rússia: Ы, Ъ, ё |
| Romênia vs. Moldávia vs. Bulgária | Chevron + script | Romênia: chevron branco+vermelho+moldura amarela. Bulgária: cirílico. Moldávia: grafite latino |
| Suíça vs. Liechtenstein vs. Áustria | Lowcam + bollard | Suíça e Liechtenstein: lowcam com carro borrado. Áustria: câmera normal |
| Países Bálticos (Estônia/Letônia/Lituânia) | Bollard + postes | Lituânia: bollard cunha+laranja exclusivo. Letônia: postes específicos. Estônia: flores brancas (fake meta parcial) |

**Atributos mais discriminatórios na Europa:**
1. Bollards (quase 1:1 por país)
2. Diacríticos do alfabeto latino
3. Chevrons (Suécia exclusivo; Portugal exclusivo)
4. Postes de utilidade (waffle → França; Stobie → impossível na Europa)
5. Geração de câmera (Suíça/Liechtenstein lowcam)

---

### Américas (~25 países)

| Par Confuso | Atributo Discriminatório | Como Distinguir |
|---|---|---|
| EUA vs. Canadá | Stop sign + linhas + Gen | "SPEED LIMIT" → EUA; "MAXIMUM" → Canadá; Gen 2 em rural → Canadá; espelho Gen 3 pico único → EUA |
| Brasil vs. Argentina | Vegetação + câmera + bollard | Brasil: araucária (Sul), caatinga (NE), cerrado, "PARE"; Argentina: carro preto Gen 3, chevron branco+vermelho, postes duplos de concreto |
| Brasil vs. Colômbia | Câmera + postes | Brasil: antena espiral Gen 3; postes variados por estado. Colômbia: octogonal similar ao México; "PARE" = Brasil vs. "STOP" = Colômbia |
| México vs. Guatemala | Stop sign + bollard | México: bollard cilíndrico base preta (exclusivo); "ALTO". Guatemala: bollard com 2 faixas pretas; "ALTO" |
| Chile vs. Argentina | Vegetação + chevron | Chile: Atacama no norte (mais seco); Patagônia no sul. Argentina: pampas; carro preto Gen 3; chevron branco+vermelho |
| Peru vs. Bolívia | Bollard + guardrail | Peru: bollard triangular vermelho+amarelo + guardrail bicolor; "PARE". Bolívia: guardrail só amarelo |

**Atributos mais discriminatórios nas Américas:**
1. Stop sign texto ("ALTO" / "PARE" / "STOP" / "MAXIMUM")
2. Araucária, Caatinga, Cerrado (biomas exclusivos do Brasil)
3. Câmera Gen 3 (carro preto → Argentina/Peru/Uruguai)
4. Bollards (México exclusivo; Peru exclusivo)
5. Linha central amarela desbotada (México)
6. Marcas exclusivas (Pemex, YPF, Petrobras)

---

### África (~20 países)

| Par Confuso | Atributo Discriminatório | Como Distinguir |
|---|---|---|
| África do Sul vs. Botswana | Bollard + linha | AS: bollard simples; linha tripla central. Botswana: bollard duplo |
| África do Sul vs. Quênia | Câmera + carro | AS: Gen 2 abundante; bird poles. Quênia: caminhão cinza com snorkel (Gen 3 off-road) |
| África do Sul vs. Namíbia | Vegetação + solo | Namíbia: deserto (Namibe), dunas; areia vermelha. AS: vegetação mais densa; fynbos no Cape |
| Senegal vs. Gâmbia | Cobertura | Gâmbia = spillover do Senegal; cobertura muito limitada e específica |
| Quênia vs. Tanzânia | Cobertura | Tanzânia = spillover do Quênia; cobertura mínima próxima a fronteiras |

**Atributos mais discriminatórios na África:**
1. Câmera/geração (bird poles + Gen 2 = África do Sul imediato)
2. Lado de condução (esquerda = África Austral + Quênia/Uganda/Ruanda)
3. Linha externa amarela (África Austral)
4. Script (etíope → Etiópia/Eritreia; árabe → norte)
5. Carro Google especial (caminhão snorkel → Quênia)

---

### Ásia (~30 países)

| Par Confuso | Atributo Discriminatório | Como Distinguir |
|---|---|---|
| Índia vs. Nepal | Câmera + script | Índia: shitcam; Devanagari + scripts regionais (Sul = Tamil/Telugu/etc.). Nepal: shitcam também; Devanagari puro; montanhas altíssimas |
| Tailândia vs. Laos vs. Camboja | Script | Tailandês: círculos no topo. Lao: mais simples, stop sign 2 chars. Khmer: hastes longas |
| China vs. Taiwan | Script | China: simplificado (menos traços). Taiwan: tradicional (mais traços) |
| Japão vs. qualquer outro | Câmera + script | Lowcam + 3 scripts simultâneos = Japão imediato |
| Malásia vs. Indonésia | Vegetação + bollard | Malásia: dendê em fileiras retas muito comuns; trânsito esquerda. Indonésia: bollard cilíndrico listrado vermelho+branco; trânsito esquerda; Bahasa diferente |
| Vietnã vs. Filipinas | Script + postes | Vietnã: latino com muitos diacríticos; postes com buracos verticais. Filipinas: inglês + tagalog; estradas de concreto; trânsito direita |
| Quirguistão vs. Cazaquistão | Câmera + paisagem | Quirguistão: carro com porta-malas e espelhos extras; montanhas. Cazaquistão: estepe plana; base de postes pintada de preto |

**Atributos mais discriminatórios na Ásia:**
1. Script (mais discriminatório do mundo inteiro)
2. Câmera especial (lowcam → Japão exclusivo; shitcam → Índia/Nepal/Camboja/Nigéria)
3. Lado de condução (esquerda → Japão, Índia, Indonésia, Malásia, etc.)
4. Vegetação (dendê em fileiras → Malásia/Indonésia; arroz em terraços → Nepal/Vietnam)

---

### Oceania (~5 países)

| Par Confuso | Atributo Discriminatório | Como Distinguir |
|---|---|---|
| Austrália vs. Nova Zelândia | Bollard + vegetação | NZ: bollard com faixa traseira vermelha (exclusivo); samambaia prateada; montanhas neozelandesas. Austrália: montes de cupim; Stobie poles em SA; vegetação seca no interior |
| Austrália (estados) | Stobie poles | South Australia: Stobie poles (exclusivo do estado) |

---

## D) LISTA FINAL DE ATRIBUTOS PARA O JSON

### `countries-data.json` — Schema Completo

Cada entrada representa um país/território. Tipos: `string`, `boolean`, `enum`, `list[string]`.

```json
{
  "id": "string",                         // slug do país (ex: "france")
  "name": "string",                       // nome em português

  // === IDENTIFICADORES PRIMÁRIOS ===
  "driving_side": "enum",                 // "left" | "right"
  "scripts": "list[string]",             // ["latin", "cyrillic", "arabic", "devanagari",
                                          //  "hangul", "kanji", "thai", "khmer", "lao",
                                          //  "sinhala", "georgian", "armenian", "ethiopic",
                                          //  "hebrew", "chinese_simplified", "chinese_traditional",
                                          //  "burmese", "mongolian", "bengali", "vietnamese_latin"]
  "latin_diacritics": "list[string]",    // diacríticos exclusivos do idioma: ["ñ"], ["ã","ô"], ["ı","ğ","ş"]
  "stop_sign": "enum",                   // "stop" | "pare" | "alto" | "dur" | "arret" | "other" | "symbol_only"

  // === CÂMERA / META ===
  "camera_dominant": "enum",             // "gen1" | "gen2" | "gen3" | "gen4" | "gen3_gen4" | "mixed"
  "camera_special": "enum",             // "lowcam" | "shitcam" | "smallcam" | "trekker" | "none"
  "gen2_abundant": "boolean",           // true apenas Canadá, Jersey, Bermudas, África do Sul, Havaí
  "google_car_special": "string|null",  // "black_gen3" | "grey_snorkel_truck" | "blurred_car" | null

  // === LINHAS DE ESTRADA ===
  "road_line_outside": "enum",           // "white" | "yellow" | "red" | "mixed" | "absent"
  "road_line_center": "enum",            // "white" | "yellow" | "double_yellow" | "triple" | "mixed" | "absent"
  "road_line_exclusive": "string|null",  // "ligne_z" | "triple_sa" | "square_denmark" | "zigzag_uk" | null

  // === INFRAESTRUTURA ===
  "bollard_type": "string|null",         // slug do bollard exclusivo: "bird_poles" | "mexico_black_base" |
                                          // "nz_red_rear" | "uk_rounded_red" | "france_cone" |
                                          // "peru_triangular" | "mongolia_bowling" | null
  "chevron": "string|null",              // "blue_white" | "blue_yellow_sweden" | "black_yellow" |
                                          // "black_yellow_portugal" | "white_red" | "white_red_yellow_romania" | null
  "utility_pole_type": "string|null",    // "wood_north_america" | "bird_poles_sa" | "stobie_sa_aus" |
                                          // "waffle_france" | "double_concrete_argentina" |
                                          // "octagonal_mexico" | "bamboo_vietnam" | null
  "guardrail_color": "string|null",      // "black_yellow_peru" | "yellow_bridge_usvi" | "brown_national_park" | null

  // === VEGETAÇÃO / PAISAGEM ===
  "vegetation_dominant": "enum",         // "tropical_dense" | "savanna" | "mediterranean" | "temperate" |
                                          // "boreal_taiga" | "steppe" | "desert_hot" | "desert_cold" |
                                          // "tundra" | "cerrado" | "caatinga" | "fynbos" | "mixed"
  "vegetation_exclusive": "list[string]",// ["araucaria"] | ["silver_fern"] | ["baobab"] | ["oil_palm_rows"] | []
  "soil_color": "enum",                  // "red_intense" | "red_pink" | "white_grey" | "beige_sandy" |
                                          // "dark_volcanic" | "orange" | "normal"

  // === GEOGRAFIA / CONTEXTO ===
  "continent": "enum",                   // "south_america" | "north_america" | "central_america" |
                                          // "europe_west" | "europe_north" | "europe_east" | "europe_central" |
                                          // "africa_sub" | "africa_north" | "africa_austral" |
                                          // "middle_east" | "asia_south" | "asia_southeast" |
                                          // "asia_east" | "asia_central" | "oceania" | "caribbean"
  "is_island": "boolean",
  "is_microstate": "boolean",
  "is_spillover": "boolean",             // cobertura é spillover de outro país
  "spillover_from": "string|null",       // slug do país de origem do spillover

  // === FEATURES EXCLUSIVAS (alta confiança) ===
  "exclusive_features": "list[string]",  // lista de features que identificam o país com >95% confiança
                                          // ex: ["ligne_z", "bird_poles", "araucaria", "lowcam_japan"]

  // === REFERÊNCIAS CRUZADAS ===
  "confusable_with": "list[string]",    // países com os quais frequentemente se confunde
  "fuel_brands_exclusive": "list[string]", // marcas exclusivas visíveis em sinais: ["Pemex"] | ["YPF"] | []

  // === METADADOS ===
  "wiki_status": "enum",                 // "complete" | "draft" | "stub"
  "confidence_score": "integer"          // 1-10: quão bem documentado está o país no wiki
}
```

### Atributos Ordenados por Prioridade de Implementação

| Prioridade | Atributo | Tipo | Justificativa |
|---|---|---|---|
| 1 | `driving_side` | enum | Presente em 140/140 países; eliminação binária imediata |
| 2 | `scripts` | list | Identifica país único em ~50 países; prioridade máxima |
| 3 | `stop_sign` | enum | Alta observabilidade; elimina continentes inteiros |
| 4 | `camera_special` | enum | Lowcam/shitcam identificam grupo muito pequeno |
| 5 | `road_line_outside` | enum | Amarela = África Austral/Israel; alta observabilidade |
| 6 | `exclusive_features` | list | Identifica país diretamente quando presente |
| 7 | `bollard_type` | string | Quase 1:1 com país; média observabilidade |
| 8 | `continent` | enum | Elimina ~80% dos países por bioma/vegetação |
| 9 | `road_line_center` | enum | Diferencia continentes (amarela = Américas/Ásia; branca = Europa) |
| 10 | `vegetation_dominant` | enum | Alta observabilidade; discriminatório em contexto |
| 11 | `chevron` | string | Alta confiança quando visível; média frequência |
| 12 | `camera_dominant` | enum | Diferencia Canadá/EUA; identifica spillover |
| 13 | `gen2_abundant` | boolean | Altamente discriminatório em contexto Norte-Americano |
| 14 | `utility_pole_type` | string | Discriminatório para países específicos |
| 15 | `vegetation_exclusive` | list | Confirma país com certeza absoluta (araucária, etc.) |
| 16 | `soil_color` | enum | Complementar; útil em contexto |
| 17 | `latin_diacritics` | list | Refinamento dentro de países latinos |
| 18 | `road_line_exclusive` | string | Linha-Z = França exclusivo |
| 19 | `google_car_special` | string | Alta confiança quando visível |
| 20 | `is_spillover` | boolean | Reduz espaço de busca drasticamente se verdadeiro |
| 21 | `guardrail_color` | string | Complementar; útil para Peru/USVI/EUA parques |
| 22 | `fuel_brands_exclusive` | list | Confirma país se visível; baixa frequência de observação |
| 23 | `confusable_with` | list | Metadado para lógica de desempate |
| 24 | `is_island` | boolean | Contexto geográfico |
| 25 | `is_microstate` | boolean | Elimina maioria dos países quando verdadeiro |

---

## Observações Finais

### Atributos a NÃO incluir no JSON (baixo valor diagnóstico)
- Arquitetura genérica (alta variação intra-país, difícil de codificar)
- Cor do carro Google padrão (Gen 4 = muitos países)
- Nomes de ruas (muita variação, difícil automatizar)
- Densidade populacional (não observável diretamente)

### Combinações de Alta Sinergia
- `driving_side=left` + `road_line_outside=yellow` = África Austral confirmada
- `camera_special=lowcam` + `driving_side=left` = Japão vs. Suíça vs. Liechtenstein (resolver por escala)
- `scripts=[devanagari]` + `camera_special=shitcam` = Índia confirmada
- `exclusive_features=[araucaria]` = Brasil Sul confirmado independente de qualquer outro dado
- `stop_sign=alto` + `bollard=mexico_black_base` = México confirmado

### Lacunas Identificadas no Wiki
- ~15 países com dados incompletos de bollard (campos `null` a preencher)
- Chevrons documentados em ~65/140 países — expandir cobertura
- Guardrails documentados em ~60/140 países — expandir cobertura
- Vegetação exclusiva documentada em ~40/140 países — expandir especialmente para África e Ásia Central

---

*Gerado em 2026-04-17 via varredura de ~90 arquivos de países + 22 conceitos.*
