<h1 align="center">Criação de Métricas para Varejo</h1>

<p align="center">
 <a href="#entendimento-do-negócio">Entendimento do negócio</a> •
 <a href="#tecnologias-utilizadas">Tecnologias utilizadas</a> •
 <a href="#tratamento-dos-dados">Tratamento dos dados</a> • 
 <a href="#entendimento-dos-dados">Entendimento dos dados</a> • 
 <a href="#perguntas-de-negócio">Perguntas de negócios</a
</p>

## Entendimento do negócio
<p align="justify">
Esta é uma proposta de resolução para um case da Formação em Dados da Escola DNC. Trata-se da criação de uma série de métricas para acompanhamento de resultados de uma loja virtual que atende todo o território nacional, vendendo produtos de diferentes departamentos em diversos canais de venda.


A loja possuía 2 bases de dados:
- <div align="justify"> uma com informações das vendas, contendo informações sobre canal de venda, bandeira, data da venda, preço com e sem frete, departamento, estado e IDs de identificação de compra e cliente
- uma com informações dos clientes, contendo informações sobre idade e renda

<p align="justify">
As premissas do negócio consideradas eram que, devido a um erro do sistema, para compras sem informação de estado deveria ser considerado o estado do MS. Além disso, o preço não poderia ser maior que o preço com frete.
 
<p align="justify">
Foi solicitada a criação das métricas sobre departamentos mais vendidos, média de preço com frete por departamento, quantidade de vendas por mês, média de renda por canal de venda e média de idade de clientes por bandeira.



## Tecnologias utilizadas
- Google Colab
- Python
- Pandas
- Matplotlib

## Tratamento dos dados
Para utilizarmos as informações de maneira ideal, foi necessário fazer a manipulação das bases de dados. Destaca-se:
- Correção de valores nulos de estado e preço, nomes de colunas e tipos de dados.
- Exclusão de valores que não atendiam à premissa do negócio.
- União das bases de vendas e clientes.

## Entendimento dos dados
<p align="justify">
Foi feita a análise univariada para observar a distribuição de frequência das variáveis categóricas e a distribuição de variáveis numéricas (média, mínimo, máximo, desvio padrão), afim de procurar por padrôes ou tendências relevantes para o negócio.

## Perguntas de negócio
Para criação das métricas solicitadas, foram utilizadas técnicas de agrupamento de dados e gráficos para visualização. A partir das informações levantadas, observou-se que:
- <div align="justify"> Os departamentos mais vendidos eram todos do segmento de eletrônicos: celulares, eletrodomésticos, eletroportáteis, TVs e informática. A partir disso, podemos identificar os produtos mais populares e ajustar a estratégia de vendas.

<p align="center">
    <img width="700" height="400" src="https://github.com/viniciusendo/Metricas_Varejo/assets/134152277/b39ef6da-c14d-45f9-82c9-858678862869">
</p>

- <div align="justify"> Os departamentos com a maior média de preço por venda eram em sua maioria do segmento de eletrônicos: TVs (vídeo e acessórios), informática, linha industrial, cine e foto e celulares. A partir disso, podemos identificar os departamentos mais rentáveis e ajustar os preços de acordo com a margem de lucro. 

<p align="center">
    <img width="700" height="400" src="https://github.com/viniciusendo/Metricas_Varejo/assets/134152277/29a779cb-46b7-44d7-8a15-38e253f24c80">
</p>

- O mês com mais vendas no período avaliado (jan a abr) foi março, apesar da diferença não ser muito significativa entre os meses. A partir disso, podemos identificar sazonalidades nos períodos das compras e planejar campanhas de marketing para determinadas épocas.

<p align="center">
    <img width="560" height="320" src="https://github.com/viniciusendo/Metricas_Varejo/assets/134152277/d8bb92b6-b9b0-4e59-a23e-18ace70360c5">
</p>
 
- A média de renda por canal de venda (mobile, internet e aplicativo) é praticamente idêntica.
- De maneira similar, a média de idade por bandeira também é praticamente a mesma.
