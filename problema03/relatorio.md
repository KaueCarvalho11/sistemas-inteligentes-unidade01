# Justificativa da normalização

Normalização se faz necessária para evitar que o modelo considere algumas features mais relevantes que outras pela diferença do seu intervalo de valores, evitando que features com valores mais altos sejam consideradas mais relevantes que as restantes.

# Interpretação sobre valores de k

Para valores muito baixos de k, de maneira geral, o modelo fica sensível a ruídos, isso é, novo vinho inserido pode ter classificação prejudicada pela presença de dado errôneo, possibilitanto que ele também seja classificado de maneira errada. No caso específico do modelo, para valores muito baixos, em k=1 o modelo obteve sua maior acurácia, seguido de uma queda de acurácia k = 3.

Para valores muito altos de k, há o risco do modelo englobar em sua avaliação para classificação classes mais distantes que não representem as caracteristicas daquela instância nova de vinho, a depender da densidade dos dados em cada região. No modelo, para valores muito altos, como em k = 11, o modelo teve acurácia menor do que k = 1, porém, maior que k = 3, k = 5 e k = 7.

# Frequência de erros

Em termos de volume absoluto, o modelo erra com maior frequência na fronteira entre as classes medio e ruim, acumulando 264 diagnósticos trocados entre si. No entanto, ao analisarmos o desempenho proporcional, a classe Bom é a que apresenta a maior taxa de falha do modelo: a máquina erra o diagnóstico em 50% das vezes ao tentar identificar os vinhos da categoria Bom, rebaixando metade deles para a categoria medio.