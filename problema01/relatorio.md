# Variáveis que possuem maior influência na produção de energia

As variáveis que possuem maior influência na produção de energia são:

### AT (Ambient Temperature)
Correlação negativa de -0.95, indicando forte correlação inversamente proporcional. Ou seja, a medida que a temperatura aumenta, a produção de energia cai, e vice versa.

### V (Exhaust Vacuum)
Correlação negativa de -0.87, indicando forte correlação inversamente proporcional. Ou seja, a medida que a temperatura aumenta, a produção de energia cai, e vice versa.

# Correlação entre as variáveis independentes
As variáveis AT (Ambient Temperature) e V (Exhaust Vacuum) possuem alta correlação positiva diretamente proporcional, um indicativo de multicolinearidade.

# Modelo é adequado para a previsão?

Sim, o modelo é adequado para previsão de produção de energia, pois:

O R² mostra que 93% da variação de produção energética pode ser explicada pela variação das features.

O RMSE indica que a distância das previsões com a realidade é de apenas 4.50 MegaWatts, número baixo quando posto ao lado de PE que varia de 420 a 495 MW

O MAE indica que a média de erro por previsão é de 3.59 MW, valor baixo comparado à escala de 420 a 495 MW da PE.