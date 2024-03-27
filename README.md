# Previsão de preços da cesta básica
![image](https://github.com/Andressaach/Previs-o-de-pre-os-da-cesta-b-sicata-b-siza/assets/100172009/29f0c90d-70d4-448c-9b1f-201964b2e305)

# 1. Descrição
- Este projeto investiga e compara o desempenho de diferentes modelos aplicados a séries temporais para previsão de preços da cesta básica alimentícia.
  
- Três abordagens foram consideradas: modelagem para séries temporais ARIMA, técnicas de machine learning com o algoritmo XGBoost e inteligência artificial com o modelo TimeGPT.
  
- A análise comparativa baseou-se em métricas de desempenho, como o erro médio quadrático (MSE), utilizando dados históricos sobre os preços dos itens alimentícios da cesta básica na cidade de Francisco Beltrão, Paraná.
  
- Os resultados indicam que o modelo de inteligência artificial TimeGPT obteve o melhor desempenho, seguido pelo XGBoost.
  
- Esses achados destacam a importância de escolher a abordagem de modelagem adequada para prever os preços da cesta básica, fornecendo insights valiosos para formuladores de políticas, gestores de empresas e consumidores na região.
  
# 2. Tecnologias e ferramentas
As tecnologias e ferramentas utilizadas foram Python (Pandas, Numpy, Matplotlib, Seaborn, Statsmodels, Plotnine, Pmdarima, Xgboost, Nixtlats), Jupyter Notebook, algoritmos de regressão de aprendizado de máquina e estatística.

# 3. Objetivos do projeto

Considerando que, a previsão de preços da cesta básica é um desafio essencial para governos, empresas e consumidores, pois influencia diretamente a qualidade de vida e o planejamento financeiro das famílias, a aplicação de modelos de previsão baseados em séries temporais assume um papel crucial. Portanto, os objetivos desse projeto são:

- Realizar uma análise exploratória dos dados para identificar padrões sazonais, tendências e possíveis influências externas nos preços dos itens da cesta básica.
  
- Comparar a precisão das previsões geradas pelos modelos ARIMA, XGBoost e TimeGPT por meio de métricas de avaliação, como o erro médio quadrático (MSE).
  
- Identificar as vantagens e limitações de cada abordagem em termos de interpretabilidade, complexidade computacional e robustez das previsões.
  
# 4. Principais insights obtidos
1. O valor da cestá básica mostra uma tendência clara de aumento ao longo do tempo. No entanto, não foram observadas grandes flutuações que indicam sazonalidade para a série temporal analisada.
   
![image](https://github.com/Andressaach/Previs-o-de-pre-os-da-cesta-b-sicata-b-siza/assets/100172009/8b3d570e-e611-445a-a79b-c924a6cf54a7)

2. Apesar, de não haver sazonalidade na série temporal referente ao valor total da cesta, observamos que para alguns itens que compõem a mesma, como batata, banana e tomate há uma sazonalidade clara. Para os preços do leite, a sazonalidade é menos evidente, mas ainda é perceptível, mostrando alguma regularidade sazonal.
   
![image](https://github.com/Andressaach/Previs-o-de-pre-os-da-cesta-b-sicata-b-siza/assets/100172009/05af17fa-d506-411a-9e27-bac1b23f5645)

3. Analisando as correlações entre os preços dos produtos que compõem a cesta básica, observamos o seguinte:
   
![image](https://github.com/Andressaach/Previs-o-de-pre-os-da-cesta-b-sicata-b-siza/assets/100172009/ade498d9-1660-4962-a96f-2754113baa2b)

- Nota-se, que existe uma forte correlação positiva entre o preço do arroz e do feijão. Isso sugere que, em geral, quando o preço de um desses itens aumenta, o preço do outro também tende a aumentar.

- O mesmo pode ser observado para os itens açúcar e farinha de trigo.

- Uma correlação positiva moderada entre o preço do açúcar e o da farinha de trigo pode indicar que esses dois produtos têm movimentos de preço semelhantes ao longo do tempo.

- O preço do café e o da margarina também estão positivamente correlacionados. Isso pode ser devido a fatores como a demanda por produtos de café da manhã.

- Há também, uma correlação positiva entre o preço da carne e o do leite. Isso pode ser explicado pela relação entre esses produtos na dieta básica.

- O preço do tomate e o da batata também estão correlacionados positivamente, sugerindo uma relação quanto à sazonalidade desses produtos.

- Há uma correlação positiva entre o preço da banana e o do pão. Isso pode ser devido à preferência dos consumidores por esses itens como lanches rápidos e acessíveis.

# 5. Avaliação dos modelos
Nesta seção, será realizada uma avaliação comparativa dos modelos ARIMA, XGBoost e TimeGPT na previsão do valor da cesta básica com base em séries temporais.

![image](https://github.com/Andressaach/Previs-o-de-pre-os-da-cesta-b-sicata-b-siza/assets/100172009/0a53fc87-7b5e-4ad4-a8b0-3aba2e8d3127)

Analisando as previsões obtidas pelo modelo ARIMA, observamos que o modelo não obteve boa capacidade para capturar padrões e tendências para a amostra utilizada, dada as diferenças entre as previsões (representadas pela linha azul) e os valores reais da variável de interesse

![image](https://github.com/Andressaach/Previs-o-de-pre-os-da-cesta-b-sicata-b-siza/assets/100172009/02e10e47-59a2-4699-a76c-1675d5c928c1)

Já para as previsões realizadas pelo modelo XGBoost, observamos que o modelo foi capaz de capturar padrões e tendências para a série temporal analisada. Através da análise gráfica, podemos dizer que os erros das previsões foram menores para o modelo XGBoost em relação ao modelo ARIMA.

![image](https://github.com/Andressaach/Previs-o-de-pre-os-da-cesta-b-sicata-b-siza/assets/100172009/d950b89a-14cb-40c4-8e09-fa12654bfae1)
Por fim, as previsões geradas pelo modelo TimeGPT para o valor da cesta básica, também demonstrou uma boa capacidade de capturar padrões e tendências, nas previsões realizadas para o período testado, assim como o modelo XGBoost.

No entanto precisamos avaliar o desempenho dos modelos a partir de uma métrica universal que permita uma comparação objetiva entre os diferentes modelos, e seja capaz de refletir a qualidade das previsões de cada um deles. Uma dessas análises amplamente utilizadas é o erro médio quadrático (MSE), ele calcula a média dos quadrados dos erros entre os valores previstos e os valores observados. Um MSE menor indica um melhor ajuste do modelo aos dados observados.

![image](https://github.com/Andressaach/Previs-o-de-pre-os-da-cesta-b-sicata-b-siza/assets/100172009/7f99b83a-306f-413e-ba03-17dc9e182abb)
Analisando o gráfico de comparação de desempenho dos modelos, baseado na métrica de desempenho MSE. Podemos dizer que o modelo que obteve o melhor desempenho foi o modelo de inteligência artificial TimeGPT, uma vez que apresentou o menor erro quadrático médio (63.13). O modelo que apresentou a segunda melhor precisão foi o modelo de machine learning XGBoost, com um MSE de 123.98, seguido do modelo de passeio aleatório sazonal (166.21). E por fim, o ARIMA que foi o menos preciso entre os modelos testados, com uma MSE de 372.24. Sendo assim, podemos concluir que o modelo de inteligência artificial TimeGPT é mais preciso para prever o valor da cesta básica para a amostra selecionada em comparação com os outros modelos avaliados.

# 6. Considerações Finais
Durante o processo de análise, foram identificadas vantagens e limitações de cada abordagem. Enquanto os modelos ARIMA são reconhecidos por sua capacidade de capturar padrões temporais em séries históricas de dados, eles podem ser limitados em sua capacidade de lidar com complexidades e nuances nos dados. Por outro lado, técnicas de machine learning, como o XGBoost, oferecem uma abordagem mais flexível, mas podem exigir mais dados e processamento computacional. Já a inteligência artificial, representada pelo TimeGPT, mostrou-se capaz de explorar relações temporais mais complexas e capturar nuances sutis nos dados, oferecendo previsões mais precisas e confiáveis.

# 7. Entre em contato comigo
Linkedin: https://www.linkedin.com/in/andressa-carla-henrique-69699919a/

Github: https://github.com/Andressaach

Gmail: andressaach@gmail.com
