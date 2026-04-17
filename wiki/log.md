---
title: "GeoGuessr Wiki — Log de Operações"
---

# Log de Operações

---

## 2026-04-17 — MANUTENÇÃO: campo sources adicionado a todos os conceitos

**Operação:** Manutenção de frontmatter (20 arquivos)  
**Escopo:** Todos os arquivos em `wiki/concepts/` sem campo `sources`

**Fontes inferidas por arquivo:**

| Arquivo | Sources adicionadas |
|---|---|
| `bollards.md` | plonkit.net, geohints.com, geodummy.com |
| `guardrails.md` | plonkit.net, geohints.com, geodummy.com |
| `utility-poles.md` | plonkit.net, geohints.com, geodummy.com |
| `chevrons.md` | plonkit.net, geohints.com, geodummy.com |
| `camera-generations.md` | plonkit.net, geodummy.com |
| `spillover-countries.md` | plonkit.net, geodummy.com |
| `caatinga.md` | plonkit.net, geodummy.com |
| `postes-brasil.md` | plonkit.net, geodummy.com |
| `alphabet-scripts.md` | plonkit.net, geodummy.com |
| `cerrado.md` | plonkit.net, geodummy.com |
| `araucária.md` | plonkit.net, geodummy.com |
| `amazônia.md` | plonkit.net, geodummy.com |
| `gerações-de-câmera.md` | plonkit.net, geodummy.com |
| `palmeiras-brasil.md` | plonkit.net, geodummy.com |
| `bollards-europa.md` | plonkit.net, geodummy.com |
| `architecture-styles.md` | plonkit.net, geodummy.com, somerandomstuff1.wordpress.com |
| `vegetation-zones.md` | plonkit.net, geodummy.com, somerandomstuff1.wordpress.com |
| `driving-side.md` | plonkit.net, geodummy.com, somerandomstuff1.wordpress.com |
| `camera-altura.md` | plonkit.net |
| `trafego-esquerda.md` | plonkit.net |

**Resultado:** Todos os 22 arquivos de conceito agora possuem campo `sources` no frontmatter. Campo pendente do LINT de 2026-04-17 resolvido.

---

## 2026-04-17 — INGEST: united-states.md — seção Regiões Distintas completa

**Operação:** INGEST (expansão de conteúdo existente)  
**Fonte:** `raw/countries/United States of America.md` (plonkit.net/united-states)  
**Arquivo atualizado:** `wiki/countries/united-states.md`

**Conteúdo adicionado:** Seção `## 9. Regiões Distintas` completamente reescrita com clues específicos por região e estado:
- Nova Inglaterra: paredes de pedra, shingle walls, three-deckers, brownstones, sinais de ponte
- Meio Atlântico / Apalachias: WV fração-em-círculo, NC setas em sinais, SC sinais pretos, PA/NH sinais de rota, Pittsburgh pontes amarelas
- Sul (Deep South): southern pines, solo vermelho, Spanish moss, shotgun houses, pilotis costeiros, telhados de metal vermelho, gramado bege no inverno
- Texas: asfalto granulado, bandas amarelas/vermelhas nos postes, Hill Country, Rio Grande Valley, H-E-B, Whataburger, Buc-ee's
- Meio-Oeste: corn belt, canola no Dakota, Iowa concreto, Wisconsin/Michigan pistas específicas, Minnesota triângulos amarelos, lettering system WI/MO
- Grandes Planícies: Nebraska Sandhills, Kansas refletores brancos, Oklahoma números verdes no verso de STOP
- Sudoeste / Quatro Cantos: mesas vermelhas, Pueblo Revival NM, Saguaro cactus AZ, Utah/Idaho ruas numéricas, I-19 em km
- Grande Bacia / Rochosas: sagebrush, bollards por estado (NV, SD/MT, WY, WA)
- Costa do Pacífico: Douglas firs, rainforests, Oregon "Speed" apenas, California listras amarelas em postes + faixa preta nas linhas + Central Valley
- Tabela de territórios não-contíguos (Alaska, Hawaii, Puerto Rico, Guam, USVI)

---

## 2026-04-17 — LINT: verificação completa de qualidade

**Operação:** LINT (auditoria de qualidade completa)  
**Escopo:** 136 arquivos em `wiki/countries/`, 22 em `wiki/concepts/`, `wiki/index.md`  
**Relatório:** `wiki/outputs/lint-report-2026-04-17.md`

**Problemas encontrados:** 2 (ambos corrigidos automaticamente)

**Corrigido automaticamente:**
- `canada.md` — adicionada seção `## 4. Vegetação e Paisagem` (biomas: boreal, pradarias, BC, Ontario/Québec, PEI solo vermelho, ártico); seções subsequentes renumeradas
- `united-states.md` — seção 5 (Vegetação) limpa e focada; adicionada seção `## 6. Arquitetura e Infraestrutura` dedicada; seções subsequentes renumeradas

**Resultado das verificações:**
- Frontmatter países: OK (todos 136 com campos obrigatórios + sources)
- Wikilinks quebrados: nenhum ativo encontrado (falsos positivos do lint-report-2026-04-10 verificados e descartados)
- Páginas órfãs: nenhuma
- Contradições: nenhuma
- Índice: OK
- Nomes de arquivo: OK
- Conceitos sem sources: 20 arquivos — baixa prioridade (CLAUDE.md não exige)

**Atenção manual identificada:**
- Seção de regiões em `united-states.md` marcada como `*(Muito vasto — ver raw)*` — conteúdo pendente de expansão
- 20 arquivos de conceito sem campo `sources`

---

## 2026-04-17 — INGEST: somerandomstuff1.wordpress.com — guia geral 2019

**Operação:** INGEST (fonte externa: guia geral de técnicas GeoGuessr)  
**Fonte:** https://somerandomstuff1.wordpress.com/2019/02/08/geoguessr-the-top-tips-tricks-and-techniques/  
**Resultado:** Conteúdo amplamente já coberto pelo wiki em maior detalhe. Apenas 2 itens genuinamente novos identificados.

**Conteúdo incorporado:**
- `concepts/guia-iniciante.md` — **Antenas parabólicas como indicador de latitude**: apontam em direção ao equador; ângulo mais vertical = perto do equador; ângulo mais horizontal = latitude alta. Adicionado à seção "Tipos de Pistas → Sol"
- `countries/mexico.md` — **Linhas amarelas desbotadas**: linhas centrais do México tendem a ser mais apagadas que nos EUA/Brasil — pista de eliminação em contexto norte-americano
- `concepts/road-lines.md` — nota "desbotada" adicionada à entrada do México

**Conteúdo já documentado (não requereram edição):**
- Direção do sol/sombra → hemisfério (já em guia-iniciante seção 4)
- Placa amarela em Colômbia, Namíbia, Kenya, Uganda, Ruanda (já em todos os arquivos)
- Linhas de estrada Escandinávia (já em norway.md, sweden.md, finland.md, denmark.md)
- Chile → linhas brancas excepcionais nas Américas (já em chile.md)
- Linha externa amarela na África Austral (já em road-lines.md)
- "Sem placa dianteira → 17 estados americanos" (já em united-states.md)
- Postes preto+amarelo no Japão (já documentado)

**Arquivos atualizados:** `guia-iniciante.md`, `road-lines.md`, `mexico.md`  
**Fonte adicionada ao frontmatter:** `somerandomstuff1.wordpress.com`

---

## 2026-04-17 — INGEST: geomastr.com — territórios e microestados (varredura real de conteúdo)

**Operação:** INGEST (busca efetiva de conteúdo geomastr para todos os territórios)  
**Escopo:** ~35 territórios/microestados/ilhas verificados via WebFetch; conteúdo incorporado onde disponível

**Conteúdo incorporado:**
- `monaco.md` — postos: Avia, Agip, Esso
- `san-marino.md` — postos: Tamoil, Agip, IP, Eni, Q8
- `montenegro.md` — postos: Lukoil, EKO, Petrol, INA, Teboil, EuroPetrol
- `isle-of-man.md` — postos: Total (road lines: Yellow outside / White inside)
- `jersey.md` — postos: Total, Esso, Rubis (road lines: Yellow outside / White inside)
- `bermuda.md` — postos: Esso, Rubis
- `gibraltar.md` — postos: Cepsa (road lines: Yellow outside / White inside)
- `us-virgin-islands.md` — postos: Total
- `puerto-rico.md` — postos: Total, Puma (road lines: White outside / Yellow inside)

**Já tinham conteúdo (não requereram edição):**
- `greece.md` — combustível já presente (EKO, Revoil, Elin, AegeanOil)
- `iceland.md` — combustível já presente (N1, Orkan, Skeljungur)

**Páginas geomastr vazias confirmadas (sem dados textuais):**
Cyprus, Liechtenstein, Svalbard, Macau, Réunion, Martinica, Alaska, Hawaii, Açores, Madeira, Ilhas Malvinas, Ilhas Pitcairn, Saint-Pierre e Miquelon, São Tomé e Príncipe, Antártida, Ilhas Cocos, Ilhas Marianas do Norte, Samoa Americana, Ilha Christmas, Groenlândia, Curaçao

**Atualizado:** `wiki/log.md`

---

## 2026-04-17 — INGEST: geomastr.com — VARREDURA COMPLETA (todos os 136 arquivos)

**Operação:** INGEST (finalização da varredura geomastr.com)  
**Escopo:** Todos os arquivos restantes — territórios, microestados, ilhas e países perdidos na primeira passagem  
**Resultado:** 100% dos 136 arquivos de países têm `geomastr.com` no frontmatter `sources`

**Países/territórios com conteúdo novo incorporado:**
- `united-arab-emirates.md` — postos: ADNOC (exclusivo UAE), ENOC, EPPCO, Emarat

**Países atualizados (frontmatter apenas — geomastr sem dados úteis ou fuel já presente):**
- Frontmatter + sources adicionados: Peru, Ecuador, Ghana, Pakistan, Nepal, Lebanon, Bhutan, Hong Kong, China, Iraq, Oman
- Territórios europeus: Faroe Islands, Gibraltar, Greenland, Monaco, San Marino, Cyprus, Liechtenstein, Svalbard, Montenegro, Andorra
- Territórios das Américas: Puerto Rico, Curacao, Alaska, Bermuda, Falkland Islands, Hawaii, Martinique, Saint-Pierre and Miquelon, South Georgia, US Minor Outlying Islands, US Virgin Islands
- Territórios asiáticos/Oceania: Macau, Northern Mariana Islands, Guam, Cocos Islands, Christmas Island, American Samoa, Pitcairn Islands, British Indian Ocean Territory
- África: Sao Tome and Principe
- Antártida
- Passagem perdida anterior: Greece, Iceland

**Atualizado:** `wiki/index.md` (data → 2026-04-17); `wiki/log.md`

---

## 2026-04-14 — INGEST: geomastr.com — postos de combustível + dados de estrada (~35 países)

**Operação:** INGEST (complementação quad-source: + geomastr.com)  
**Fonte:** geomastr.com/country/{slug} — dados de road lines, bollards, fuel stations, domínio, prefixo  
**Escopo:** ~35 países atualizados; `geomastr.com` adicionado ao frontmatter `sources` de todos

**Países processados e conteúdo incorporado:**

- `south-africa.md` — linhas externas vermelhas em zonas urbanas especiais; postos: Total, Puma, Caltex, BP, Sasol, Engen, Shell
- `indonesia.md` — bollards vermelho+branco listrado; postos: Pertamina (exclusivo), Caltex
- `japan.md` — postos: ENEOS, Idemitsu, CosmoOil (exclusivos)
- `south-korea.md` — postos: SK Energy, GS Caltex, Hyundai Oilbank, S-Oil, E1
- `brazil.md` — postos: Ipiranga, BR Distribuidora, Raizen/Shell
- `argentina.md` — postos: YPF (exclusivo), Puma, Esso, AxionEnergy
- `russia.md` — postos: Lukoil, Rosneft, Gazprom, Tatneft
- `india.md` — postos: IndianOil, BharatPetroleum, HindustanPetroleum
- `turkey.md` — postos: Opet, PetrolOfisi (exclusivos)
- `mexico.md` — postos: Pemex (exclusivo estatal)
- `kenya.md` — postos: KenolKobil (exclusivo Quênia/África Oriental)
- `nigeria.md` — postos: Oando, ForteOil, MRSOilNigeria
- `ghana.md` — postos: Goil, AlliedOil
- `chile.md` — postos: COPEC (exclusivo do Chile)
- `colombia.md` — postos: EcoPetrol, Terpel, Biomax
- `peru.md` — postos: PetroPeru, Primax, Pecsa
- `ecuador.md` — postos: Petroecuador (exclusivo estatal)
- `australia.md` — postos: Caltex, ColesExpress, Woolworths Petrol, United Petroleum
- `new-zealand.md` — postos: Z Energy (exclusivo NZ)
- `france.md` — postos: Total, Esso, Carrefour, E.Leclerc
- `germany.md` — postos: Aral (exclusivo Alemanha)
- `italy.md` — postos: Eni/Agip (exclusivos Itália)
- `poland.md` — postos: Orlen, Lotos (exclusivos Polônia)
- `romania.md` — postos: Petrom, Rompetrol (exclusivos Romênia)
- `portugal.md` — postos: Galp (exclusivo Portugal/Ibéria)
- `canada.md` — postos: Petro-Canada (exclusivo Canadá), Irving (leste)
- `vietnam.md` — postos: Petrolimex, PVOil (estatais Vietnã)
- `malaysia.md` — postos: Petronas (exclusivo Malásia)
- `philippines.md` — postos: Petron, Phoenix Petroleum, Seaoil
- `senegal.md` — postos: Petrosen (estatal Senegal)
- `rwanda.md` — postos: MountMeru (África Oriental); linhas centrais amarelas confirmadas
- `tunisia.md` — postos: Agil (exclusivo Tunísia)
- `uganda.md` — postos: Hass Petroleum (África Oriental); bollards vermelho+branco
- `spain.md` — postos: Repsol, Cepsa (dominantes), Disa (exclusivo Canárias)
- `united-kingdom.md` — postos: Tesco, Morrisons, Asda, Sainsbury's (exclusivos UK)
- `united-states.md` — sources atualizado (fuel já documentado na sessão anterior)

**Conceitos atualizados:**
- `wiki/concepts/bollards.md` — Indonésia: bollards vermelho+branco listrado adicionados
- `wiki/concepts/road-lines.md` — África do Sul linhas externas vermelhas em zonas urbanas; Ruanda/Uganda adicionados à tabela de linha central amarela; nota sobre UK/Espanha linhas amarelas laterais de estacionamento

**Metodologia:**
- Hub/category pages do geomastr (continent, bollards, alphabets) retornam apenas galerias de imagens sem texto útil
- Dados textuais obtidos exclusivamente de páginas individuais de país: geomastr.com/country/{slug}/
- Rate limit atingido em 2026-04-12 para lote de 8 países; retomado em 2026-04-14

**Atualizado:** `wiki/index.md` (data → 2026-04-14); `wiki/log.md`

---

## 2026-04-11 — INGEST: geodummy.com — varredura completa (~120 países)

**Operação:** INGEST (complementação tri-source: plonkit.net + geotips.net + geodummy.com)  
**Fonte:** geodummy.com/{country-slug} para todos os países com página wiki existente  
**Escopo:** ~120 países verificados; `geodummy.com` adicionado ao frontmatter `sources` de todos os países com resposta 200

**Países com conteúdo novo incorporado:**

- `madagascar.md` — jeeps de gaiola; canoas lakana; cores variadas de placa (amarela/preta/branca, às vezes tarja azul ou verde)
- `malaysia.md` — retângulos pretos com texto nos postes; meio-fio amarelo
- `malta.md` — Gen 3: carro branco (cobertura principal)
- `martinique.md` — placas com faixa azul à direita
- `nepal.md` — shitcam montada em moto; placas com texto e borda vermelha
- `new-zealand.md` — marcações de bus lane verdes
- `nigeria.md` — Gen 3 com barras listradas preto+amarelo
- `peru.md` — placas antigas amarelas ainda em circulação; sinais de cidade azuis
- `portugal.md` — pinheiro-manso (Pinus pinea); lombadas de paralelepípedo
- `puerto-rico.md` — placa traseira com faixa verde no fundo
- `reunion.md` — placas EU com segunda faixa azul à direita
- `romania.md` — postes com listras diagonais vermelho e branco
- `russia.md` — sinais direcionais azuis grandes
- `san-marino.md` — Gen 2: carro preto
- `serbia.md` — casas estilo cottage fora das cidades
- `south-africa.md` — JoJo tanks (depósitos de água); árvores candelabra (Euphorbia sp.)
- `spain.md` — Gen 2 disponível em partes do país
- `sweden.md` — casas brancas com telhados laranja em Gotemburgo/Västra Götaland
- `switzerland.md` — placa traseira alta e estreita com texto em duas linhas
- `tanzania.md` — placas amarelas com texto preto
- `thailand.md` — netted poles; postes preto+laranja; muros de pedra no NE; plantações de borracha e dendê
- `turkey.md` — caixas d'água cilíndricas nos telhados; placas com fonte em negrito pronunciado
- `united-arab-emirates.md` — caixas d'água brancas nos edifícios; placas de Abu Dhabi com faixa vermelha no topo
- `united-states.md` — sinais de rua com fundo verde (vs. azul Canadá); marcadores de gasoduto amarelos/laranjas

**Países com sources atualizadas, sem conteúdo novo** (informação já documentada):  
mexico, monaco, mongolia, montenegro, netherlands, north-macedonia, norway, pakistan, philippines, poland, qatar, rwanda, senegal, singapore, slovakia, slovenia, south-korea, sri-lanka, taiwan, tunisia, ukraine, uganda, united-kingdom, uruguay, vanuatu, vietnam

**Países que retornaram 404 no geodummy** (sources não atualizadas):  
oman, panama, namibia, macau (verificados em sessão anterior)

**Atualizado:** `wiki/index.md` (data); `wiki/log.md`

---

## 2026-04-11 — VARREDURA COMPLETA: cobertura real do geotips.net

**Operação:** Verificação e complementação do INGEST geotips.net  
**Conclusão:** geotips.net cobre apenas **~47 países** (não 100+). Países não cobertos pelo geotips ficam apenas com `plonkit.net` como fonte.

**Países cobertos pelo geotips por região:**
- Europa: Romania, Hungary, Albania, Iceland, UK, Denmark (6)
- América do Sul: Brazil, Argentina, Peru (3)
- Ásia: Philippines, UAE, Malaysia, Jordan, Laos, Hong Kong, Mongolia, Japan, Sri Lanka, Kyrgyzstan, Bhutan, Cambodia, Macau, Nepal, Thailand, South Korea (16)
- América do Norte: USA, Mexico, Guatemala, Costa Rica, US Virgin Islands, Canada, Puerto Rico, Greenland (8)
- Oceania: Australia, New Zealand, Christmas Island, Guam, Northern Mariana Islands, Cocos Islands (6)
- África: South Africa, Botswana, Nigeria, Ghana, Senegal, Kenya (6) + Eswatini/Lesoto mencionados mas truncados

**Correções e adições desta sessão:**
- `northern-mariana-islands.md` — frontmatter sources corrigido (estava ausente)
- `nigeria.md` — divisores de concreto nas cores da bandeira (verde+branco)
- `ghana.md` — bollards estilo UK (herdado do Commonwealth)

**Total final de arquivos com `sources: [plonkit.net, geotips.net]`:** 44 países

---

## 2026-04-11 — INGEST: geotips.net — todos os continentes (~44 países atualizados)

**Operação:** INGEST (complementação dual-source: plonkit.net + geotips.net)  
**Fonte:** geotips.net/south-america, /europe, /asia, /north-america, /africa, /oceania  
**Escopo:** ~44 países atualizados; `sources: [plonkit.net, geotips.net]` adicionado ao frontmatter de todos

**Conteúdo novo incorporado por região:**

**Europa:**
- `denmark.md` — refletores VERDES nos bollards (exclusivos da Dinamarca na Europa)
- `albania.md` — veículos Dacia predominantes; táxis com placas no teto; formato de telefone (prefixo de área + "2" para fixos; 06X = celular)
- `iceland.md` — adesivo de inspeção amarelo-neon visível na placa traseira (Gen 4 recente)
- `bhutan.md` — sistema waystone SL-1; divisão em 20 dzongkhags
- `senegal.md` — rachaduras longitudinais na superfície das estradas; prefixo de telefone (7x = celular, 3x = fixo; DK = Dakar, KD = Kolda)
- `ghana.md` — fita preta não cobre sempre o rack (sem fita em Boabeng); tro-tros (vans combi coletivas) como pista
- `romania.md` — marcadores de tensão em amarelo nos postes; bollards "marco" coloridos por tipo de estrada (amarelo=local, azul=condado, vermelho=nacional, verde=europeia/via expressa)
- `hungary.md` — postes de concreto SEM marcador amarelo (diferencia de Romênia)
- `united-kingdom.md` — sinais de aviso em postes de madeira com raio amarelo; Belisha beacons (globo laranja nas faixas de pedestres zebra — exclusivo UK)

**América do Sul:**
- `brazil.md` — placa de STOP "PARE" (vs. "ALTO" no México/América Central)
- `argentina.md` — variante em concreto dos postes A-frame; esquinas chanfradas "ochava" nas cidades em grade
- `peru.md` — eucaliptos muito comuns entre 2000–3500m; celulares sempre começam com 9 (9 dígitos); fixos: 7 dígitos Lima/Callao, 6 dígitos resto do país

**Ásia:**
- `japan.md` — folhas de abóbora/squash em Hokkaido (detalhe sazonal de vegetação)
- `south-korea.md` — bollards brancos com listra preta e ponto amarelo (design exclusivo KR)
- `cambodia.md` — sistema de numeração de rodovias: 8 estradas de 1 dígito saindo de Phnom Penh em sentido horário
- `philippines.md` — quadras de basquete em todo o país; cartazes de eleição ubíquos
- `malaysia.md` — bollards brancos com retângulos vermelhos; árvore Yellow Meranti diagnóstica
- `laos.md` — prefixo de telefone: código de área com 0, celular começa com 02
- `jordan.md` — táxis com fundo verde e teto prateado
- `sri-lanka.md` — códigos de província nas placas (WP, SP, CP, NP, EP, UP, NW, SG, NC); celulares começam com 07

**América do Norte:**
- `united-states.md` — linha central dupla amarela (vs. Canadá = linha simples mais comum); ônibus escolares amarelos exclusivos; 17 estados sem placa frontal
- `canada.md` — cobertura de snowmobile no Ártico; linha central simples amarela (mais comum que nos EUA)
- `mexico.md` — táxis rosa+branco exclusivos da Cidade do México
- `guatemala.md` — formato de telefone (8 dígitos, primeiro dígito = tipo); marcações Una Via/Doble Via; placas pequenas (15×30cm)
- `costa-rica.md` — táxis vermelhos com placa amarela no teto; prefixos (5/6/7/8 = celular, 2/4 = fixo; 8 dígitos)
- `us-virgin-islands.md` — código de área 340; taxis tipo pickup aberto; guardrails amarelos em áreas perigosas

**África:**
- `south-africa.md` — carro camuflado no Parque Nacional Kruger (único no mundo)
- `botswana.md` — sinais de rodovia com fundo verde + letra "A" (único na região); bollards azulados perto de Gabane
- `nigeria.md` — posição da luz de emergência do carro policial (esquerda = sul/Lagos; direita = norte/Abuja); cores de táxi por cidade (Lagos, Abuja, Asaba, Enugu, Ibadan)
- `kenya.md` — veículo safari na Lewa Wildlife Conservancy (único nessa localidade)

**Oceania:**
- `australia.md` — cores de ônibus por estado (8 estados); semáforos com borda branca por estado (WA/NSW/QLD/TAS/ACT = com borda; VIC/SA/NT = sem); Hungry Jack's confirma Austrália
- `new-zealand.md` — tabela de códigos de área (02/03/04/06/07/09); palavras maori com macrons
- `christmas-island.md` — sinais de nome de rua com fundo amarelo (distinto do padrão australiano)
- `guam.md` — painéis de acesso elétrico perto de sinais de stop; postes com bases brancas e azuis
- `northern-mariana-islands.md` — marcadores de milha com frações; marcadores de rota com formato de copo (cup-shaped)
- `cocos-islands.md` — sinais bilíngues inglês/malaio (único território australiano com isso)

**Apenas sources atualizadas (conteúdo já completo):** UAE, Hong Kong, Thailand, Macau, Puerto Rico, Greenland, Mongolia, Kyrgyzstan

**Atualizado:** `wiki/index.md` (data → 2026-04-11); `wiki/log.md`

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
