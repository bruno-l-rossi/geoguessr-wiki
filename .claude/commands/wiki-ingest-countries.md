---
description: Pesquisa e compila páginas de países para o GeoGuessr wiki
allowed-tools: Read, Write, Bash, Glob, Grep, WebFetch, WebSearch
---

# Wiki Country Ingest

Leia o CLAUDE.md para seguir as convenções do projeto.

Para cada país na lista fornecida:
1. Tente acessar https://www.plonkit.net/{country-slug} e extraia o conteúdo
2. Se o plonkit não estiver acessível, faça uma pesquisa web por "GeoGuessr {country name} tips clues guide plonkit"
3. Salve o material bruto em raw/countries/{country-slug}-plonkit.md
4. Compile a página wiki em wiki/countries/{country-slug}.md seguindo a estrutura padrão do CLAUDE.md
5. Crie páginas em wiki/concepts/ para qualquer conceito novo mencionado
6. Atualize wiki/index.md e wiki/log.md após cada país

Lista de países a processar: $ARGUMENTS

Processe um país por vez e reporte o progresso. Se um país falhar, continue para o próximo e registre o erro no log.
