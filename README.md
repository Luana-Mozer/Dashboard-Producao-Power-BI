# Dashboard de Produção - Power BI

<img width="1360" height="731" alt="Image" src="https://github.com/user-attachments/assets/e08d3476-05ed-4a49-b988-f44deef22217" />

Este projeto foi criado para acompanhar a produção de uma equipe no Power BI, usando uma base em Excel com ordens de produção, operadores, produtos, ocorrências, horas trabalhadas, quantidade aprovada e quantidade rejeitada.

A principal ideia do dashboard é permitir uma leitura rápida da produção individual de cada funcionário e também analisar o desempenho em cada mês. Assim fica mais fácil entender quem produziu mais, onde ocorreram paradas, quais produtos tiveram rejeição e como a produção evoluiu ao longo do tempo.

## Demonstração do dashboard

<video src="Midia/video-producao.mp4" controls width="100%"></video>

Caso o vídeo não carregue automaticamente no GitHub, ele também está disponível neste arquivo:

[Assistir ao vídeo de demonstração](Midia/video-producao.mp4)

## Base utilizada

A base original está no arquivo `Producao.xlsx` e possui as seguintes informações:

- número da ordem de produção;
- nome do operador/funcionário;
- produto produzido;
- ocorrência registrada, quando existiu parada ou etapa específica;
- data e hora de início;
- data e hora de fim;
- total de horas;
- quantidade aprovada;
- quantidade rejeitada.

Essas colunas foram usadas para montar indicadores de produção, horas produtivas, horas paradas e rejeições.

## Passo a passo da criação

1. Abri a planilha no Power BI Desktop.
2. Usei o Power Query para conferir os tipos de dados, como datas, horas, textos e números.
3. Organizei a base para trabalhar com os campos de operador, produto, ocorrência, total de horas, quantidade aprovada e quantidade rejeitada.
4. Criei os indicadores principais do dashboard:
   - total produzido;
   - total rejeitado;
   - horas produtivas;
   - horas paradas.
5. Montei os gráficos para acompanhar a produção por período.
6. Adicionei filtros para analisar os dados por funcionário, produto e mês.
7. Finalizei o visual usando o fundo personalizado `fundo.png` e os ícones da pasta `Icones`.

## O que o dashboard permite analisar

Com o dashboard final, é possível acompanhar:

- a produção individual de cada funcionário;
- a produção de cada funcionário em cada mês;
- a quantidade total produzida;
- a quantidade rejeitada;
- as horas produtivas;
- as horas paradas;
- os produtos analisados;
- as ocorrências que impactaram a produção.

Esse tipo de análise ajuda a transformar uma planilha operacional em uma visão mais clara para tomada de decisão.

## Ferramentas utilizadas

- Power BI Desktop
- Power Query
- Excel
- GitHub

## Arquivos do projeto

- `Dashboard Producao.pbix`: arquivo principal do Power BI com o dashboard final.
- `Producao.xlsx`: planilha usada como base de dados.
- `fundo.png`: imagem de fundo utilizada no dashboard.
- `Icones/`: ícones usados nos cards de indicadores.
- `Midia/video-producao.mp4`: vídeo de demonstração do dashboard.

## Como visualizar

1. Baixe este repositório.
2. Abra o arquivo `Dashboard Producao.pbix` no Power BI Desktop.
3. Se o Power BI pedir, atualize o caminho da base para o arquivo `Producao.xlsx`.
4. Use os filtros do dashboard para analisar a produção por funcionário, produto e mês.

## O que aprendi com esse projeto

Esse projeto me ajudou a praticar a criação de um dashboard operacional no Power BI, conectando uma base de produção em Excel a uma visualização mais objetiva.

Também foi uma forma de reforçar como filtros bem escolhidos ajudam a responder perguntas importantes, principalmente quando o objetivo é acompanhar a produção individual de funcionários ao longo dos meses.

---

Projeto desenvolvido para meu portfólio de análise de dados.
