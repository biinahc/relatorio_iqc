# Relatório IQC

Dashboard de Controle de Qualidade para inspeção de peças, criado como uma página única (`index.html`).

## Funcionalidade

- Importa arquivos Excel (`.xlsx` ou `.xlsm`) contendo dados de IQC.
- Detecta automaticamente a aba válida do relatório e permite selecionar outras abas, se houver.
- Analisa as linhas de relatório de inspeção por turno, com agrupamento de:
  - Quantidade inspecionada
  - Quantidade de defeitos
  - Defeitos encontrados

## Recursos do Dashboard

- Painel de upload com drag-and-drop e seleção de arquivo.
- Alternância entre visão mensal e semanal.
- Filtro por turno: `Ambos os Turnos`, `1º Turno`, `2º Turno`.
- Seleção de intervalo de dias para visão semanal.
- Indicadores-chave (KPIs):
  - Peças inspecionadas
  - Peças com defeito
  - Total de defeitos
  - Item crítico com maior número de defeitos
- Gráficos interativos usando Chart.js:
  - Comparativo de produtividade vs qualidade entre turnos
  - Gráfico donut de tipos de defeito
  - Ranking de peças críticas com mais defeitos
- Lista de não conformidades detalhadas e tabela de itens do IQC.
- Busca, ordenação e paginação na tabela de itens.

## Como usar

1. Abra `index.html` no navegador.
2. Faça upload de um arquivo Excel válido (`.xlsx` ou `.xlsm`).
3. Selecione a aba correta quando necessário.
4. Use os filtros e controles para explorar os dados de inspeção e defeitos.

## Tecnologia

- HTML/CSS com Tailwind via CDN
- JavaScript puro para leitura e análise de arquivos Excel
- SheetJS (`xlsx`) para parse do Excel
- Chart.js para visualização de dados

## Observações

- O parser é otimizado para relatórios IQC com estrutura de tripletos (`QTD INSPECIONADA`, `QTD DEFEITOS`, `DEFEITOS ENCONTRADOS`).
- O dashboard já inclui dados demo para testes, que podem ser usados se não houver upload imediato.
