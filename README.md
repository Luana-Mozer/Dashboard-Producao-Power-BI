# Dashboard de Producao Power BI

Projeto de dashboard de producao criado a partir da base `Produção.xlsx`, seguindo o layout visual do arquivo `Plano de Fundo.png`.

## Entregaveis

- `powerbi/Dashboard_Producao.pbip`: projeto Power BI preparado para abrir no Power BI Desktop.
- `powerbi/tema-dashboard-producao.json`: tema visual escuro com cores do layout.
- `powerbi/medidas-dashboard-producao.dax`: medidas DAX usadas nos KPIs, grafico e gauges.
- `powerbi/MONTAGEM_DASHBOARD_POWER_BI.md`: guia de montagem do report no Power BI.
- `entregaveis/preview-dashboard-producao.png`: pre-visualizacao do dashboard com os dados reais.
- `entregaveis/resumo-dashboard-producao.xlsx`: resumo conferido dos indicadores.

## Indicadores principais

- Total Aprovado: 3.084.251
- Total Rejeitado: 21.076
- Horas Produtivas: 30.956
- Horas Paradas: 8.890
- Disponibilidade: 77,69%
- Qualidade: 99,32%

## Como usar

Abra `powerbi/Dashboard_Producao.pbip` no Power BI Desktop. Se o Power BI solicitar o caminho da base, selecione o arquivo `Produção.xlsx` que esta na raiz do projeto. Depois importe o tema `powerbi/tema-dashboard-producao.json` e use o guia `powerbi/MONTAGEM_DASHBOARD_POWER_BI.md` para conferir o posicionamento dos visuais.
