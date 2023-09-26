<h1 align="center">DCN - Case Varejo</h1>

<p align="center">
 <a href="#entendimento-do-negócio">Entendimento do negócio</a> •
 <a href="#tratamento-dos-dados">Tratamento dos dados</a> • 
 <a href="#entendimento-dos-dados">Entendimento dos dados</a> • 
 <a href="#perguntas-de-negócio">Perguntas de negócios</a> •  
 <a href="#tecnologias-utilizadas">Tecnologias utilizadas</a
</p>

## Entendimento do negócio

Esta é uma proposta de resolução para um case da Formação em Dados da Escola DNC. Trata-se da criação de uma série de métricas para acompanhamento de resultados de uma loja de varejo.

A loja possuía 2 bases de dados:
- uma com informações das vendas, contendo informações sobre canal de venda, bandeira, data da venda, preço com e sem frete, departamento, estado e IDs de identificação de compra e cliente
- uma com informações dos clientes, contendo informações sobre idade e renda.

Foram solicitadas métricas sobre departamentos mais vendidos, média de preço com frete por departamento, quantidade de vendas por mês, média de renda por canal de venda e média de idade de clientes por bandeira.

As premissas do negócio eram que, devido á um erro do sistema, para compras sem informação de estado deveria ser considerado o estado do MS. Além disso, o preço não poderia ser maior que o preço com frete.

## Tratamento dos dados
Para utilizarmos as informações de maneira ideal, foi necessário fazer a manipulação das bases de dados. Destaca-se:
- Correção de valores nulos de estado e preço, nomes de colunas e tipos de dados
- Exclusão de valores que não atendiam à premissa do negócio
- União das bases de vendas e clientes

## Entendimento dos dados
Foi feita a análise univariada para observar a distribuição de frequência das variáveis categóricas e a distribuição de variáveis numéricas (mín, máx, desvio padrão), afim de procurar por padrôes ou tendências relevantes para o negócio.

## Perguntas de negócio
Para criação das métricas solicitadas, foram utilizadas técnicas de agrupamento de dados e gráficos para visualização. A partir das informações levantadas, observou-se que:
- Os departamentos mais vendidos eram todos do segmento de eletrônicos: celulares, eletrodomésticos, eletroportáteis, TVs e informática
- Os departamentos com a maior média de preço por venda eram em sua maioria do segmento de eletrônicos: TVs (vídeo e acessórios), informática, linha industrial, cine e foto e celulares
- O mês com mais vendas no período avaliado (jan a abr) foi março, apesar da diferença não ser muito significativa entre os meses
- A média de renda por canal de venda (mobile, internet e aplicativo) é praticamente idêntica
- De maneira similar, a média de idade por bandeira também é praticamente a mesma.

## Tecnologias utilizadas
- Google Colab
- Python
- Pandas
- Matplotlib
