# Copilot Instructions for Olist Insights

## Objetivo
Fornecer ao GitHub Copilot instruções claras sobre o dataset Olist, suas tabelas principais, relacionamentos e metas estratégicas da empresa.

## Contexto do projeto
Este repositório contém um notebook Python de análise exploratória para o conjunto de dados Brazilian E-Commerce Public Dataset da Olist.
O notebook foi originalmente pensado para execução no Google Colab, mas também pode ser usado localmente no VS Code.

## Arquivo de esquema
Utilize o arquivo de imagem `assets/data_set_schemas.png` para entender e explicar as ligações de chave entre as tabelas.

### Relações principais no schema
- `olist_orders_dataset` é a tabela central do modelo.
- `olist_orders_dataset.order_id` relaciona-se com:
  - `olist_order_payments_dataset.order_id`
  - `olist_order_reviews_dataset.order_id`
  - `olist_order_items_dataset.order_id`
- `olist_order_items_dataset` explora detalhes de itens e liga-se a:
  - `olist_products_dataset.product_id`
  - `olist_sellers_dataset.seller_id`
- `olist_orders_dataset.customer_id` relaciona-se com:
  - `olist_order_customer_dataset.customer_id`
- Tanto `olist_order_customer_dataset` quanto `olist_sellers_dataset` compartilham informações geográficas baseadas em `zip_code_prefix` com:
  - `olist_geolocation_dataset.zip_code_prefix`

Isso significa que os dados de clientes, vendedores e geolocalização podem ser cruzados para entender comportamento, rotas e desempenho logístico.

## Informações do Dataset
O dataset inclui informações relacionadas a:
- Clientes
- Pedidos
- Pagamentos
- Produtos
- Logística
- Vendedores
- Avaliações
- Geolocalização

## Principais tabelas disponíveis
1. `customers`: dados de clientes e localização.
2. `orders`: pedidos e status operacionais.
3. `order_items`: itens comprados, preços e fretes.
4. `payments`: informações de pagamento.
5. `order_reviews`: avaliações e comentários.
6. `products`: informações de produtos.
7. `sellers`: dados dos vendedores.
8. `geolocation`: dados geográficos.

## Avaliação das fontes de dados
A Olist deseja iniciar sua jornada de transformação utilizando Inteligência Artificial Generativa e Agentes de IA.
O foco deve ser em identificar oportunidades de melhoria em:
- Experiência do cliente
- Eficiência logística
- Retenção e fidelização
- Análise de reviews
- Eficiência operacional
- Automação de processos
- Apoio à tomada de decisão
- Escalabilidade operacional

## Como usar este guia
- Ao gerar recomendações ou insights, priorize os relacionamentos entre pedidos, clientes, produtos, reviews e geolocalização.
- Use o esquema visual em `assets/data_set_schemas.png` para explicar como os dados se conectam.
- Destaque como cada tabela pode contribuir para responder desafios de negócios da Olist.
- Considere que o notebook foi pensado para Colab, mas o foco do uso do Copilot deve ser a estrutura do dado e as análises que podem ser feitas a partir desse modelo.

## Nota adicional sobre execução local
No ambiente local, o caminho dos dados pode variar. Se o usuário estiver no Colab, o caminho esperado é:
`/content/drive/MyDrive/1AIAT/Tech_Challange/FASE1/archive/`

---

### Resumo para o Copilot
Use este documento como referência rápida:
- O dataset é uma fonte relacional centrada em pedidos.
- A tabela `orders` é o nó principal.
- Dados de pagamento, avaliação e itens estão diretamente ligados a um pedido.
- Produtos e vendedores são consultados a partir dos itens do pedido.
- Geolocalização conecta clientes e vendedores por CEP.
- O objetivo final é apoiar uma transformação de IA em experiência, logística e processos.
