# Tech Challenge Olist Insights

![Esquema dos datasets](assets/data_set_schemas.png)

Este repositório contém um notebook Python para análise exploratória dos datasets da Olist Store.

## Visão geral

O notebook realiza a leitura dos dados principais do Olist, faz cruzamentos entre clientes, pedidos, itens, produtos e pagamentos, e gera insights visuais para apoiar análises de negócios.

## Dataset

Os dados utilizados são do conjunto "Brazilian E-Commerce Public Dataset" da Olist, disponível em:

https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

## Como usar

O notebook foi desenvolvido para ser executado no Google Colab. Para abrir o notebook no Colab, acesse o repositório no GitHub e use o link de visualização do notebook Python:

https://github.com/evaldopm/tech-challenge-olist-insights

No Google Drive, crie a estrutura de pastas a partir da raiz do seu drive pessoal:

`/1AIAT/Tech_Challange/FASE1/archive/`

No Colab, `/content/drive/` é o ponto de montagem do Google Drive e `MyDrive` representa o seu drive pessoal. Portanto, o caminho usado no notebook é:

`/content/drive/MyDrive/1AIAT/Tech_Challange/FASE1/archive/`

Os arquivos carregados no notebook são:

- `olist_customers_dataset.csv`
- `olist_geolocation_dataset.csv`
- `olist_order_items_dataset.csv`
- `olist_order_payments_dataset.csv`
- `olist_order_reviews_dataset.csv`
- `olist_orders_dataset.csv`
- `olist_products_dataset.csv`
- `olist_sellers_dataset.csv`
- `product_category_name_translation.csv`

## Instruções

1. Abra o notebook `notebooks/olist.ipynb` no Google Colab.
2. Monte o Google Drive com o comando do Colab.
3. Garanta que os arquivos estejam no diretório indicado.
4. Execute as células na ordem para carregar os dados e gerar os gráficos.

## Objetivo

Criar uma análise clara e objetiva dos dados da Olist, apoiando decisões com insights sobre categorias de produtos, volume de pedidos por estado, tipos de pagamento e outras métricas relevantes.