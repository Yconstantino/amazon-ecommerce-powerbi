# Amazon E-commerce — Análise de Vendas no Power BI

Dashboard interativo e apresentação de insights sobre **51.290 pedidos** de um e-commerce em 2018.

![Visão geral](imagens/slide-2.png)

## Perguntas de negócio

1. **Qual tipo de login meus clientes preferem ao comprar?**
2. **Como a data e a hora afetam minhas vendas?**
3. **De qual produto obtenho o maior lucro por unidade?**

## Principais insights

| Pergunta | Resposta |
|---|---|
| Login preferido | **Member**, com 95,7% das vendas (49.097). Guest vem em 2º, com 3,9%. |
| Hora do dia | **81% das vendas acontecem entre 10h e 22h**, com pico às 11h. Da 1h às 6h há só 2,8% das vendas. |
| Data | Jan a abr é o período mais fraco (fevereiro é o pior mês). **Novembro é o melhor mês** (R$ 8,8 mi). O dia da semana muda pouco (~15%). |
| Lucro por unidade | **Apple Laptop: 67,12 por unidade**, seguido de Tyre (65,40) e Iron (57,21). Por categoria, Fashion lidera (31,10). |

| | |
|---|---|
| ![Login](imagens/slide-3.png) | ![Hora](imagens/slide-4.png) |
| ![Data](imagens/slide-5.png) | ![Lucro](imagens/slide-6.png) |

## Recomendações

- Converter clientes **Guest em Member**, com incentivo no checkout.
- Concentrar campanhas na janela **10h–22h**.
- Criar promoções sazonais para levantar **jan a abr**.
- Dar mais visibilidade aos produtos de **maior margem por unidade**.

## O dashboard

O arquivo [`dashboard/Dashboard Amazon.pbix`](dashboard/) tem 4 páginas: Visão Geral, Tipo de Login, Data e Hora, e Lucro por Produto. Ele usa:

- tema escuro com as cores da Amazon (laranja `#FF9900` e azul `#00A8E1`);
- 7 filtros sincronizados entre as páginas (período, categoria, dispositivo, gênero, login, forma de pagamento e prioridade);
- medidas DAX próprias ([`dax/medidas_e_colunas.dax`](dax/medidas_e_colunas.dax)).

> O modelo aponta para um Excel local e para um SQL Server local. Para **atualizar** os dados é preciso ajustar as fontes em *Transformar dados*. Para só **visualizar**, basta abrir o arquivo no Power BI Desktop.

## Apresentação

[`apresentacao/`](apresentacao/) tem a apresentação de 8 slides em PowerPoint (editável) e em PDF.

## Ferramentas

Power BI Desktop · DAX · SQL Server · Excel

## Estrutura

```
├── dashboard/      → arquivo .pbix
├── apresentacao/   → .pptx e .pdf com os insights
├── dax/            → medidas e colunas calculadas
└── imagens/        → slides usados neste README
```

