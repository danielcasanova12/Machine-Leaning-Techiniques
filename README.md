
## K-Nearest Neighbor (KNN) (k vizinhos mais próximos)
Seu objetivo é após termos os dados classificados(Dados de treino) quando inserimos o dado que queremos saber a qual grupo ele pertence temos que mandar o dado e o k (k significa o número de  vizinhos que o novo dado está mais próximo) ele vai calcular a distância do novo ponto inserido para todos os outros pontos e vai guardar este cálculo após isso ele vai pegar as k menores distancia e vai colocar o dado na classe predominante.Quanto menor o k estamos mais sujeitos a ruídos mas perdemos um pouco da precisão para encontrar um k bom devemos fazer varios teste para ver se o modelo está se comportando melhor ou se o algoritmo está se saindo mal com o k maior.
Para o algoritmo do knn funcionar perfeitamente precisamos normalizar os dados.

Ex:Se  tiver k=3 e as classes da cor vermelha e azul ele ele vai calcular a distância do novo ponto para todos os dados das classes e logo após este cálculo ele vai verificar quais são os 3 dados com a menor distância dele e vai verificar qual tem maior predominância se deste 3 dados forem 2 do vermelho então o novo ponto vai ir para a classe vermelha.

Código exemplo usando KNN:


![KNN](https://github.com/danielcasanova12/Machine-Leaning-Techiniques/assets/119464431/f2f892f7-16ac-452c-b490-d9e7e542ed91)
Nossa acurácia foi maior que 0.9 isso quer dizer que nosso modelo treinado com o algoritmo knn está gerando previsões corretas para 96,49% dos exemplos no conjunto de testes

## Principal Component Analysis (PCA) Análise do Componente Principal
Esta técnica é uma das mais comuns de redução de dimensionalidade, ou seja ela nos ajuda diminuir as dimensões do nosso problema, se tivermos 30 variáveis temos 30 dimensões ela reduz a quantidade de variáveis tentando preservar a variancia dos dados, resumidamente ela cria um novo sistema de variáveis que serão uma combinação linear dos eixos, elas conseguem explicar melhor os dados do que as variáveis iniciais 
![Pca](https://github.com/danielcasanova12/Predicao/assets/119464431/d7905325-dfee-4770-971d-fd777c7c6c0b)

Variancia por que cada nova variável tem  [0.84136038 0.11751808 0.03473561]

Aqui podemos perceber que o nivel de variancia da primeira variável é de 84% e a segunda de 11%
isso quer dizer que com apenas 2 variáveis

## ETL (Extract, Transform, Load)
Normalmente é usado quando não temos capacidade computacional na fonte ou no destino.Então entre a extração e o load usamos uma engine ou outro servidor para transformar os dados.

## ELT (Extract, Load, Transform)
Ao contrário do ETL ele transforma os dados no final do processo fazendo-se não necessário o uso de engines no meio do caminho.


## Q-learning (Aprendizado por reforço)

O aprendizado por reforço é o aprendizado cujo nosso agente(inteligência artificial) vai aprender com as interações com nosso ambiente ele fará ações e receberá de volta o estado e uma recompensa que pode ser negativa ou positiva, ele aprende com seus erros e acertos. Este tipo de aprendizado de máquina é muito usado na robótica e também em jogos. Uma forma prática de visualizarmos isso no mundo real podemos ver como ensinamos os cachorros, normalmente começamos ensinando eles pelo básico que seria o deitar sentar e pular e depois que ele já aprendeu isso começamos com outras tarefas como buscar uma bolinha que jogamos para ele, conforme ele vai fazendo as tarefas vamos dando recompensas para ele.

## Confusion Matrix
A Confusion Matrix serve para avaliarmos nosso modelos de Classificação, ela é uma matriz quadrada com as dimensões da quantidade de variáveis ex: se tivermos 4 variáveis ela será uma matriz 4x4. Nas colunas 
![confusionMatriz](https://github.com/danielcasanova12/Predicao/assets/119464431/f2bb54cd-494f-44c7-97a5-b72d3772595d)
Nesta matriz podemos ver na diagonal em vermelho os acertos e na outra diagonal os erros.
Uma das métricas de avaliação é a acurácia que se mede com esta fórmula
 ((TP + TN)/N) = 150/165=0.91 = 91%
Temos que cuidar ao usar acurácia pois podemos ter dados desbalanceados com dados que só acontecem em 2% dos casos, se nosso modelo ignorar estes dados nosso modelo vai ter uma acurácia de 98% que seria uma acurácia boa mas não é pois ela ignora os casos que queremos analizar 
## Recall(Sensibilidade)
![Screenshot_92](https://github.com/danielcasanova12/Predicao/assets/119464431/2926e306-1e75-4efd-a82e-7cea78ed1ecf)
## Especificidade
É o inverso do recall ele usa a coluna TN e FP sua fórmula é :
![Screenshot_93](https://github.com/danielcasanova12/Predicao/assets/119464431/892e4cde-4975-4930-8617-d2a077acde60)

## Precisão
Dos classificados como TP e FP quantos % realmente são verdadeiros :
![Screenshot_95](https://github.com/danielcasanova12/Predicao/assets/119464431/59d11973-926e-4002-8a58-8224c530c1d9)
## F1 Score
É uma média harmônica que leva em conta a precisão e o recall 
![Screenshot_96](https://github.com/danielcasanova12/Predicao/assets/119464431/47796257-2b3f-4074-8fda-0d717aa5683e)
## ROC
A curva ROC é uma curva que varia de 0.5 a 1 onde 1 significa 100% de  sensibilidade e 100% de especificidade e quando dá 0.5 o teste não tem capacidade diagnóstica nem uma.Idealmente, queremos que nosso modelo tenha uma alta taxa de verdadeiros positivos e uma baixa taxa de falsos positivos, o que significa que a curva ROC estaria mais próxima do canto superior esquerdo do gráfico.

## AUC
A curva AUC facilita para comparar uma curva ROC com outra.Embora os gráficos ROC sejam desenhados usando Taxas de Verdadeiros Positivos e Taxas de Falsos Positivos para resumir matrizes de confusão, existem outras métricas que tentam fazer a mesma coisa. Essas métricas são usadas para avaliar o desempenho de modelos de classificação e identificar o equilíbrio entre a taxa de acertos e a taxa de falsos positivos.

## Dealing With Real-World Data
Bias e Variância: 
 * Bias ou viés é a distância média entre as previsões e os valores reais.
 * Variância: Dispersão das previsões.

![Screenshot_97](https://github.com/danielcasanova12/Predicao/assets/119464431/b0897a99-6031-4354-bb1e-8d62b896879f)

O erro é calculado da seguinte maneira
𝐸𝑟𝑟𝑜𝑟 = 𝐵𝑖𝑎𝑠² + 𝑉𝑎𝑟𝑖𝑎𝑛𝑐𝑒
Nosso objetivo é ter um modelo que tenha Bias e variancia baixos para obter o menor erro possível.

## Cleaning  Data (Limpeza de Dados)

Este processo nos ajuda a identificar e remover os dados que podem prejudicar o treinamento do nosso modelo 
* Outliers: São valores muito diferentes da maioria dos outros dados.
* Missing Data: Valores ausentes causados por erros da entrada ou perda de dados.
* Erroneous Data: Dados que foram alterados acidentalmente.
* Irrelevant Data: Dados que são irrelevantes para nosso modelo.
* Inconsistent Data: Dados de diferentes fontes ou que foram alterados ao longo do tempo
* Formatting: Dados mal formatados, como diferentes unidades de medidas ou datas.

Esta parte de limpeza de dados é um passo que pode definir se nosso modelo vai ser um bom modelo ou se nosso modelo terá problemas. Devemos dar muita atenção nesta parte para garantir que nossos dados realmente estejam limpos e prontos para uso.

## Detecção de Outliers
* Z-Score: Essa técnica utiliza a média e o desvio padrão dos dados para identificar outliers. Valores com Z-Score maior que 3 ou menor que -3 geralmente são considerados outliers.
Percentis: Essa técnica divide os dados em quartis. O primeiro quartil (Q1) representa 25% dos dados, o terceiro quartil (Q3) representa 75% dos dados e o intervalo interquartil (IQR) é a diferença entre Q3 e Q1. Valores que estão fora do intervalo IQR +/- 1.5*IQR podem ser considerados outliers.
Dados Desbalanceados

* Em problemas de classificação, é comum ter classes desbalanceadas, ou seja, uma classe possui muito mais exemplos que a outra. Isso pode prejudicar o desempenho do modelo, pois ele tende a aprender apenas a classe majoritária.

## Técnicas para lidar com dados desbalanceados
* Oversampling: Aumentar artificialmente a quantidade de exemplos na classe minoritária.
* Undersampling: Reduzir artificialmente a quantidade de exemplos na classe majoritária.
* SMOTE (Synthetic Minority Over-sampling Technique): Criar novos exemplos na classe minoritária a partir de exemplos existentes.

## Outras técnicas de pré-processamento são elas:
* Binning: Transformar dados numéricos em dados categóricos.
* Transforming: Transformar os dados para melhorar a performance do modelo.
* Encoding: Transformar os dados em um formato compatível com o modelo.
* Scaling/Normalização: Ajustar a escala dos dados para que estejam em uma faixa similar.
* Shuffling: Embaralhar os dados para evitar que o modelo aprenda padrões indesejados.

* 


