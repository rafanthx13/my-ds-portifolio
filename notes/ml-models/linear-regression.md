# REgressâo Linear

HABIT TRACKER

Resumo: Apenas reiterando, o que acontece é que buscamos uma equação linear para descrever a
relação de N variáveis, chamadas de features, com uma outra variável, chamada de alvo.

A equaçâo será:

y = ax + b

Onde evemos encontrar os coeifcieintes a e b, de tal forma que deduzam a loss fucntion que em geral é o erro quadrático médio (MSE - Mean Squared Error)

## Usanda Cauclul apra encontrar a e b mais fácil

Usando caclucla para necontrar  a e b para os coeificieintes:
+ Restruturando MSE e usando derivada parcial = 0, voce encontra os pontos minimos que reduzem a funçao, e assim obter uma formula para a e b que usa poucos dados

https://www.freecodecamp.org/portuguese/news/aprendizagem-da-maquina-uma-introducao-ao-erro-quadratico-medio-e-linhas-de-regressao/

## Teste de Hipotestse em  REressâo linar

https://medium.com/nerd-for-tech/hypothesis-testing-on-linear-regression-c2a1799ba964

Quando construímos um modelo de regressão linear múltipla, podemos ter algumas variáveis ​​preditoras/independentes em potencial. Portanto, é extremamente importante selecionar as variáveis ​​que são realmente significativas e influenciam fortemente o experimento. Para obter o modelo ideal, podemos tentar todas as combinações possíveis de variáveis ​​independentes e ver qual modelo se ajusta melhor. Mas esse método é demorado e inviável. Portanto, precisamos de outro método para obter um modelo decente. Podemos fazer o mesmo por eliminação manual de recursos ou usando qualquer abordagem automatizada (RFE, Regularização, etc.).

Na eliminação manual de recursos, podemos:

+ Construir um modelo com todas as features
+ Elimine os recursos que são menos úteis na previsão (alto valor p),
+ Elimine os recursos redundantes (usando correlações e VIF),
+ Reconstrua o modelo e repita.

Para calcular esse alto p-valor faça coomo no exemplo. O que tive o P > |t| maior que 0.005 siginfica que tem que tirar pois nao sao singificandates
