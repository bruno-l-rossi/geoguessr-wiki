---
title: "Guia do Iniciante — GeoGuessr"
date_created: 2026-04-10
date_modified: 2026-04-17
sources: [plonkit.net, somerandomstuff1.wordpress.com]
summary: "Referência compilada do guia oficial do Plonk It para iniciantes: mecânicas do jogo, modos de jogo, tipos de pistas (sol, lado de condução, idioma, arquitetura, vegetação, infraestrutura, meta de câmera), e glossário completo de termos da comunidade."
tags: [conceito, guia, iniciante, mecânicas, glossário]
type: concept
status: draft
---

# Guia do Iniciante — GeoGuessr

Síntese do [Plonk It Beginner's Guide](https://www.plonkit.net/beginners-guide). Referência rápida para mecânicas, tipos de pistas e termos da comunidade.

---

## 1. Mecânicas do Jogo

### Movimentação
- **W/S** — avançar/recuar; **A/D** ou setas — girar câmera
- **R** — voltar ao início do round (importante: você guessa a localização inicial, não onde você está)
- **C** — criar/retornar a um checkpoint
- **Z** — desfazer último movimento
- **Fast move**: pressionar seta direcional + segurar **Enter** (ou Space antes de colocar pino)

### Bússola
- Bússola clássica: seta vermelha = norte, branca = sul
- Recomendado: usar as duas bússolas simultaneamente (clássica + nova)
- Técnica de alinhamento de estrada: olhar para baixo apontando para norte (tecla **N** duas vezes) — a estrada na tela fica paralela à estrada no mapa

### Pontuação
- Sistema não-linear: a mesma distância perde **mais pontos** quanto mais perto da localização você estiver
- Acerto perfeito (5k): raio de ≤25m em qualquer mapa; até ~140-200m em mapas mundiais
- Mapas de países têm scoring muito mais rigoroso que mapas mundiais

### Tipos de Mapa
- **Pinpointável**: cada localização está em um ponto específico (interseção, ponte, curva) — todo round tem solução perfeita
- **Não-pinpointável**: localizações em trechos longos de estrada — nem sempre é possível acertar 5k
- **Handpicked**: localizações selecionadas manualmente
- **Geradas arbitrariamente**: localizações escolhidas por algoritmo (não IA)
- Recomendado: jogar mapas pinpointáveis handpicked de qualidade (evitar mapa oficial "World")

---

## 2. Modos de Jogo

### Single Player
| Modo | Características |
|---|---|
| **Moving** | Objetivo: 5k em todo round; jogar em mapas pinpointáveis |
| **No Move** | Mais comum para streaks; pistas de reconhecimento de país mais importantes |
| **NMPZ** (No Moving, Panning or Zooming) | Uma única imagem; mapas competitivos evitam pistas de carro |

### Modos por Objetivo
| Objetivo | Descrição |
|---|---|
| **Country streak** | Adivinhar o país correto o máximo de vezes seguidas; manter com script da comunidade |
| **Region/Subdivision streak** | Adivinhar a subdivisão certa em países grandes |
| **Hedge streak** | Quantas vezes consecutivas acima de 20.000 pontos |
| **25k speedrun** | Tempo até conseguir placar perfeito em mapa específico |
| **Highscore** | Maior pontuação possível em No Move ou NMPZ |

### Competitivo (Duels)
- Dois jogadores, 6.000 pontos de vida cada; diferença de score = dano aplicado ao perdedor de cada round
- **Multiplicador**: começa em 1; aumenta 0,5 por cada round com guess melhor que o adversário
- Divisões: Bronze/Silver/Gold = Moving; Gold+ = No Move; Master/Champion = NMPZ

---

## 3. Câmeras e Cobertura (Meta)

### Gerações de Câmera
Ver [[gerações-de-câmera]] para guia completo. Resumo:

| Geração | Identificação Visual |
|---|---|
| **Gen 1** | Resolução muito baixa; raramente em mapas competitivos |
| **Gen 2** | Borrão circular largo embaixo + halo de cor no céu; resolução média |
| **Gen 3** | Boa resolução; cores dessaturadas; céu acinzentado mesmo em dias de sol |
| **Gen 4** | Melhor qualidade; cores vibrantes, levemente supersaturadas |

### Shitcam
Câmera de baixo custo usada pelo Google em poucos países. Identificação: **baixa resolução + borrão circular largo** cobrindo o carro (parecido com Gen 2, mas com distinções).

**Países principais:**
- **[[india]]** — câmera primária do país; quase toda a cobertura
- **[[nigeria]]**, **[[cambodia]]**, **[[lebanon]]**, **[[ecuador]]** — cobertura comum com shitcam
- Europa (verão 2025): Google lançou cobertura shitcam em toda a Europa, mas raramente usada em mapas competitivos

### Lowcam
Câmera montada mais baixa por exigências de privacidade. Identificação: itens ao redor aparecem **mais altos** que o normal, borrão do carro é **maior**. Não confundir com Gen 2 (que tem halo no céu).

**Países com lowcam exclusivo:**
- **[[japan]]** — lowcam em toda a cobertura
- **[[switzerland]]** — lowcam em toda a cobertura (carro borrrado)
- **[[liechtenstein]]** — lowcam em toda a cobertura

**Lowcam parcial:**
- **[[sri-lanka]]** — apenas cobertura Gen 4

### Smallcam
Câmera mais nova (lançada fim de 2024). Identificação: borrão circular com **pequena protuberância na frente** (formato de joaninha/cantil). Qualidade igual a Gen 4; montada **mais baixo** que Gen 4 padrão.

- Em alguns países parte do carro é visível: antena em [[south-africa]], parte frontal em [[hawaii]]

### Cobertura Não-Oficial
- **Cobertura de veículo privado ("Ari")**: carro completamente visível (sem blur); qualidade variável; linhas azuis no mapa
- **Photospheres**: imagens 360° individuais de usuários; pontos azuis no mapa
- Competitivo: **apenas cobertura oficial**

### Carros do Google (Meta)
Partes do carro são visíveis em Gen 3 e Gen 4. Útil em países com cobertura limitada:

| País/Região | Carro Característico |
|---|---|
| **[[kenya]]** | Pickup cinza com snorkel — Gen 4 |
| **[[kyrgyzstan]]** | Carro com porta-malas e espelhos retrovisores visíveis |
| **[[russia]]** | Carro preto com antena longa |
| **[[argentina]]** | Carro preto com traseira visível — Gen 3 (também no [[uruguay]] e [[peru]]) |

### Cobertura Sazonal
Alguns países têm toda/maioria da cobertura de uma única estação — dá ao país uma aparência específica:
- **[[kyrgyzstan]]** — cobertura outubro-dezembro: outono/inverno em todo o país
- **[[andorra]]** — maioria da cobertura no outono

---

## 4. Tipos de Pistas

### Pistas Gerais

**Sol:** ao sul = Hemisfério Norte; ao norte = Hemisfério Sul. Confiável apenas quando o sol está mais próximo de N/S do que de L/O. Atenção: entre os Trópicos o sol pode aparecer do lado "errado" no verão.

**Antenas parabólicas:** apontam em direção ao equador (satélites geoestacionários ficam sobre o equador). Perto do equador, a antena aponta quase verticalmente; em latitudes maiores, aponta num ângulo mais pronunciado em direção ao horizonte equatorial. Útil para estimar latitude quando outros elementos são inconclusivos.

**Lado de condução:** elimina rapidamente metade dos países. Quando não há carros visíveis: sinais ficam no lado dos carros; antena do Google aparece na traseira; rastro de poeira em estradas de terra; volante fica no lado mais próximo do centro da pista.

**Idioma e escrita:** scripts únicos identificam país ou região imediatamente (japonês, árabe, hangul, devanagari, etc.). Caracteres especiais no alfabeto latino diferenciam países de língua aparentemente similar.

**Bandeiras e domínios:** úteis mas não devem ser a busca principal — inibem aprendizado de outras pistas.

### Infraestrutura

**Bollards:** marcadores de beira de estrada com designs exclusivos por país. Detalhe crítico: **forma e cor dos refletores** diferenciam países com bollards superficialmente similares (ex: Espanha e Alemanha — ambos branco/cunha, mas Espanha tem refletor frontal amarelo).

**Linhas de estrada:**
- Linha externa amarela = África austral, Oriente Médio
- Dupla linha amarela central = Américas
- Linhas longas externas em N. Europa = Noruega
- Zigzag urbano = Reino Unido
- Linha tripla exclusiva = África do Sul, países vizinhos

**Postes (utility poles):** material, forma, topo e marcações variam por país e estado/província. Especialmente úteis em:
- **França**: poste escada/waffle; topo em losango/flecha; "poletop francês" (losango com 3 fios abaixo)
- **Argentina**: poste duplo de concreto
- **Grécia**: poste de madeira com armação metálica com 5 fios
- **Romênia**: poste de concreto com 5 furos longos e finos
- **Japão**: transformadores distintos por região (ver [[japan]])
- **África do Sul**: "bird poles" — 1-5 barras horizontais com isoladores brancos (ver [[south-africa]])

**Sinais de trânsito:** stop signs com palavras diferentes (STOP/PARE/ALTO/DUR/mão desenhada). Bordas de sinal, fontes e espessura de borda vermelha variam por país.

**Sinais de rua:**
- Ankara (Turquia): fundo azul com topo em arco
- Bucharest (Romênia): similar mas borda verde característica
- Cingapura: fundo verde com texto branco
- Budapest (Hungria): retangular branco, texto serif

**Placas de veículo:** cor, presença/ausência de placa dianteira, marcações coloridas (ex: Colômbia = única na América Latina com placas amarelas em veículos privados).

### Vegetação
- Pinheiros bálticos: Europa do Norte e Central
- Opuntia (figueira-da-índia): zonas áridas mediterrâneas
- Palmeiras açaí: Pará, Brasil (e toda a bacia amazônica)
- Identificar espécies específicas é um dos skills mais avançados do jogo

### Arquitetura
- Roofs: ardósia = Bretanha; telha laranja/vermelha com ganchos = Chugoku/Japão; preto = Sul do Japão
- Elementos únicos: Trullo (cone de pedra) = Apúlia, Itália; Tongkonan (telhado de barco em palafitas) = Sulawesi Sul, Indonésia; Hórreos (celeiros em pilares) = Astúrias, Espanha; chaminés decoradas = Dalarna, Suécia

### Geologia
- Solo muito vermelho = Brasil
- Solo escuro = áreas vulcânicas (Islândia, Vanuatu)
- Solo arenoso e claro = Yucatán, México
- Solo russo: players dizem ter aparência única

---

## 5. Estratégias por Região

| Região | Pistas Mais Eficazes |
|---|---|
| **Europa** | Bollards, postes, idioma, arquitetura — dezenas de pistas por país |
| **Américas** | Paisagem/bioma, postes, sinais de trânsito (cada país tem design distinto); carros/câmera ajudam mas não são necessários |
| **Ásia** | Varia muito por país; zonas rurais do Sudeste Asiático são difíceis até para experts |
| **África** | Meta de carro + geração de câmera + paisagem básica é suficiente na maioria dos casos |
| **Oceania** | Austrália e Nova Zelândia são os únicos com cobertura de carro; algumas pistas de infraestrutura distinguem bem as duas |
| **Ilhas pequenas / territórios** | Trekker meta ou carro meta → memorizar cada trekker individualmente |

---

## 6. Glossário da Comunidade

| Termo | Definição |
|---|---|
| **5k** | Placar perfeito (5.000 pontos). Usado informalmente para qualquer guess muito próximo |
| **AI Generated** | Mapa com localizações escolhidas por algoritmo (não é IA de verdade) |
| **Ari** | Cobertura não-oficial (de empresas privadas). De "Autori", empresa que cobriu a Finlândia extensivamente |
| **Handpicked** | Mapa com localizações selecionadas manualmente pelo criador |
| **Hedge** | Guess no centro da área provável, minimizando pontos perdidos em vez de maximizar. "Water hedge" = guess no mar entre opções plausíveis |
| **Loc** | Localização (abreviação de "location") |
| **Lowcam** | Câmera montada mais baixo que o padrão por questões de privacidade (Japão, Suíça, Liechtenstein; Sri Lanka em Gen 4) |
| **Meta** | Qualquer tipo de pista usada no GeoGuessr — desde geração de câmera até postes e bollards |
| **Pano / Panorama** | Uma posição específica no Street View. Cada clique para frente é um novo pano |
| **Pinpointável** | Mapa onde cada localização tem solução perfeita possível |
| **Plonk** | Guess feito sem muito pensamento sobre a localização exata |
| **Rift** | Falha de costura no Street View, visível no céu em alguns países específicos |
| **Shitcam** | Câmera de baixo custo usada pelo Google em alguns países (Índia principalmente); baixa resolução + borrão circular largo |
| **Smallcam** | Câmera lançada em 2024; borrão com protuberância frontal (formato joaninha/cantil); qualidade igual a Gen 4 |
| **Spill / Spillover** | Cobertura que "vazou" para um país sem cobertura oficial quando o carro Google cruzou a fronteira. Ver [[spillover-countries]] |
| **Trekker** | Câmera carregada em mochila ou montada em veículo especial (barco, zebu, camelo) para lugares sem acesso de carro |
| **Tripod** | Cobertura com câmera comercial em tripé — geralmente dentro de edifícios (museus, etc.) |

---

## 7. Recursos Externos

| Recurso | Link | Uso |
|---|---|---|
| **Map Making App** | map-making.app | Checar cobertura; remover linhas de cobertura não-oficial |
| **Geoguessr Training Script** | miraclewhips.dev | Toggle terrain map e linhas de cobertura in-game |
| **geo.emily** | geo.emily.bz | Quizzes de scripts, códigos telefônicos, subdivisões; histórico de coberturas |
| **GeoHints** | geohints.com | Catálogo de pistas de infraestrutura por país (nível intermediário/avançado) |
| **Regionguessing Meta Library** | docs.google.com/spreadsheets | Todos os guias em inglês por país, com descrições |
| **Plonk It Maps Directory** | plonkit.net/maps | Melhores mapas recomendados por categoria |

---

## 8. Fake Metas (Pistas Falsas)

**Fake metas** são pistas incorretas que se espalharam na comunidade.

- **Flores brancas da Estônia**: visíveis em toda a região báltica, apenas um pouco mais comuns na Estônia (Gen 3). Pode ser usado como desempate, não como confirmação.
- Poletops em países específicos podem aparecer fora da região esperada — não significa que a pista é falsa, só que não é 100%.
- Pistas completamente incorretas são raras mas existem; geralmente corrigidas rapidamente na comunidade.

Conceito relacionado: [[gerações-de-câmera]] | [[trafego-esquerda]] | [[bollards-europa]] | [[spillover-countries]]
