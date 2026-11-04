# Balanceamento entre classes

O cojunto de dados esta desbalanceado, havendo 700 amostras da classe 'good', e 300 da classe 'bad'. Dessa forma, a acurácia se torna uma métrica inéficaz, pois, ela trata erros de falso positivo e erros de falso negativo como igualmente ruins, o que é problemático em alguns cenários, como o de classificação de risco de crédico, onde deixar passar um cliente mal pagador normalmente será mais prejudicial do que gerar um alarme falso sobre o cliente bom pagador. Caso o modelo faça uma previsão errônea que todos os clientes são bons pagadores, o modelo terá uma taxa de acerto de 70% dos casos, o que pareceria aceitável de primeiro momento, mas, na prática, créditos seriam liberados para os 30% que não são bons pagadores.

# Normalização de atributos

A normalização de atributos não é necessária porque a escala de valores não irá influenciar o modelo a considerar uma feature mais importante que outra, uma vez que a construção da árvore se dará por meio de comparações do tipo "se-então". Dessa forma, features serão comparadas de maneira isolada com o limiar de decisão, sem influência de outras features, independentemente de sua escala de valores. 

# Análise de profundidade

A profundidade com maior desempenho é a profundidade 7.

Em profundidas muito baixas, como nas profundidades 2 e 3, o modelo apresenta acurácia baixa tanto na validação quanto no treino, indicando underfitting, isso é, o modelo não consegue aprender o suficiente para fazer generalizações.

Em profundidades muito altas, o modelo sofre de overfitting, o que pode ser observado no fato de que, no desempenho de acuráciade treino, quanto maior a profundidade, maior a acurácia do modelo. Porém, ao mesmo tempo, a acurácia da validação cai, como se pode observar da profunidade 10 até a sem limite, indicando que o modelo não aprendeu de modo a fazer generalizações, e sim, de modo a decorar os dados de treino, por isso o ótimo desempenho no mesmo, e o desempenho em queda brusca na validação em relação ao mesmo nível de profundidade.

# Gini vs Entropia

Sim, houve diferença relevante. Utilizando o critério de gini, a acurácia da validação se manteve estável até a profundidade 10. Já utilizando o critério da entropia, a acurácia da validação já começou a cair após a profundidade 5, indicando overfitting ainda mais cedo. Isso ocorre porque o cálculo logarítmico da entropia pune a impureza de forma mais severa, fragmentando ainda mais os dados em profundidade menores que a de gini.

# Atributos mais importantes para a classificação

Attribute1 (Status of existing checking account), Attribute5 (Credit amount) e Attribute2 (Duration in month)

# Caminho até nó folha com maior número de amostras de mau risco

Attribute1 deve ser maior que 0.5, attribute2 deve ser maior que 11.5. attribute 6 deve ser maior que 0.5, attribute5 deve ser menor ou igual a 8015.5, attribute 6 deve ser menor ou igual a 3.5, attribute 3 deve ser menor ou igual a 2.5, e attribute2 deve ser maior ou igual a 15.5

# Análise de métricas

O erro mais frequente cometido pelo modelo é o de classificar um bom pagador como mau pagador, sendo esse o erro mais grave por ocasionar em recusas indevidas de crédito e perda de receita para a instituição.

Eu ajustaria o limiar de decisão, diminuindo-o para facilitar a classificação dos clientes como bons pagadores. Dessa forma, buscaria reduzir a quantidade de bons pagadores classificados incorretamente como maus pagadores, embora isso pudesse aumentar a quantidade de maus pagadores classificados como bons.