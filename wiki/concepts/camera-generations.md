---
title: "Gerações de Câmera do Street View por País"
date_created: 2026-04-10
date_modified: 2026-04-10
summary: "Referência de quais países têm qual geração de câmera do Google Street View. Complementa gerações-de-câmera.md com listagem por país e como identificar a geração visualmente."
tags: [conceito, câmera, street-view, gerações, identificação]
type: concept
status: draft
---

# Gerações de Câmera do Street View por País

Este conceito lista os países por geração de câmera e como identificar cada uma visualmente. Para descrição técnica detalhada de cada geração, ver [[gerações-de-câmera]].

---

## Como Identificar a Geração

### Sinais Visuais por Geração

| Geração | Resolução | Borrão | Antena | Outros |
|---|---|---|---|---|
| **Gen 1** | Muito baixa; pixelada | Quadrado | Não visível | Muito rara atualmente |
| **Gen 2** | Baixa-média | Oval | Não ou curta | Preto+branco no carro às vezes |
| **Gen 3** | Média-alta | Oval maior | Stubby com espiral | Antena visível na maioria |
| **Gen 4** | Alta | Oval menor | Antena menor ou sem | Mais nítida, menos ghosting |
| **Shitcam** | Muito baixa | Irregular | Visível | Imagem granulada, escura |
| **Lowcam** | Varia | Baixo ao chão | Curta ou sem | Câmera próxima do solo |
| **Smallcam** | Alta | Menor | Pequena | Carro menor; cobertura 2024+ |

---

## Gen 2 — Países com Cobertura

**Características visuais:** resolução menor, borrão oval, frequentemente é a cobertura mais antiga disponível.

| País | Notas |
|---|---|
| [[canada]] | Rural e áreas remotas; urbano já tem Gen 3/4 |
| [[hawaii]] | Todo território — antena frontal às vezes visível |
| [[jersey]] | **Exclusivamente Gen 2** — única geração disponível na ilha |
| [[south-africa]] | **Gen 2 é a ÚNICA câmera Gen 2 no continente africano** — confirma África do Sul imediatamente |
| [[monaco]] | Maioria Gen 2; alguns spills Gen 3 da França |
| [[bermuda]] | Gen 2 predominante |
| [[united-states]] | Algumas coberturas históricas; urbano tem Gen 3/4 |

> ⚠️ Ver [[south-africa]]: se você vir câmera Gen 2 na África, é quase certamente África do Sul — nenhum outro país africano tem Gen 2.

---

## Gen 3 — Países com Cobertura Predominante

**Características visuais:** antena stubby com espiral visível atrás, borrão oval maior, qualidade média-alta.

| País | Notas Diagnósticas |
|---|---|
| [[russia]] | Carro **preto** com antena longa — distingue do Gen 3 padrão |
| [[argentina]] | Carro **preto** (Gen 3) — diferente do Brasil |
| [[peru]] | Carro **preto** (Gen 3) |
| [[kyrgyzstan]] | Carro com **roofrack** (bagageiro no teto) + espelhos extras |
| [[brazil]] | Antena stubby com espiral; Gen 4 também disponível em algumas áreas |
| [[uruguay]] | **Exclusivamente Gen 3** (+ spill Gen 4 em ponte específica) |
| [[colombia]] | Gen 3 predominante |
| [[chile]] | Gen 3 misto |
| [[mexico]] | Gen 3 misto |
| [[france]] | Gen 3 com antena curta em algumas áreas; spill em [[monaco]] |
| [[germany]] | Gen 3/4 misto |
| [[south-korea]] | Gen 2 e Gen 3 disponíveis |
| [[turkey]] | Gen 3 predominante |
| [[india]] | Gen 3 base, mas frequentemente shitcam |
| [[japan]] | Gen 3/4 base, mas em lowcam — ver seção específica |

---

## Gen 4 — Países com Cobertura Recente

**Características visuais:** resolução mais alta, borrão menor e mais limpo, antena menor.

| País | Notas |
|---|---|
| [[united-states]] | Áreas urbanas e principais autoestradas |
| [[united-kingdom]] | Atualização contínua; Gen 4 nas cidades |
| [[france]] | Áreas urbanas e algumas estradas rurais |
| [[germany]] | Áreas urbanas |
| [[australia]] | Gen 4 nas cidades; interior pode ser Gen 3 |
| [[new-zealand]] | Gen 4 predominante |
| [[brazil]] | Gen 4 disponível, especialmente SP e sul |
| [[south-africa]] | Gen 4 smallcam — ver seção específica |
| [[japan]] | Gen 4 base, mas lowcam — imagem mais larga |
| [[sri-lanka]] | Gen 4 parcialmente em lowcam — ver seção lowcam |

---

## Shitcam — Câmera de Baixa Qualidade

**Características visuais:** imagem granulada e escura, resolução muito baixa, desfoque irregular, às vezes tremida. Identificada por ser visivelmente inferior a qualquer câmera Gen padrão.

| País | Notas |
|---|---|
| [[india]] | Shitcam é a câmera **primária** — quase toda cobertura da Índia é shitcam |
| [[nigeria]] | Shitcam em toda cobertura disponível |
| [[cambodia]] | Shitcam na maioria das áreas |
| [[lebanon]] | Shitcam em grande parte do país |
| [[ecuador]] | Shitcam em algumas áreas (misto com Gen normal) |

> A shitcam é o identificador mais imediato da **Índia** — se a qualidade for muito ruim, assuma Índia primeiro.

---

## Lowcam — Câmera Posicionada Baixo

**Características visuais:** perspectiva muito próxima do chão, estrada parece mais larga, borrão fica atrás e baixo, visualmente mais distorcida lateralmente.

| País | Notas |
|---|---|
| [[japan]] | Lowcam em **toda** a cobertura — carro preto e branco; borrão grande |
| [[switzerland]] | Lowcam em **toda** a cobertura — carro borroso (borrado o carro inteiro) |
| [[liechtenstein]] | Lowcam — idêntico à Suíça visualmente |
| [[sri-lanka]] | Lowcam **parcial** — apenas cobertura Gen 4; cobertura Gen 3 é normal |

**Como diferenciar Japão vs. Suíça (ambos lowcam):**
- [[japan]]: script em kanji/hiragana; vending machines; tráfego pela esquerda; carro preto+branco nítido
- [[switzerland]]: script latino/alemão/francês/italiano; tráfego pela direita; carro todo borroso

---

## Smallcam — Câmera Menor e Mais Nova

**Características visuais:** carro menor, câmera posicionada diferente, às vezes mais vistas inusitadas (capô visível, menos altura).

| País | Notas |
|---|---|
| [[brazil]] | Smallcam disponível em algumas áreas; antena menor |
| [[peru]] | Carro preto smallcam visível |
| [[argentina]] | Carro preto smallcam |
| [[south-africa]] | Antena do carro visível no smallcam Gen 4 — diagnóstico |
| [[hawaii]] | Parte frontal do carro às vezes visível na câmera |
| [[france]] | Algumas áreas com smallcam |

---

## Trekker — Câmera de Mochila ou Veículo Especializado

**Características visuais:** perspectiva de pedrestre ou veículo off-road; não é carro Google padrão; frequentemente em áreas sem acesso de carro.

| País / Local | Contexto |
|---|---|
| [[belarus]] | **Apenas trekker em Minsk** — não há carro Google convencional |
| [[pitcairn-islands]] | Trekker em ilha sem carros |
| [[vanuatu]] | Trekker em trilhas |
| [[british-indian-ocean-territory]] | Trekker em Diego Garcia |
| [[northern-mariana-islands]] | Trekker em algumas ilhas |
| Parques nacionais | Trekker em trilhas (vários países) |

---

## Tripod — Câmera Estática

**Características visuais:** sem movimento; panorâmica 360° de ponto fixo; frequentemente em locais turísticos ou interiores.

- Pontos turísticos em vários países
- Interiores de museus, monumentos, etc.
- ⚠️ Não representa cobertura de rua convencional — pino raramente aparece num tripod num round normal

---

## Carros Google por País

Alguns países têm carros Google com aparência distinta — pista diagnóstica mesmo sem ver texto:

| País | Aparência do Carro |
|---|---|
| [[kenya]] | **Caminhão cinza com snorkel** (pneus altos, antena alta) |
| [[kyrgyzstan]] | Carro com **roofrack** e espelhos extras |
| [[russia]] | Carro **preto** com antena longa |
| [[argentina]] | Carro **preto** (Gen 3) |
| [[peru]] | Carro **preto** (Gen 3) |
| [[japan]] | Carro **preto e branco** em lowcam |
| [[switzerland]] | Carro **completamente borroso** em lowcam |

---

## Cobertura por Câmera — Resumo Rápido

| Geração | Países Chave |
|---|---|
| **Gen 2 exclusivo** | [[jersey]] |
| **Gen 2 na África** | [[south-africa]] (único) |
| **Gen 3 exclusivo** | [[uruguay]] |
| **Shitcam** | [[india]], [[nigeria]], [[cambodia]], [[lebanon]], [[ecuador]] |
| **Lowcam** | [[japan]], [[switzerland]], [[liechtenstein]], [[sri-lanka]] (parcial) |
| **Trekker exclusivo** | [[belarus]] (apenas Minsk), [[pitcairn-islands]] |
| **Carro colorido diagnóstico** | [[kenya]] (caminhão cinza), [[russia]] (preto+longa), [[japan]] (P&B lowcam) |

---

Relacionados: [[gerações-de-câmera]] | [[japan]] | [[south-africa]] | [[india]] | [[switzerland]] | [[jersey]] | [[guia-iniciante]]
