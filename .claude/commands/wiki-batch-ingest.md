---
description: Processa todos os arquivos novos em raw/countries/ e compila o wiki
allowed-tools: Read, Write, Bash, Glob, Grep, WebSearch
---

# Wiki Batch Ingest

Leia o CLAUDE.md para seguir as convenções do projeto.

1. Liste todos os arquivos em raw/countries/ usando Glob
2. Liste todos os arquivos já processados em wiki/countries/
3. Identifique quais arquivos de raw/countries/ ainda NÃO têm correspondente em wiki/countries/
4. Para cada arquivo não processado:
   a. Leia o conteúdo do arquivo raw
   b. Compile a página wiki em wiki/countries/{slug}.md seguindo a estrutura padrão do CLAUDE.md
   c. Identifique conceitos novos e crie/atualize páginas em wiki/concepts/
   d. Adicione [[wikilinks]] entre países relacionados e conceitos
   e. Reporte: "✅ Processado: {país}"
5. Após processar todos, atualize wiki/index.md com todas as entradas
6. Registre todas as operações em wiki/log.md
7. Apresente um resumo final: quantos países processados, quantos conceitos criados
