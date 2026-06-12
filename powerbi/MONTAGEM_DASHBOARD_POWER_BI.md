# Dashboard de Producao no Power BI

Este projeto foi preparado para recriar o painel da imagem de referencia usando a base `Produção.xlsx`, o fundo `Plano de Fundo.png` e os icones da pasta `Ícones`.

## Estrutura visual

- Pagina: 16:9, 1920 x 1080.
- Plano de fundo: `Plano de Fundo.png`, ajuste `Fit`, transparencia `0%`.
- Tema: importar `powerbi/tema-dashboard-producao.json`.
- Fonte sugerida para titulos e valores: Segoe UI Semibold.

## Campos criados no modelo

- `Mes Numero`: ordenacao do mes.
- `Mes`: nome do mes para o eixo do grafico.
- `Tipo Hora`: classifica linhas com ocorrencia como `Parada` e linhas sem ocorrencia como `Produtiva`.

## Medidas DAX

As medidas tambem estao no arquivo `powerbi/medidas-dashboard-producao.dax`.

```DAX
Total Aprovado = SUM ( BaseProducao[Qtd Aprovada] )
Total Rejeitado = SUM ( BaseProducao[Qtd Rejeitada] )
Horas Totais = SUM ( BaseProducao[Total Horas] )
Horas Produtivas = CALCULATE ( [Horas Totais], BaseProducao[Tipo Hora] = "Produtiva" )
Horas Paradas = CALCULATE ( [Horas Totais], BaseProducao[Tipo Hora] = "Parada" )
Disponibilidade = DIVIDE ( [Horas Produtivas], [Horas Totais] )
Qualidade = DIVIDE ( [Total Aprovado], [Total Aprovado] + [Total Rejeitado] )
Aprovado Mil = DIVIDE ( [Total Aprovado], 1000 )
```

## Posicionamento sugerido

Use os blocos vazios do fundo como encaixe dos visuais:

- KPI 1: icone `Produzido.png` + Cartao `[Total Aprovado]`.
- KPI 2: icone `Rejeitado.png` + Cartao `[Total Rejeitado]`.
- KPI 3: icone `Hora Produtiva.png` + Cartao `[Horas Produtivas]`.
- KPI 4: icone `Hora Parada.png` + Cartao `[Horas Paradas]`.
- Slicer 1: `Operador`.
- Slicer 2: `Mes`.
- Grafico central: Grafico de area com eixo `Mes`, valores `[Total Aprovado]`, ordenado por `Mes Numero`.
- Gauge esquerdo: valor `[Disponibilidade]`, minimo `0`, maximo `1`, formato percentual.
- Gauge direito: valor `[Qualidade]`, minimo `0`, maximo `1`, formato percentual.

## Valores conferidos na base

- Total Aprovado: `3.084.251`.
- Total Rejeitado: `21.076`.
- Horas Produtivas: `30.956`.
- Horas Paradas: `8.890`.
- Disponibilidade: `77,69%`.
- Qualidade: `99,32%`.

## Observacao tecnica

O arquivo `.pbip` e a pasta de modelo foram deixados no padrao de projeto do Power BI para controle de versao. Para gerar um `.pbix`, abra `powerbi/Dashboard_Producao.pbip` no Power BI Desktop, aplique o layout acima se o report abrir em branco, atualize a fonte da planilha caso o Power BI solicite o caminho absoluto e salve como `.pbix`.
