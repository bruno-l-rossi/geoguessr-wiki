# GeoGuessr Wiki — Schema

## Visão Geral
Base de conhecimento pessoal sobre GeoGuessr, focada em identificação de países e regiões. Fontes brutas ficam em `raw/`. O wiki compilado fica em `wiki/`. Você (o AI) mantém todo o conteúdo do wiki. Eu defino a estratégia; você executa a compilação, manutenção e consultas.

## Estrutura de Diretórios
- `raw/countries/` — Material fonte sobre cada país (textos colados, anotações)
- `wiki/countries/` — Uma página compilada por país
- `wiki/concepts/` — Conceitos gerais (vegetação, arquitetura, tipos de câmera, etc.)
- `wiki/outputs/` — Respostas a consultas específicas
- `wiki/index.md` — Índice mestre (mantido por você)
- `wiki/log.md` — Log de operações (mantido por você)

## Convenções de Arquivos
- Nomes em kebab-case minúsculo (ex: `brazil.md`, `south-america.md`)
- Toda página DEVE ter frontmatter YAML no topo:
  ---
  title: "Nome do País"
  date_created: YYYY-MM-DD
  date_modified: YYYY-MM-DD
  summary: "Uma ou duas frases descrevendo o conteúdo"
  tags: [país, continente]
  type: country
  status: draft
  ---
- Use [[wikilinks]] para referências internas
- Negrite termos-chave na primeira ocorrência

## Estrutura Padrão de Página de País
Cada página de país em `wiki/countries/` deve seguir esta estrutura:

1. **Visão Geral** — Localização, idioma, população, capital
2. **Câmera e Cobertura** — Tipo de câmera do Street View (cor, qualidade, altura), cobertura disponível
3. **Pistas Visuais Principais** — As dicas mais confiáveis para identificar o país
4. **Vegetação e Paisagem** — Flora típica, terreno, clima visual
5. **Arquitetura e Infraestrutura** — Estilo de casas, postes, fios elétricos, muros
6. **Sinais e Textos** — Idioma nas placas, formato de placas de trânsito, toponímia
7. **Veículos e Transporte** — Tipos de carros, ônibus, motos comuns
8. **Regiões Distintas** — Sub-regiões com características visuais diferentes
9. **Pegadinhas Comuns** — Erros frequentes, países que confundem com este
10. **Resumo Rápido** — Bullet points das 5 pistas mais decisivas

## Operações

### INGEST (quando adiciono fontes brutas)
1. Ler o arquivo fonte em raw/
2. Criar ou atualizar a página do país em wiki/countries/
3. Identificar conceitos gerais mencionados (vegetação, arquitetura, etc.)
4. Criar ou atualizar páginas de conceitos em wiki/concepts/
5. Adicionar [[wikilinks]] conectando países a conceitos relacionados
6. Atualizar wiki/index.md
7. Registrar em wiki/log.md

### QUERY (quando faço uma pergunta)
1. Ler wiki/index.md para entender o conteúdo disponível
2. Ler as páginas relevantes
3. Sintetizar resposta com citações em [[wikilinks]]
4. Salvar resposta em wiki/outputs/
5. Atualizar index.md e log.md

### RESEARCH (quando peço para pesquisar um país)
1. Usar web search para buscar informações de GeoGuessr sobre o país
2. Focar em: dicas visuais, câmera, vegetação, arquitetura, placas, regiões
3. Compilar página completa seguindo a estrutura padrão acima
4. Salvar em wiki/countries/
5. Atualizar index.md e log.md

### LINT (verificação de qualidade)
1. Encontrar contradições entre páginas
2. Encontrar páginas órfãs (sem links de entrada)
3. Identificar [[wikilinks]] quebrados
4. Sinalizar conteúdo incompleto
5. Sugerir novos países ou conceitos para adicionar

## Padrão de Qualidade
- Foco prático: cada dica deve ser acionável durante o jogo
- Sempre indicar nível de confiança: alta / média / baixa
- Sinalizar dicas que se sobrepõem com países vizinhos com ⚠️
- Preferir informação visual e concreta a descrições abstratas
- Resumo Rápido deve ter exatamente 5 bullet points, os mais decisivos
