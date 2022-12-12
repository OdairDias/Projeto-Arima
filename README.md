# Modelo-preditivo- preço-ações--montecarlo
## objetivos: 
Objetivo do projeto foi tentar prever o preço futuro da ações da empresa Petrobras utilizando o modelo de monte carlo.
### O que é Simulação de Monte Carlo?
A Simulação de Monte Carlo, também conhecida como Método de Monte Carlo ou uma simulação de probabilidade múltipla, é uma técnica matemática, que é usada para estimar os possíveis resultados de um evento incerto. O Método de Monte Carlo foi inventado por John von Neumann e Stanislaw Ulam durante a Segunda Guerra Mundial para melhorar a tomada de decisão em condições incertas
### Pra que serve??
As Simulações de Monte Carlo avaliavam o impacto do risco em muitos cenários da vida real, como inteligência artificial, preços de ações, previsão de vendas, gerenciamento de projetos e precificação.
### Como ela funciona? 
Diferente de um modelo de previsão normal, a Simulação de Monte Carlo prevê um conjunto de resultados com base em um intervalo de valores estimados em relação a um conjunto de valores de entrada fixos. Em outras palavras, uma Simulação de Monte Carlo cria um modelo de resultados possíveis, usando uma distribuição de probabilidade, como uma distribuição uniforme ou normal, para qualquer variável que tenha incerteza inerente. Ela, então, recalculará os resultados sucessivamente, cada vez usando um conjunto diferente de números aleatórios entre os valores mínimo e máximo. Em um teste típico de Monte Carlo, este exercício pode ser repetido milhares de vezes para produzir um grande número de resultados prováveis. As simulações de Monte Carlo também são utilizadas para previsões de longo prazo devido à sua precisão.
### Porque usar este modelo? 
O modelo de monte carlo se mostra muito efetivo no cálculo do preço de ações uma vez que adiciona aleatoriedade como elemento fundamental para predição, os preços das ações possuem uma acentuada tendência a alatoriedade.

## Porque analisar as ações da Petrobras? 
Um dos motivos é que as ações da Petrobras no Brasil é quem tem maior volume de negociação tanto por dia quanto mês ou seja, representa o sentimento da maior quantidade de players do mercado, o segundo motivo, ela é uma empresa estatal ou seja, representa uma parte do sentimento do mercado em relação aos rumos que o governo está dando a economia e o terceiro motivo, ela representa o setor petrolífero, retira petróleo e exporta porém não refina, então temos que importar de outros países, sendo o valor de importações  baseado nos preços internacionais, que são calculados em dólar. Isso quer dizer que podemos medir o sentimento interno dos  grandes players, como eles  estão enxergando a política pública dentro do país, como também temos um termômetro externo, internacional sobre como estão as coisas pelo mundo, são estes o motivo de se analisar as ações da Petrobrás.   

## Análise
Começamos importando os dados, aqui podemos ver o comportamento dos dados no período de  12/12/2021 a 12/12/2022 este será o período análisado

![image](https://user-images.githubusercontent.com/117185803/207122847-90597a2a-66ae-4be9-8be6-62412cb86644.png)

Aqui estamos constrindo uma variável chamda variação diaria com base no fechamento do dia anterior, iremos usar esa informação no nosso modelo
![variação diaria](https://user-images.githubusercontent.com/117185803/207123951-6956b1f4-79e6-4390-8f41-6db2e1d26dbf.png)

Pegamos os dados, aplicamos uma função de log a fim de suavizar o modelo
![image](https://user-images.githubusercontent.com/117185803/207124260-dea893ac-c9d4-4037-b2fb-85d38f91c132.png)

Por fim geramos as simulções de monte carlo com previsão de noventa dias e com simulção de três mil cenários diferentes usando como base nosso ultimo preço de fechamento 23.46 

![simulação monte carlo](https://user-images.githubusercontent.com/117185803/207125220-9293ebbe-a650-4f0b-8d60-290add9329fe.png)

## Resultados

  Tivemos como resultado uma projeção para os próximos noventa dias a contar do dia 12/12/2022. Sendo a linha laranja a projeção criada e a linha pontilhada a margem de erro estipulada no modelo.
  ### Fatos relevantes 
  Vale ressaltar que apesar do modelo já ser alimentado com certa dose de aleatoriedade, devemos levar em consideração nosso cenário macro econômico e global. Estamos passando por um momento de certa incerteza dentro do mercado, pautada principalmente pelo setor político, além disso temos um dos principais produtores de petróleo do mundo no meio de uma guerra o que impede a exportação deste produto para o resto do mundo, sendo a Europa principalmente afetada pois possui um inverno rigoroso e tem nos combustíveis fosseis a principal fonte de aquecimento e o principal, possui forte dependência do combustível Russo, país que está em guerra e sofrendo sanções internacionais sem poder exportar seu combustível. Estamos diante de uma eminente falta do produto no mercado global e isso deve pressionar os preços das comodities pra cima, fato que já ocorreu este ano tendo o governo que intervir, porém o subsidio concedido aos combustíveis acaba no fim deste ano de 2022. Além disso ainda temos os principais países do mundo a beira de uma forte resseção fruto da injeção de dinheiro nas economias para enfrentar a crise do covid-19, ou seja, estamos com o cenário de uma incerteza política, uma provável falta de combustíveis no mercado internacional seguido de uma recessão global.
  
![image](https://user-images.githubusercontent.com/117185803/207127787-7b20f4b3-45b4-4d10-90fa-fd50adba6537.png)

