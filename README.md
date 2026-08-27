# LH Nautical — Desafio Lighthouse

Projeto desenvolvido como parte do **Desafio Lighthouse**, da Indicium AI, com foco na análise de dados de uma operação comercial do segmento náutico.

O projeto reúne um notebook de análise exploratória, modelagem das relações entre tabelas, carregamento de dados, análise de vendas e clientes, previsão de demanda e recomendação de produtos.

> Desenvolvido por **Italo Marcony Souza Silva**.

## Objetivos

- Explorar e compreender as principais tabelas do banco de dados.
- Avaliar a qualidade, a estrutura e a consistência dos dados.
- Analisar vendas, clientes, produtos e categorias.
- Identificar padrões de faturamento e comportamento de compra.
- Criar uma previsão simples de demanda.
- Desenvolver uma recomendação de produtos baseada em similaridade.
- Gerar análises que possam apoiar decisões comerciais.

## Estrutura dos dados

O projeto utiliza seis arquivos CSV principais:

| Arquivo | Descrição | Registros |
|---|---|---:|
| `orders.csv` | Pedidos realizados, canais, clientes, status e valores | 48.998 |
| `order_items.csv` | Itens presentes em cada pedido | 147.320 |
| `products.csv` | Cadastro de produtos | 500 |
| `product_variants.csv` | Variações dos produtos | 1.009 |
| `customers.csv` | Cadastro e informações dos clientes | 2.000 |
| `categories.csv` | Categorias de produtos | 14 |

Os dados abrangem pedidos registrados entre **2020 e 2026**, permitindo análises temporais, comerciais e de comportamento dos clientes.

## Análises realizadas

### 1. Análise exploratória de dados

- Visualização inicial das tabelas.
- Verificação de dimensões e tipos de dados.
- Estatísticas descritivas.
- Conversão e análise de colunas de data.
- Identificação de valores nulos em colunas importantes.
- Avaliação da distribuição dos valores dos pedidos.

### 2. Estrutura e relacionamentos

Foram avaliados os relacionamentos entre pedidos, itens, produtos, clientes, categorias e variações. Essa etapa permite combinar as tabelas para construir métricas de vendas, produtos mais relevantes e perfil de consumo dos clientes.

### 3. Análise de vendas

Foram calculadas métricas como:

- Faturamento total.
- Quantidade de pedidos e itens vendidos.
- Ticket médio.
- Receita por categoria.
- Receita por produto.
- Desempenho por canal de venda.
- Distribuição das vendas por dia da semana.
- Evolução mensal das vendas.
- Relação entre custo, receita e resultado aproximado por produto.

### 4. Análise de clientes

A análise de clientes considera, entre outros indicadores:

- Faturamento acumulado por cliente.
- Frequência de compras.
- Ticket médio.
- Diversidade de categorias adquiridas.
- Ranking de clientes por valor movimentado.

Essas métricas ajudam a identificar clientes de maior valor e oportunidades de segmentação comercial.

### 5. Previsão de demanda

Foi criada uma previsão inicial da quantidade de pedidos para os meses seguintes, utilizando o histórico mensal disponível e uma abordagem simples baseada na média móvel.

A previsão serve como referência exploratória e pode ser aprimorada futuramente com modelos estatísticos ou de machine learning, incluindo variáveis sazonais, canais, categorias e comportamento histórico.

### 6. Recomendação de produtos

Foi implementado um mecanismo de recomendação baseado em similaridade por cosseno. A abordagem utiliza características dos produtos para encontrar itens semelhantes e sugerir alternativas relacionadas.

Exemplo de aplicação:

> Dado um produto consultado, o sistema retorna outros produtos com maior similaridade, apoiando estratégias de venda cruzada e recomendação personalizada.

## Tecnologias utilizadas

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Como executar

### Executando no Google Colab

1. Abra o notebook no Google Colab. (https://colab.research.google.com/drive/1GEHc9NpfisJJbUjJr-OrApCw0l8UEm3T?usp=sharing)
2. Faça o upload dos arquivos CSV necessários.
3. Execute as células em ordem.
4. Verifique as tabelas, métricas e visualizações geradas.

### Executando localmente

Clone o repositório:

```bash
git clone https://github.com/italomarcony/desafio_lh_nautical
cd desafio_lh_nautical
```

Crie e ative um ambiente virtual:

```bash
python -m venv .venv
```

No Windows:

```bash
.venv\Scripts\activate
```

No Linux ou macOS:

```bash
source .venv/bin/activate
```

Instale as dependências:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

Inicie o Jupyter Notebook:

```bash
jupyter notebook
```

Depois, abra o arquivo:

```text
lh_nautical_desafio_indicium.ipynb
```

Certifique-se de que os arquivos CSV estejam no mesmo diretório do notebook ou ajuste os caminhos utilizados nas células de leitura.

## Notebook no Google Colab

Caso o notebook não seja renderizado corretamente no GitHub ou algum gráfico não seja exibido, acesse a versão no Google Colab:

[ abrir notebook no Google Colab ](https://colab.research.google.com/drive/1GEHc9NpfisJJbUjJr-OrApCw0l8UEm3T?usp=sharing)

## Observações

- Os resultados dependem dos arquivos CSV utilizados na execução.
- O notebook contém células comentadas e resultados de análises exploratórias.
- A previsão de demanda é uma abordagem inicial, não um modelo definitivo de produção.
- As recomendações dependem das características e do tratamento aplicado aos dados dos produtos.
- Para uso em produção, seria necessário adicionar validações, tratamento de erros, controle de versões dos dados e monitoramento dos resultados.

## Autor

**Italo Marcony Souza Silva**
