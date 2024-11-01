# paic_serie_temporal
# Título: Uso de séries temporais para a previsão de preços de ações no mercado financeiro.
Repositório para guardar as versões feitas no ambiente collab e explicação sobre o projeto de iniciação científica na universidade.

## Sumário:
1. Introdução.
2. Objetivos.
3. Metodologia
4. Explicação dos Resultados.
5. Referências.
  
## Introdução:
  <p>O mercado financeiro é um espaço que se refere a um conjunto de instituições, instrumentos e atividades que permite a compra e venda de ativos financeiros como ações, títulos, moedas e commodities [1]. Ele desempenha um papel fundamental na economia global permitindo que empresas, governos e indivíduos levantem capitais, gerenciem riscos e alcancem seus objetivos financeiros [2]. Vale ressaltar que esse ativo não é de renda fixa, mas de renda variável, isto porque há uma volatividade em seus preços fazendo com que o ganho e a perda obtidos sejam maiores, é por causa disso que o perfil dos compradores é arrojado para lidar com essas variações e obter rentabilidades mais seguras [8,9]. Um dos pontos para torna-los atraentes para os investidores é a mudança da taxa SELIC. A diminuição dessa taxa faz com que a operação na bolsa de valores seja mais atraente, visto que o crédito fica mais barato e ativos de renda fixa perdem preferência diante das ações da bolsa de valores [3]. Um dos ativos citados que é muito conhecido são as ações, elas são partes de uma empresa que decidiu se abrir para o mercado, dando oportunidade a terceiros virarem sócios dela e, quando são adquiridas, tornam-se acionistas, onde essas operações devem ser efetuadas pelas instituições registradas pela CVM (Conselho de Valores Mobiliários) [4,8]. A obtenção de ações pode ser feitas através das bolsas de valores, podendo ser usada corretoras pra isso, e o preço delas varia conforme o momento da empresa, flutuação do mercado e fatores externos. Ademais, existem dois tipos de ações que são as ordinárias e as preferenciais [4].</p>
	<p>As Ordinárias representam a propriedade de uma empresa e os detentores delas possuem poder de decisão em relação a questões da empresa, já que os acionistas dessas ações fazem parte de uma assembleia de acionista da companhia. As preferenciais não dão direito a votos nas assembleias, mas dão recebimento de dividendos e reembolso em caso de liquidação da empresa, consequentemente recebendo maior parcela de lucro em comparação com as ordinárias [4].</p>
	<p>Em virtude disso existem técnicas que ajudam o investidor a se sobresair dentro desse cenário como o Day Trade que é a compra e venda de papeis no mesmo dia usando a estratégia de análise técnica e gerenciamento de risco e o Swing Trade que é a compra e venda de papeis de curto e médio prazo, podendo durar dias ou semanas. Entretanto, requer paciência para pegar as ideias porque não são fáceis de usar [7].</p>
	<p>Na área de tecnologia, Outra técnica que pode ajudar no mercado finaceiro é a Série Temporal.  Elas são uma maneira de organizar informações quantitativas no tempo de um momento específico [6]. É uma importante área para estudar valores estacionários, ou seja, dados que se alteram ao longo do tempo de uma variável de interesse, ademais pode representar várias variáveis como preço de ações, previsão meterológica, vendas de produtos, estimação de produtos industriais, etc [11]. Ela é usada para modelar ou prever comportamentos futuros usando dados históricos e para isso se usa análise estatística e séries temporais para poder identificar padrões sazonais, tendências, ciclos e flutuações nos dados para assim atingir objetivos [5, 10]. Outro meio que é bastante usado são as Redes Neurais Recorrentes (RNN) que é uma estrutura que se assemelha a um cérebro humano, ou seja, acabada imitando o funcionamento do sistema nervoso e o treinamento desse modelo acaba sendo análogo ao aprendizado humano podendo atingir bom desempenho pela conexão entre os elementos computacionais simples [11] e junto com as Séries Temporais a criação de um modelo de previsão de preços de preços acaba sendo muito preciso.</p>
	<p>Em virtude disso, podem-se usar séries temporais para poder prever futuros preços das ações no mercado financeiro.</p>

## Objetivos 
 O objetivo deste projeto é usar métodos de séries temporais, modelos de ML, para realizar a predição de preço das ações utilizando datasets com preços de compra e venda desses ativos e realizar uma análise comparativa verificando quais foram os melhores parâmetros e identificar qual modelo se saiu melhor para cada cenário.
 
## Metodologia:
 Os modelos utilizados variaram dos clássicos para os híbridos e depois do resultado 1 foram utilizados apenas 2 dos anteriores e mais 2 novos modelos criados pela literatura. Os modelos clássicos usados no projeto foram:
 - ARIMA:
 - SARIMA:
 - Holt-Winters:
 - MLP:
 - LSTM:
 - GRU:
 - Tranformers:
 - TimeGPT: 
 - AutoGluon:

 A API do site Yahoo! Finance é utilizada para a extração das 6 ações sendo: Banco do Brasil, TAESA, Copasa, Magazine Luiza, Totvs e o Índice Ibovespa. De cada uma foi considerada a variável Close (Fechamento) como a variável alvo. 
 O pré-processamento deveu-se a preparar os dados em janelas de cenário 5, 15, 25 e 35 dias para a previsão de 1 dia e utilizando a abordagem de previsão iterativa é possível prever x dias, mas nesse projeto foi considerado também prever 5, 15, 25 e 35 dias no futuro. Além disso, foi testado os dados no seu formato absoluto (sem nenhum tipo de tratamento) e formato diferenciado (valor atual - valor anterior).
 As métricas utilizadas no projeto foram: MSE, RMSE, MAE, MAPE e R². 
 
## Resultados:
Considerando o resultado 4 do projeto (São muitos resultados para esse resumo) usando os modelos GRU, Transformers, AutoGluon e TimeGPT e a métrica R². A primeira tabela refere-se aos dados absolutos: 

| Modelos     | 5 dias | 15 dias | 25 dias | 35 dias |
|-------------|--------|---------|---------|---------|
| GRU         | -104.847% | -31.474% | 19.622% | -10.913% |
| Transformers| -43.164% | -120.615% | -142.007% | -32.125% |
| TimeGPT     | -146.690% | -334.250% | -255.235% | -119.567% |
| AutoGluon   | -796.979% | -312.937% | -230.232%|  -206.907% |


## Referências: 
- [1]	https://www.parmais.com.br/blog/o-que-e-mercado-financeiro/
- [2]	Prochnow, Fabio Alberto; Barone, Dante Augusto Couto, Oliveira, Luiz Otávio Vilas Bôas. Programação genêtica para predição de séries temporais aplicados a mercadso financeiros (2013).
- [3]	Oliveira, Guilherme Albertini de; Rodrigues, Paulo Sérgio Silva. Predição do mercado financeiro com uma arquitetura de extração de contexto baseada em decomposição de series temporal.
- [4]	Ianda, Tito Francisco; Perlin, Marcelo Scherer. Mercado de ações: um estudo da diferença de preçoes entre ações ordinárias e preferenciais no Brasil.
- [5]	Oliveira, Pedro Carvalho de. Séries Temporais: Analisar o Passado, Predizer o Futuro.
- [6]	Cardoso, Maria Regina Alves; Antunes, José Leopoldo Ferreira. Uso da análise de séries temporais em estudos epidemiológicos.
- [7]	Guia do Day Trade: como comprar e vender ações no mesmo dia - InfoMoney
- [8]	Ações são investimentos de renda fixa ou renda variável? - Fala, Nubank
- [9]	Qual o seu Perfil de Investidor? Entenda o que é e Descubra o seu! (mobills.com.br)
- [10]	https://statplace.com.br/blog/caracteristicas-das-series-temporais/
- [11]	Furtuoso, Gabriel Dilly Vieira; Santos, Marcos dos; Quintal, Renato Santiago. APLICAÇÃO DE REDES NEURAIS RECORRENTES NA PREVISÃO DE SÉRIES TEMPORAIS: UM ESTUDO DE PREÇOS DE AÇÕES DA BOLSA DE VALORES (2022).
