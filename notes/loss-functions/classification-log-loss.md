# Métrica para classificação - Log Loss ou binary cross-entropy

## Links

https://mariofilho.com/guia-completo-da-log-loss-perda-logaritmica-em-machine-learning/

## Quando usar

Log Loss é parecido com Acurácia, com a diferença que, ele foca mais na probabilidade para uma determinada classe do que ser da classe mesmo. Por exmeplo, em uma classificaçao binaria, geralmente ao thshehold é 0.5. Enquanto que a cauracia só se preocupa se a poba é  maior ou menor que o ponto de corte, a log loss vai focar se a proba está mesmo próximo dos extemros, 0 e 1.

**Foca mais na probabildiade que é dada para um elemetno ser de uma classe**

Responsta da net: https://stats.stackexchange.com/questions/180116/when-is-log-loss-metric-appropriate-for-evaluating-performance-of-a-classifier

Log-loss is an appropriate performance measure when you're model output is the probability of a binary outcome.

The log-loss measure considers confidence of the prediction when assessing how to penalize incorrect classification. For instance consider two predictions of an outcome P(Y=1|X), where the predictions are 0.51 and 0.99 respectively. In the former case the model is only slightly confident of the class prediction (assuming a 0.5 cutoff), while in the latter it is extremely confident. Since in our case both are wrong, the penalty will be more harsh for the more confident (but incorrect) prediction by employing a log-loss penalty.

## Mario FIlho

https://mariofilho.com/guia-completo-da-log-loss-perda-logaritmica-em-machine-learning/

Log loss (ou perda logarítmica) é uma métrica de avaliação de modelos de classificação em machine learning, tanto binários quanto multiclasse.

Ela brilha em casos em que é importante que as probabilidades emitidas pelo modelo estejam alinhadas com a proporção real de ocorrências do alvo.

fórmula

![](https://mariofilho.com/img/log_loss/0.png)

````python
from sklearn.metrics import log_loss

# Rótulos verdadeiros
y_true = [1, 0, 1, 1, 0]

# Probabilidades previstas pelo modelo
y_pred = [[0.9, 0.1], [0.8, 0.2], [0.3, 0.7], [0.1, 0.9], [0.7, 0.3]]

# Calcula a log loss
loss = log_loss(y_true, y_pred)

print(loss)  # Imprime a log loss
````
