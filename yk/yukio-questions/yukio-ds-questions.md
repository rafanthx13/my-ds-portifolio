# Perguntas Importantes de Data Science - Yukio Content

```
1 - O que é regularização (YK03)
2 - O que são modelos ensemble (yk03)
3 - Como funciona um árvore de decisao (yk03)
4 - O que é loss function (yk03)
5 - O que é um modelo de ML (yk-02-08-23)
6 - O qu eé regressâo linear
7 - O que é overfitting (yk02)
8 - O que são estimadores Blue
9 - O que é VIF (yk03)
10 - Qual a diferença entre Multicolinearidde x correlaçao x colinearidade
11 - O que é Cherry Picking (yk04)
12 - O que é p-hakcking (yk04)
13 - O que é víes de sobrevivencia (yk04)
14 - O que é efeito cobra (yk04)
15 - O que é a Falsa causalidade (falta de um treceiro elemento) (yk04)
16 - Entropia, incerteza (yk04 ou 05)
17 - Ordem de execuçao do SQL e como otimizar
18 - SQL stametens to DS (yk05)
19 - O que é p-valor (yk05)
20 - K-Means (yk05)
21 - O que é erro do tip 1 e 2 (yk05)
22 - Diferneça entre precisao e recall (yk06)
23 - O que é discretizaçao (yk08)
24 - RFV e XPTO (yk11)
25 - Método cotovelo e silhueta (clustering (yk10))
26 - O que é ECDFe porque é melhor que histograma (yk12)
27 - Livro Ace THe DataScience interview questions
28 - COncietos de NeuralNet: Early Stoppin, Drop Out, Batch Normalization, Gradiente descendente estocástico, cross-entropy, sigmoid, softmax (yk18)
29 - COHORT (yk20)
30 - O que é pivot-able (yk20)
31 - Testes KS: Kolmogorov-Sminrnov
32 - DataDrift (yk21))
33 - O que é skenss e kurtoise yk21()
34 - O que é Mann-Whitney (yk22)
36 - O que é Data Leakeage (yk22)
37 - O que é Holdout,  Cross-validation e metodologias para valiad rum modelo
38 - Viés e Variância
39 - Premissas de Gauss-Markov para reg. linear
40 - Inferencia (yk26)
41 - R  e R2 Ajustado
```

## 1 - O que é regularização (YK03)

É uma técninca para evitar overfitting, que é, quando o modelo se ajuda demais aos daos de treino, ficando de certa forma viciado, como se tivesse decorado a base de treino, é o caso quando o modelo vai bem no treino e bem menos no teste.

Overfitting é comun em modelos muito complexos como deep learning pois é quando o padrão a ser encontrado é xomplexoas, como os usaos de DL.

A regularizçâo é uma forma de adicionar uma penalizade ao procesos de treinamento de ML para que, ao diminuit a loss function, nâo pases d um ponto saudável. Essa penalizdade vai corrigir o aprendizado faznedo com que o modelo nâo passe do ponto em que é generalista apra especifico demais.

As regularzçôes mais famosos sao as apra corrigir regressoa linear: L1 (lasso), L2 (ridge) e ELastic Net

Em suma, a regularização vai tentar evitar que um modelo se ajuste demais aos dados de
treinamento, melhorando sua capacidade de generalização para novos dados.

## 2 - O que são modelos ensemble (yk03)

modelos ensemble  sâo modelos que combinam mais de um modelos, dos ais diversos tipos, para azer uma previsao melhor.

Ex: Rnadom Forest: COmo o nome diz, uma FOrest usa mais de uma árvore de decisao

Baggins: QUnaod os modelos aprendem de forma paralelas e independente entre si. O reusltado é a soma (com pesos) ou média das previsões

Boosting: É quando um modelo aprende com o output d eum outro modelo

## 3 - Como funciona um árvore de decisao (yk03)

A árvore de decisão é um algoritmo que funciona como se fosse um fluxograma de perguntas
que levariam até uma resposta final, até uma tomada de decisão. Então você imagina que a
gente tenha uma árvore para um modelo de risco de crédito. Na hora que um cliente for passar
pelo modelo, ele vai cair numa série de perguntas nesse fluxograma, coisas como "número de
imóveis próprios", "salário abaixo ou acima de determinada faixa", "se possui uma dívida em
aberto ou não". Cada uma das possíveis respostas vai levar a uma decisão final do modelo,
entre classificar a pessoa como boa ou má pagadora.

A escolha entre começar com a pergunta da dívida, ou do salário, a sequência de perguntas,
vai ser determinada através da relevância da feature. E o algoritmo vai considerar a feature
mais relevante aquela que consegue separar melhor o público. Para simplificar, imagine que a
gente tenha a pergunta se a pessoa tem ou não imóvel e a pergunta se a pessoa tem ou não
dívida em aberto. A dos imóveis, deixa um lado com metade sendo mau pagador e metade
sendo bom pagador. A de dívida em aberto, deixaria todos os maus pagadores de um lado e os
bons de outro, ou que seja todos os maus de um lado e o outro lado com 90% de bons
pagadores e 10% de maus pagadores. Bom, então a pergunta da dívida separa melhor os bons
dos maus clientes, ela é a que iria primeiro. Claro, isso simplificando. Na prática, temos duas
possíveis métricas, o índice de Gini ou a Entropia.

## 4 - O que é loss function (yk03)

É o que o modleo usa para saber se está indo bem no terinmaneto. É uma forma para quantificar erros.

Ex: Uma regressâo linear encontra os coeficiente obsevando o erro, que no caos, é a loss funcoion, buscando minimizá-lo.loss function é um termo generico, mas, uma loss function real pdoeria ser, por xemplo  MSE (Mean Squared Error - Erro médio quadrático).

MInimizar a funçâo perda significa preve o mais primo possivel da saida real.

Uma loss function para classificaçao pode ser log loss (tambem chamad de binary cross-entropy)

## 8 - O que são estimadores Blue?

https://k3ybladewielder.medium.com/princ%C3%ADpios-da-regress%C3%A3o-linear-3ab26a7b4340

Sob a hipótese da veracidade de alguns pressupostos, os estimadores obtidos pelo método de mínimos quadrados ordinários (ordinary least square — OLS ) serão os Melhores Estimadores Lineares Não Viesados (MELNV, ou BLUE - Best Linear Unbiased Estimator).

Um estimador é BLUE quando atende as propriedades de produzir uma menor variância (Best), sua relação é linear (Linear) e sua distribuição amostral é não-enviesada (Unbiased), ele é enviesado quando sistematicamente sobreestima ou subestima o valor do parâmetro populacional.



## 9 - O que é VIF (yk03)

https://k3ybladewielder.medium.com/princ%C3%ADpios-da-regress%C3%A3o-linear-3ab26a7b4340

Técnica para detectar multicolineariedade podemos fazer o teste [Variance Inflation Factor (VIF)](https://en.wikipedia.org/wiki/Variance_inflation_factor) e/ou visualizar uma matriz de correlação (pearson) entre as variáveis independentes. O calculo de VIF é feito em cada variável indepentente, se igual a 1 não existe correlação, de 1 a 5 existe correlação moderada e maior que 5 existe alta correlação.

EM Python

https://www.kaggle.com/code/simranjain17/linear-regression-assumptions-code#Statsmodel-Regression-and-Meaning

```python
#Multicollinearity - VIF
#VIF>10, REMOVE. - high VIF indicates high multicollinearity
#VIF>10 indicates heavy multicollinearity so those factors should be removed, <5 is good

from statsmodels.stats.outliers_influence import variance_inflation_factor
vif = [variance_inflation_factor(x_train.values, i) for i in range(x_train.shape[1])]
pd.DataFrame({'vif':vif[0:]}, index = x_train.columns).T

#based on results - BMI should be definitely removed
"""
	age	sex	bmi	children	smoker	region_northwest	region_southeast	region_southwest
vif	7.748538	1.969008	11.326139	1.794558	1.249763	1.902356	2.36985	2.068206
"""
```



## 10 - Qual a diferença entre Multicolinearidde x correlaçao x colinearidade

O que é COlinearidade e Multicolineariadde

Expressão da relação entre duas (colinearidade) ou mais (multicolinearidade) variáveis independentes. Diz-se que duas variáveis independentes exibem colinearidade completa se seu coeficiente de correlação é 1, e completa falta de colinearidade se o coeficiente de correlação é 0. A mutlicolinearidade ocorre quando qualquer variável independente é altamente correlacionada com um conjunto de outras variáveis independentes. Um caso extremo de colinearidade/multicolinearidade é a singularidade, na qual uma variável independente é perfeitamente prevista (ou seja, correlação de 1,0) por uma outra variável independente (ou mais uma).

A multicolinearidade é uma situação em que duas ou mais variáveis independentes em um modelo de regressão encontram-se altamente correlacionadas.

Essa alta correlação pode afetar a qualidade dos resultados do modelo e dificultar a interpretação dos resultados.

Por exemplo, imagine que você queira estimar o efeito da escolaridade e renda na satisfação com a vida. Aqui no Brasil, renda e escolaridade são altamente correlacionadas. Isso pode dificultar a interpretação dos resultados do modelo, uma vez que a contribuição de cada variável para explicar a variável dependente fica menos clara.

**O grande problema está em que como são correlacionados, não dá pra sabeer se o efeito que uma delas causa é dela ou de outra. Ou seja, fica dificil distinguir de onde vem o efeito**

**==> Como identificar a Multicolinearidade?**

Uma maneira de detectar a multicolinearidade é examinar a matriz de correlação das variáveis independentes. Correlações altas, acima de 0,70 entre pares de variáveis indicam que elas estão fortemente correlacionadas. Correlações acima de 0,80 são ainda mais preocupantes.

Outro indicador é o valor do fator de inflação da variância (VIF), que mede quanto a variância do coeficiente estimado para uma variável é inflada devido à multicolinearidade com as outras variáveis independentes. VIFs maiores que 10 indicam alta multicolinearidade, enquanto valores entre 5 e 10 podem ser preocupantes.

A multicolinearidade é o mesmo fenômeno, só que para mais do que duas variáveis. Ou seja, quando três ou mais variáveis tem uma relação (quase) perfeita entre si.

**==> Como lidar com a multicolinearidade?**

Existem várias técnicas que podem ser utilizadas para lidar com a multicolinearidade:

**Técnica 1: Exclusão de variáveis**

A maneira mais simples de lidar com a multicolinearidade é excluir a variável multicolinear. Isso pode ser feito sem perda de informação, já que aquela variável está redundante com outras variáveis. No entanto, essa técnica pode ser problemática, especialmente se a variável excluída for importante para a análise.

**Técnica 2: Agrupamento de variáveis**

Outra maneira é realizar um agrupamento das variáveis multicolineares, por meio de técnicas de redução, como Análise de Componentes Principais (ACP). Nesse caso, ao invés de utilizar múltiplas VIs, gera-se um escore único, a partir de uma variável de agrupamento, gerada pela Análise de Componentes Principais (ACPs). A vantagem dessa técnica é que o modelo se torna mais parcimonioso. A desvantagem é que você perde a informação de cada preditor individualmente.

**==> O que é Multicolinearidade - Outra Explicação**

Em regressão, "multicolinearidade" refere-se a preditoras correlacionadas com outras preditoras. A multicolinearidade ocorre quando o modelo inclui vários fatores correlacionados não apenas à sua variável de resposta, mas também uns aos outros. Em outras palavras, resulta quando você tem fatores que são, de certa forma, um pouco redundantes.

Analogia: Você vai ver uma banda de rock and roll com dois grandes guitarristas. Você está ansioso para ver qual deles toca melhor. Mas no palco, ambos estão tocando trechos de música ao mesmo tempo! Quando os dois estão tocando alto e rápido, como você pode dizer qual guitarrista tem o maior efeito no som? Mesmo que eles não estejam tocando as mesmas notas, o que eles estão fazendo é tão similar que é difícil distinguir um do outro.

Esse é o problema com a multicolinearidade.

A multicolinearidade aumenta os erros padrão dos coeficientes. O aumento dos erros padrão, por sua vez, significa que os coeficientes para algumas variáveis independentes podem não ser significativamente diferentes de 0. Em outras palavras, ao super-inflacionar os erros padrão, a multicolinearidade torna algumas variáveis estatisticamente insignificantes quando deveriam ser significativas. Sem multicolinearidade (e, portanto, com erros padrão mais baixos), esses coeficientes poderiam ser significativos.

COMO POSSO LIDAR COM A MULTICOLINEARIDADE?

Se a multicolinearidade for um problema em seu modelo - se o VIF para um fator estiver próximo ou acima de 5 - a solução pode ser relativamente simples. Experimente uma destas:

- **Remova do modelo as preditoras que são altamente correlacionadas**. Se você tiver dois ou mais fatores com um VIF alto, remova um deles do modelo. Como eles fornecem informações redundantes, a remoção de um dos fatores correlacionados geralmente não reduz drasticamente o R-quadrado. Considere o uso de [regressão stepwise](https://blog.minitab.com/blog/statistics-and-quality-data-analysis/giving-thanks-for-the-regression-menu-v2), [regressão melhores subconjuntos](https://blog.minitab.com/blog/statistics-and-quality-data-analysis/giving-thanks-for-the-regression-menu-v2), ou o conhecimento especializado do conjunto de dados para remover essas variáveis. Selecione o modelo que apresenta o maior valor de R-quadrado.
- **Use [Regressão de Mínimos Quadrados Parciais (PLS)](https://blog.minitab.com/blog/statistics-and-quality-data-analysis/giving-thanks-for-the-regression-menu-v2) ou Análise de Componentes Principais**, que são métodos de regressão que reduzem o número de preditoras a um conjunto menor de componentes não correlacionados.

## 11 - O que é Cherry Picking (yk04)

Cherry Picking é o nome que damos para quando escolhemos somente dados que suportam
nossas hipóteses/crenças, ignorando os demais.

## 12 - O que é p-hakcking (yk04)

É tentar maniuplar os ados para encontrar um p-valor aceitável



https://www.youtube.com/watch?v=0IMYHTB07tk

## 13 - O que é víes de sobrevivencia (yk04)

Muitas vezes, profissionais de dados e pesquisadores tomam conclusões apenas com base em
parte da amostra. Imagine que você está estudando um remédio e parte dos pacientes morrem
durante o tratamento; ou que você esteja estudando como certa dieta impacta a saúde das
pessoas e parte da sua amostra desiste da dieta no meio do processo. Tomar decisões com
base apenas em quem permaneceu no estudo até o final pode ser arriscado. Sempre que isso
for necessário, é preciso cautela nas conclusões e interpretação dos resultados do
experimento.

Voltemos ao experimento do remédio e dos pacientes que morreram antes que ele chegasse
ao final. Imagine que você tenha 2 grupos de 50 pessoas. Um grupo tomou remédio, outro
grupo não tomou. Imagine que o remédio cause um efeito colateral que ninguém conhecia e
que pode, em algumas pessoas, acelerar o desenvolvimento da doença que deveria ser
tratada. Não é algo conhecido dos pesquisadores, mas esse remédio é inútil e ainda pode
causar piora em 20% dos pacientes, normalmente, pessoas já com dificuldade de melhorar dadoença.
Ao fim de 1 ano de tratamento, no grupo controle, das 50 pessoas tratadas com placebo, 25
estão melhores e 25 seguiram com a doença, tendo ainda uma leve piora do quadro. Ou seja,
note desde já que mesmo sem tratamento, 50% das pessoas melhoram sem fazer nada. No
grupo tratado com remédio, 10 pessoas morreram e sobraram 40. Como o remédio acelera a
morte de quem já tinha alguma condição pior de saúde, no restante dos participantes, tivemos
25 pessoas com melhora na qualidade de vida e 15 que pioraram o quadro.

Um pesquisador desavisado, pode concluir o seguinte do experimento: no grupo controle, 50%
melhoraram e 50% pioraram a condição de sua saúde. Já no grupo tratado com remédio,
62,5% melhoraram e 37,5% pioraram sua saúde. Ou seja, ele concluiu que o remédio é ótimo
para tratar a doença, algo que sabemos ser equivocado.

## 14 - O que é efeito cobra (yk04)

Não vejo como uma falácia de dados, mas estava na lista e é importante falar do caso. Isso
ocorre quando temos incentivos perversos, quando algo tem efeito contrário ao esperado. Por
exemplo, na Colômbia, o exército teve uma política de incentivos para matar mais terroristas,
remunerando militares por mortes. O que aconteceu? Eles passaram a matar inocentes.
Acho importante e vem junto com a minha insistência para que todos interessados em políticas
públicas leiam livros como Freakonomics. Não importa o quanto sua hipótese é boa e faça
sentido na sua cabeça. Na prática, pode ocorrer algo que você não esperava e o resultadoacabar indo em outra direção.

## 15 - O que é a Falsa causalidade (falta de um treceiro elemento) (yk04)

Esta é a famosa frase: Correlação não implica em causa. Pode acontecer da correlação ser
apenas uma coincidência, algo espúrio. Mas também pode acontecer de existir uma terceira
variável que não foi envolvida na análise. Por exemplo, imagine que você descubra que álcool
está correlacionado com sucesso. Pode ser que algum colega seu ouça essa notícia e saia
bebendo para tentar obter mais sucesso. Você, no entanto, trabalha com dados e sabe que
correlação não implica em causa. Depois de estudar mais os dados, descobre que o que
acontece é que pessoas que bebem são mais sociáveis e ser sociável é um fator importante
para se obter o sucesso profissional. Logo, não é o álcool que causa sucesso, mas sim a
pessoa ser sociável.

## 16 - Entropia, incerteza (yk04 ou 05)

Entropia pode ser definida como a medida que nos diz o quanto nossos dados estão desorganizados e misturados. 

Quanto maior a entropia, menor o *ganho de informação* e vice-versa. 

Nossos dados ficam menos entrópicos conforme dividimos os dados em conjuntos capazes de representar apenas uma classe do nosso modelo.

Numa árvore de decisâo, escolhe-se o caminho que  minimizem a entropia e aumentem o ganho de informação.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*BcvhO2MbJ-TJurIasvRm-w.png)

## 17 - Ordem de execuçao do SQL e como otimizar

FROM + JOIN > WHERE > GROUP BY > HAVING > SELECT > ORDER BY > LIMIT

Por causa disso há aluns casos interssantes

+ LIMIT: COmo ele é o ultimo significa que se voce faz algo e coloca limit para reduzir, saiba que VAI FAZER AQUILO QUE VOCE QUER SOBRE TUDO E SÓ VAI RECORTAR NO FINAL. ISOS NAO IMPEDE UM GRANDE PROCESSAMENTO
  + Uma forma de melhorar e otimizar da forma como penamosa
  + AO invez de fazerr `SELECT AFUCNTION(*) FROM X LIMIT 3000`
  + Faça: `SELECT AFUNCTION(y.*) FROM SELECT * FROM X LIMIT 3000) AS y`
+ WHERE > HAVING: Se você usa o HAVING para filtrar, por exmeplo, fitlrar uma categoria especifica do group by, ao invez de colocar esse filtro no having, coloque no WHere que vai OTIMIZAR

## Quando fazer o pré-processamento e quando fazer o split?

Já comentei diversas vezes que o preenchimento de missing, tratamento de categóricas e
encoders devem ser feitos após o split em treino-teste. Isso porque os dados de teste são
simulações de dados em produção, logo, não devem ser usados na construção do modelo, eles
não podem ser “vistos” pelos dados de teste. Entretanto, se você fizer um preenchimento de
missing usando a média da coluna inteira, antes do split, você estará usando no cálculo da
média a informação dos dados de treino e de teste juntos. Ou seja, informação dos dados de
teste irá parar nos dados de treino.

Sendo assim, a forma de evitar o erro é fazendo os tratamentos de missing, scaler e encoder
após o split. Veja, entretanto, que estamos falando de preprocessamento. Há outros
tratamentos que podem ser feitos antes mesmo do split. Entendendo bem os motivos
explicados no parágrafo acima, você não vai errar nunca essas questões. Abaixo, duas
discussões para você seguir com a reflexão:

+ https://stats.stackexchange.com/questions/95083/imputation-before-or-after-splitting-into-train-and-test
+ https://datascience.stackexchange.com/questions/53138/which-comes-first-multiple-imputation-splitting-into-train-test-or-standardiz

Agora, responda à seguinte pergunta: eu preciso criar uma variável que utilize o número de
dias entre a coluna 1 e a coluna 2. Ou seja, quero gerar uma nova coluna que é resultado da
subtração entre outras duas. Isso deve ser feito antes ou depois do split em treino-teste? Faz
diferença? Por qual motivo? Discuta com seus colegas!

## 19 - O que é p-valor na analise de regressao linear (yk05)

**COMO EU INTERPRETO OS VALORES-P NA ANÁLISE DE REGRESSÃO LINEAR?**

O valor-p para cada termo testa a hipótese nula de que o coeficiente é igual a zero (sem efeito). Um valor-p baixo (< 0,05) indica que você pode rejeitar a hipótese nula. Em outras palavras, uma preditora que tenha um valor-p baixo provavelmente será uma adição significativa ao seu modelo, porque as alterações no valor da preditora estão relacionadas a alterações na variável resposta.

Por outro lado, um valor-p maior (insignificante) sugere que as mudanças na preditora não estão associadas a mudanças na resposta.

Na saída abaixo, podemos ver que as variáveis preditoras do Sul e do Norte são significativas porque ambos os valores-p são 0,000. No entanto, o valor-p para o Leste (0,092) é maior do que o nível alfa comum de 0,05, o que indica que ele não é estatisticamente significativo.

![img](https://blog.minitab.com/hs-fs/hubfs/image-17.png?width=315&name=image-17.png)

Normalmente você usa os valores-p dos coeficientes para determinar quais termos devemos manter no modelo de regressão. No modelo acima, devemos considerar a remoção de Leste.



## 20 - K-Means (yk05)

O algoritmo K-Means é provavelmente a técnica mais popular de aprendizado
não-supervisionado. A lógica por trás do algoritmo é simples: agrupar observações de acordo
com um grupo de características, deixando as observações mais semelhantes no mesmo
cluster. Podemos falar tanto de agrupar indivíduos consumidores de acordo com seu
comportamento de compra, quanto de produtos de um supermercado separados de acordo
com tamanho e preço, ou cidades em que a empresa atua, de acordo com número de vendas e
receita média.

Para continuar no nosso ritmo sem jargão e matematiquês, vamos falar do funcionamento do
algoritmo de uma forma simples e direta. Funciona assim: você começa determinando "K", i.e.,
o número de grupos que deseja segmentar seus dados. Há diversas formas de se escolher um
"K" ideal ao problema, algumas com mais, outras com menos subjetividade. Por enquanto,vamos ignorar essa parte e apenas assumir que escolhemos a quantidade de grupos que
queremos dividir nossos indivíduos. Na sequência, de forma aleatória, o algoritmo selecionará
K pontos para serem os centros dos grupos, esses pontos são chamados "centróides". Em
seguida, cada elemento é colocado no grupo do centróide mais próximo.

Então vamos lá entender bem: escolhemos o número de grupos, o algoritmo determina
aleatoriamente algumas posições para serem os centros dos grupos e as observações são
colocadas nos grupos em que o centro é mais próximo a elas. Imagine assim, você tem um
centróide (0,0) e um outro centróide (100, 100), então se tiver uma observação (10, 10), ela
ficará no grupo do primeiro centróide. Logo falaremos de como calcular essa distância - spoiler
alert: distância euclidiana -, mas por enquanto vamos assumir somente esse exemplo óbvio.
Uma vez que os pontos todos forem distribuídos, o centro é recalculado, usando a média de
seus elementos. Novamente, os elementos são alocados para os centróides mais próximos.
Isso é feito inúmeras vezes, até que não seja mais possível.

A lógica por trás do algoritmo é um dos motivos de seu sucesso, é muito simples de
compreender o que está acontecendo. No fundo, você está apenas colocando coisas
semelhantes juntas e essa semelhança é baseada numa distância matemática. Simples assim!
Para reforçar mais um pouco, recomendo a leitura deste antigo post meu:
https://estatsite.com.br/2016/05/03/tecnicas-de-clustering-k-means/
Agora, quer ver algo legal? Eu já fiz o K-Means "na mão", só usando o Excel. Se quiser ver e
matar a curiosidade de como funciona o algoritmo na prática, é só acompanhar o
desenvolvimento no seguinte post:
http://www.estatsite.com.br/2017/05/23/clusterizacao-na-pratica/
O importante você já pegou: o algoritmo vai distribuir os indivíduos em grupos onde eles
estarão mais próximos entre os seus semelhantes. Se temos um indivíduo de renda mil reais,
um de renda 2 mil reais e um de renda 100 mil reais, é provável que os 2 primeiros fiquem no
mesmo grupo. Se quiser pensar nisso com mais características, basta adicionar um cálculo
matemático, como o da distância euclidiana, e tá pronto!

## 21 - O que é erro do tip 1 e 2 (yk07)

![](img-1))

**Quando você rejeita algo que é verdadeiro, você está cometendo um erro do tipo I.** 

**E quando não está rejeitando algo falso, você está cometendo um erro tipo II**.

Para finalizar, vamos olhar alguns termos importantes:
●
Verdadeiro Positivo (VP): É uma predição correta do modelo em que a classe prevista
e a classe real são iguais e ambas iguais a 1. Por exemplo, se o modelo prevê que uma
pessoa está doente e ela realmente está doente, então temos um caso de verdadeiro
positivo. Lá na nossa primeira matriz de confusão, temos 10 casos de VP.
●
Verdadeiro Negativo (VN): É uma predição correta do modelo em que a classe prevista
e a classe real são iguais e iguais a 0. Por exemplo, se o modelo prevê que uma pessoa
não é culpada de um crime e ela realmente não é culpada, temos um caso de
verdadeiro negativo. Na nossa primeira matriz, temos 12 casos de VN.
●
Falso Positivo (FP): É uma predição incorreta do modelo onde ele prevê que a classe
é positiva, igual a 1, mas na verdade é igual a zero. Por exemplo, se o modelo prevê
que uma pessoa está doente, mas, na verdade, ela não está doente, então temos um
caso de falso positivo. No nosso primeiro exemplo desta seção, temos 1 caso de FP.
●
Falso Negativo (FN): É uma predição incorreta do modelo, onde a classe prevista é
negativa, igual a zero, mas, na verdade, a observação tem classe positiva, igual a 1. Por
exemplo, se o modelo prevê que uma pessoa não é culpada de um crime, mas na
verdade ela é culpada, então temos um caso de falso negativo. No nosso primeiro
exemplo, temos 2 casos de FN.
●
Precision: É a proporção de verdadeiros positivos em relação a tudo que o modelo
classificou como positivo, como 1. Seria o mesmo que dizer assim: de todos os casos
em que meu modelo disse que era 1, temos X% sendo realmente 1.
A fórmula da precisão é: VP / (VP + FP)
●
Recall (ou Sensibilidade): É a proporção de verdadeiros positivos em relação a tudo
que realmente é 1. Seria o mesmo que dizer: de tudo que é realmente 1, meu modelo
conseguiu capturar corretamente X%.
A fórmula do recall é: VP / (VP + FN)

## 22 - Diferneça entre precisao e recall (yk07

**Precisão**

A precisão mede a quantidade de vezes que o seu modelo acerta em relação ao total de vezes que ele tenta acertar.

A precisão mede o quanto podemos confiar num modelo quando ele prevê que um exemplo pertence a uma determinada classe. Ou seja, dos que ele previou como positivos, quantos ele acertou.

Exemplo: 

Imagine que você tem um modelo de machine learning que tenta prever se uma pessoa tem ou não uma doença rara.

Nos dados de avaliação seu modelo previu que 80 pessoas têm a doença, mas apenas 60 delas realmente tinham a doença, então a precisão dele é de 60/80 = 75%.

No futuro, podemos esperar que, se o modelo prever que uma pessoa tem a doença, em 75% dos casos ele estará certo.

**Se a Precisão for X. E meu modelo diz que i é da classe W, então tenho X% de certeza que é W**

**dentre as previsões positivas, quais estão corretas.**

**RECALL**

O recall mede a quantidade de vezes que o seu modelo acerta em relação ao total de vezes que ele deveria ter acertado.

O recall é o número de pessoas que o modelo identificou corretamente como tendo a doença dividido pelo número total de pessoas que realmente têm a doença nos seus dados.

Ou seja, de todas as pessoas que ele poderia classificar como positivas, quantas ele acertou.

Por isso esta métrica também é conhecida como taxa de detecção: de todos os exemplos que o modelo poderia detectar, quantos ele realmente conseguiu.

PODE SER ENTENTIDO como

Se o REcall fo X, enão  meu modelo classifica corretamnte X dos elementos da classe W. E não epga W-1 elementos que deveria ser da classe W.

**dentre as observações que são positivas, quantas nosso modelo capturou.**

**F1**

A média harmônica é usada porque ela dá mais importância a valores baixos.

F1 = 2 * ((P * R)/(P+R))

Perceba que se um dos dois for muito baixo, vai baixar muito a métrica



**Quando usar cada coirsa**

Quando usar cada uma?

A **acurácia** é uma boa indicação geral de como o modelo performou. Porém, pode haver situações em que ela é enganosa. Por exemplo, na criação de um modelo de identificação de fraudes em cartões de crédito, o número de casos considerados como fraude pode ser bem pequeno em relação ao número de casos considerados legais. **Para colocar em números, em uma situação hipotética de 280000 casos legais e 2000 casos fraudulentos, um modelo simplório que simplesmente classifica tudo como legal obteria uma acurácia de 99,3%.** Ou seja, você estaria validando como ótimo um modelo que falha em detectar fraudes.

A **precisão** pode ser usada em uma situação em que os **Falsos Positivos são considerados mais prejudiciais que os Falsos Negativos**. Por exemplo, ao classificar uma ação como um bom investimento, é necessário que o modelo esteja correto, mesmo que acabe classificando bons investimentos como maus investimentos (situação de Falso Negativo) no processo. Ou seja, o modelo deve ser preciso em suas classificações, pois a partir do momento que consideramos um investimento bom quando na verdade ele não é, uma grande perda de dinheiro pode acontecer.

O ***recall\*** pode ser usada em uma situação em que os **Falsos Negativos são considerados mais prejudiciais que os Falsos Positivos.** Por exemplo, o modelo deve de qualquer maneira encontrar todos os pacientes doentes, mesmo que classifique alguns saudáveis como doentes (situação de Falso Positivo) no processo. Ou seja, o modelo deve ter alto *recall*, pois classificar pacientes doentes como saudáveis pode ser uma tragédia.

## 23 - O que é discretizaçao (yk08)

*Discretização* é o processo de colocar valores em buckets de modo que haja um número limitado de possíveis estados.

EM suma, é converter núero discrteos/continuos em intervalos (byuckets)

## 24 - RFV e XPTO (yk11)

É uma classificação em clustering usando 3 items

A classificação leva em consideração três visões de cada cliente da carteira ativa:

- **R – Recência** | O quão recente é a última venda feita para o cliente
- **F – Frequência** | Quantos pedidos o cliente fez num determinado período
- **V – Valor** | Qual o valor do ticket médio dos pedidos do cliente

Serve para conhecer os clientes

## 25 - Método cotovelo e silhueta (clustering (yk10))

São méotodo para determinar mlehor número de clusters no Kmeans

**Método COtovelo - Elbow**

Neste método é preciso rodar seu algoritmo de clustering com alguns valores, por exemplo, de 1 a 10. Calcular a função de custo, a soma dos quadrados das distâncias internas dos clusters, e traçá-la em um gráfico. O melhor número para a quantidade de clusters é quando a adição de um novo cluster não muda significativamente a função de custo. Isso geralmente acontece no "cotovelo" da linha.

**Método Silhueta**

A análise por Silhouette mede o quão bem um ponto se encaixa em um cluster. Neste método um gráfico é feito medindo quão perto os pontos de um cluster estão dos pontos de outro cluster mais próximo. O coeficiente de Silhouette quando próximo de +1, indica que os pontos estão muito longe dos pontos do outro cluster, e quando próximo de 0, indica que os pontos então muito perto ou até interseccionando um outro cluster.

## 26 - O que é ECDFe porque é melhor que histograma (yk12)

https://www.youtube.com/watch?v=_2VDsKU-7SU

## 27 - Livro Ace THe DataScience interview questions

Nâo acho online



## 29 - COHORT (yk20)

A Análise Cohort é uma **métrica focada no cliente**, que nos ajuda a entender o comportamento dos usuários ao longo do tempo. Por essa razão, é uma métrica muito importante não só para o time de Produto, mas também para **[Customer Success](https://www.cursospm3.com.br/blog/customer-success-o-que-e-importancia-como-alinhar-com-produto/)**, que também olha para o **[\*lifetime value\* (LTV)](https://www.cursospm3.com.br/glossario/ltv-lifetime-value/)** dos clientes.

Uma analise de COHORT É: UMA ANALISE DE GRUPOS AO LONGO DO TEMPO OU DE ALGUM VALOR CONTINUO

https://www.cursospm3.com.br/blog/como-fazer-analise-cohort-e-por-que-ela-e-importante-para-pms/?gclid=Cj0KCQjw0IGnBhDUARIsAMwFDLnjFPzM24mRDxI-wED7DFY7YzlulGOa7sFbG3azne_uHIElCFBEoxkaAgn2EALw_wcB

A Análise Cohort funciona **a partir da coleta de dados** sobre clientes, perfis e ações em diferentes [softwares](https://blog.vindi.com.br/mercado-de-software-no-brasil/) utilizados em uma empresa. Por essa razão, ela está fortemente relacionada ao conceito de Big Data — a imensidão de [dados](https://blog.vindi.com.br/gestao-de-dados-em-uma-empresa-saas-qual-software-usar/) que são capturados a todo instante e precisam ser tratados para a realização de análises e obtenção de insights.

Por meio da Análise Cohort, é possível criar **grupos de clientes** com diferentes atributos em comum baseados em uma ação ou período. Eles podem ser agrupados pela participação em uma determinada campanha, por data de início do relacionamento com a empresa, por data da primeira compra e qualquer outro evento que seja de interesse estratégico.

https://blog.vindi.com.br/analise-cohort/

## 30 - O que é pivot-able (yk20)

pivot-table é o group by em Excel

## 31 - Testes KS: Kolmogorov-Sminrnov

O teste de Kolmogorov-Smirnov é um teste de igualdade entre duas distribuições
de probabilidades. Ele pode ser utilizado para comparar a distribuição de uma amostra com uma distribuição de referência ou com outra distribuição de outra
amostra

**Usando KS para saber se houver DataDrift**

Então, vamos focar em comparar a
distribuição de duas amostras. No caso, seria a distribuição dos dados originais
(que o modelo foi treinado) e os dados que temos agora. Dessa forma, podemos
verificar se a distribuição mudou significativamente e, portanto, houve um data
drift.

Quando comparamos essas duas distribuições de amostras distintas, estamos
tentando saber qual é a probabilidade de essas duas amostras pertencerem à
mesma distribuição de probabilidades. E uma vantagem de utilizar esse teste é
que ele é não paramétrico, ou seja, ele não exige que saibamos exatamente qual
é a forma da distribuição dos dados. Isso é extremamente útil porque, na vida
real, muitas vezes não temos informações detalhadas sobre a distribuição dos
dados que estamos analisando.

**Estatistica KS**

A estatística KS vai nos retornar um valor numérico que representa a maior
diferença absoluta entre as distribuições acumuladas das notas. Por exemplo,
se o valor for 0.1, significa que há uma diferença de 0.1 entre as distribuições.
Quanto maior for esse valor, maior é a diferença entre as distribuições, o que
indica que o desempenho dos alunos, ao longo do tempo, sofreu uma modificação
em seu padrão, logo, há uma grande chance de ter ocorrido um data drift.

Para deixar mais simples ainda, imagine que a estatística KS seja uma régua
que mede a diferença entre essas duas distribuições. Quanto mais distante a
régua estiver de zero, maior é a diferença entre as notas antes e depois.

**Usando KS com um teste estatístico**

Ao utilizar essa estatística, podemos fazer um teste estatístico para avaliar se
as duas amostras de notas são realmente diferentes, ou seja, se houve data drift
ou se podem ter mantido o padrão. Para isso, comparamos o valor obtido com um valor crítico (geralmente, 0.05). Se o valor estiver abaixo desses limites, é
bem provável que as notas não possuam a mesma distribuição.

Nossa hipótese nula aqui é que as notas
dos alunos hoje e as notas usadas para treinar o modelo são retiradas da mesma
distribuição. O p-valor nos ajuda a avaliar o quanto os dados que observamos
são compatíveis com o que esperávamos com base em nosso modelo estatístico.
Se o p-valor for muito baixo, isso significa que há uma grande diferença entre os
dados observados e as expectativas do modelo (notas originais). Por outro lado,
se o p-valor for alto, aceitamos a hipótese nula, ou seja, as notas dos alunos hoje
e as notas usadas para treinar o modelo são retiradas da mesma distribuição.

Para calcular esse valor, leva-se em consideração a estatística KS (o valor D)
juntamente com o tamanho das amostras de ambas as distribuições. Os valores
críticos para rejeitar a hipótese nula, ou seja, para dizer que as notas não foram
retiradas da mesma distribuição, são de 1% a 10% (geralmente, utilizamos 5%),
o que significa que qualquer p-valor menor ou igual a esses levaria à rejeição da
hipótese nula.

**COmo fazer em python**

```python
import scipy,stats as stats
import numpy as np

ks_stats = stats.ks_2samp(dado_hoje, dados_originais)
```

Retrna 2 valores

+ A estatistica KS: que é a mair diferneça na ECPF entre os dois grupos de ados
+ O p-valor. 
  + Se p-valor > 0.05 siginfica que  não há evidencias que houve datafrift
  + S p-valor < 0.05 siginfica que com 95% houve datadrift



Serve para comparar se 2 conjuntos de dados tem a mesma distribuição.

Como fazer: Calcula o ECDF dos dosi conjnto e colcoa um do lado do outro

The **general steps to run the test** are:

1. Create an EDF for your sample data (see [*Empirical Distribution Function*](https://www.statisticshowto.com/empirical-distribution-function/) for steps),
2. Specify a parent distribution (i.e. one that you want to compare your EDF to),
3. Graph the two distributions together.
4. Measure the greatest vertical distance between the two graphs.
5. Calculate the test statistic.
6. Find the critical value in the [KS table](https://www.statisticshowto.com/kolmogorov-smirnov-test/#table).
7. Compare to the critical value.

## 32 - DataDrift (yk21)

Data Drifit: Quando a distribuiçao dos dados muda com o tempo, oq ue é algo normal de fazer. VOcê tem que ficar atenteno e verifica isos pois terá impacto no seu modelo em produção.

## 33 - O que é skenss e kurtoise yk21()

https://support.minitab.com/pt-br/minitab/20/help-and-how-to/statistics/basic-statistics/supporting-topics/data-concepts/how-skewness-and-kurtosis-affect-your-distribution/

**skensse**

+ É a asimetria da distribuiçao. pode estár a direita ou esquerada

A assimetria é a medida em que os dados não são simétricos. Valores de assimetria iguais a zero, positivos ou negativos revelam informações sobre a forma dos dados.

![img](https://support.minitab.com/pt-br/minitab/20/media/generated-content/images/histogram_symmetrical_nonskewed_normal.png)

###### Figura A

![img](https://support.minitab.com/pt-br/minitab/20/media/generated-content/images/histogram_symmetrical_nonskewed_nonnormal.png)

###### Figura B

###### Distribuições simétricas ou não assimétricas

Conforme os dados tornam-se simétricos, seu valor de assimetria aproxima-se de zero. A Figura A mostra dados de distribuição normal, que por definição exibe assimetria relativamente pequena. Ao traçar uma linha abaixo do meio deste histograma de dados normais é fácil de ver que os dois lados refletem um ao outro. Mas a falta de assimetria simplesmente não significa normalidade. A Figura B mostra uma distribuição onde os dois lados ainda refletem um ao outro, apesar de os dados estarem longe de serem uma distribuição normal.

![img](https://support.minitab.com/pt-br/minitab/20/media/generated-content/images/histogram_right_skewness_with_arrow.png)

###### Distribuições com assimetria positiva ou à direita

Dados com assimetria positiva ou à direita são assim chamados por causa da "cauda" dos pontos de distribuição à direita, e porque seu valor de assimetria será maior do que 0 (ou positiva). Dados salariais são, frequentemente, assimétricos desta maneira: vários funcionários em uma empresa ganham relativamente pouco, enquanto cada vez menos pessoas ganham altos salários.

![img](https://support.minitab.com/pt-br/minitab/20/media/generated-content/images/histogram_left_skewness_with_arrow.png)

###### Distribuições com assimetria negativa ou à esquerda

Assimetria à esquerda ou dados assimétricos negativos são assim chamados porque a "cauda" da distribuição aponta para a esquerda, e porque ela produz um valor de assimetria negativo. Os dados da taxa de falha são frequentemente assimétricos à esquerda. Considere as lâmpadas: muito poucas vão queimar imediatamente, a grande maioria durará por um longo tempo.

## 34 - O que é Mann-Whitney (yk22)

Em estatística o teste U de Mann-Whitney (também conhecido por teste da soma dos postos de Wilcoxon, teste de Wilcoxon-Mann-Whitney ou teste de Mann-Whitney)[[1\]](https://pt.wikipedia.org/wiki/Teste_U_de_Mann-Whitney#cite_note-1) É um teste não paramétrico aplicado para duas amostras independentes. É de fato a versão da rotina de teste não-paramétrico de *t de Student*.

Se você estiver interessado
em comparar as médias de dois grupos, o Teste de Mann-Whitney U é geral-
mente a melhor escolha.

## 36 - O que é Data Leakeage (yk22)
## 38 - Viés e Variância

**a variância nos diz qual é o erro de um modelo em relação aos dados de teste; o viés, por outro lado, nos diz o quão bem um modelo se adequa aos dados de treino**. 

**1. Modelo linear nos parâmetros**

**2. Média nula e exogeneidade estrita**

**3. Sem multicolinearidade exata**

Na amostra, nenhuma das variáveis explicativas é constante. Não há relações lineares exatas entre as variáveis explicativas. Não exclui alguma correlação (não perfeita) entre as variáveis. De acordo com Gauss e Markov, quando um modelo tem multicolinearidade exata, geralmente é devido a um erro do analista.

**4. Homocedasticidade**

A variância do erro e, portanto, de Y, é independente dos valores explicativos e, além disso, da variância do erro constante. Matematicamente, é expresso como:

![img](https://cdn.economy-pedia.com/7177037/teorema_de_gauss-mrkov_-_qu_es-_definicin_y_concepto_2021_economy-wikicom_5.jpg.webp)

Aqui está uma série de dados com aparência homocedástica.

![img](https://cdn.economy-pedia.com/7177037/teorema_de_gauss-mrkov_-_qu_es-_definicin_y_concepto_2021_economy-wikicom_6.jpg.webp)

**5. Sem autocorrelação**

Os termos de erro de duas observações diferentes condicionais a X não estão relacionados. Se a amostra for aleatória, não haverá autocorrelação.

![img](https://cdn.economy-pedia.com/7177037/teorema_de_gauss-mrkov_-_qu_es-_definicin_y_concepto_2021_economy-wikicom_7.jpg.webp)

## 39 - Premissas de Gauss-Markov para reg. linear

**O Teorema de Gauss-Markov é um conjunto de suposições que um estimador OLS (Ordinary Least Squares) deve cumprir para ser considerado ELIO (Optimal Linear Unbised Estimator).** E**O teorema de Gauss-Markov foi formulado por Carl Friederich Gauss e Andrei Markov.**

Explicadas no material 26 e na live, aos 43 min



1- Linearidade nos paramtros

+ Você está definidio uma equaçâo linear. Basicamente é quando nao aconteece duas coisas:
+ há um a *x (um peso e um varaivel) e 
+ Nôa há nenhum X elevdo ao quadrado (aí vira polinomial)
+ NÃO CORRE x1 * x2 (Nâo ocorre multiplicaçao entre variaveis)
+ Lembrse: Linaer é uma reta, entao a relaçao entre y  e x tem uma ocnstante somente
+ É A PRÓŔIA ESCPEFICIAÇAO DO MODELO. A OLS e a regressao linaer já az isso, entao tome como verdade

2 - Amostragem Aleartpror

+ Geralmente é tomada como verdde, e se a amostra for grnade, peloo teorema geral do s numeros é tambe

3 - Medica condicional do Termo de erro é zero

+ A média do erro é gual a zero, ou seja, se somar todos os erros em que sua linah está abaixo e diminuir pelos erros dos pontos que estao abaixo da linha, devem dar zero. A SOMA DOS ERROS (POSITIVO e negativo) chega perot de zero

4 - Ausencia de Multicolinearidade Perfeita

+ Multicolinearidad: quando a variavel alvo é especlicada cpor uma ou um conjunto de variaveis indetnessepde (feateurse), ou até mesmo multicolinerareide entre as variaviees dependentes X1 é explicado por X2 ou X3 
+ Um exmeplo de multicolinaeiradde ferpeitoa seria fazer o dummy/one-hot-encondig de estaos. Pois cada estado pode ser explicadao pela ausaneic anos outros. Aí é uma multicolinearided perfeita, quando voce consegue prevr completmanete uma variavel com o valos de uma ou mais de outras
+ Voce descobre colineariadde ou multicolinearidde atravez do VIF, se for  maior que 5 é bem provalvem que há uma alta colineriadde
+ Para inferencia, a colineriadde atrapalha porque voce na vai conseguir distinguir direito a causa-efeito das variaveis já que elas se misturam. Se há colinearidade, entoa, é melhor tirar uma delas.
+ No VIF vc analisa uma em relaçao a todas as outras. Se tiver aalgum VIF alto voce tira e aina roda denovo. 
+ O que é o VIF: É fazer uma Regressao para uma varaivel e tratar ela como depdnen das outras (X1 = X2*A + x2*B), aí eu calcula R2 que vai de 0 a 1 que é quase a nota de acerto do modelo. Um R2 alto vai produzir um VIF alto pois a formula é
  + VIF = 1/(1-R2)
  + Retiramos se o VIF for 5 (a variavle é 50% explida pelas outras) ou 10 (é explicada 90%)

5 - Homoscedastidade

+ O err tem que se homogeneo, para valores ALVO tantao muito altos quanto muito baixos  nâo deve dá um eror tão grande assim
+ É quereer que erre igual em todos.. Pois seâo haverá um vies em alum lugar para produzir um erro tao discrepante 

BLUE

+ Se tiver tudo isos, etao seu estimador é BLUE . Voce está dizendo que os coefeicientes sao os melhores possiveis, o mais confiado possível.
+ Para previsão nao chegca nada disos, agora, em inferiencia tem que olhar.
+ Eele está usando o livro do Matheus Fcaure para estudar e aprender e dar auala de inferencecia

## 40 - Inferencia, R  e R2 Ajustado (yk26)

Conforme falamos anteriormente, para que os coeficientes de uma regressão linear sejam
válidos - e, aqui, válido deve ser entendido como o melhor linear e sem viés -, precisamos
garantir 5 premissas: linearidade nos parâmetros, amostragem aleatória, média condicional do
termo de erro igual a zero, ausência de multicolinearidade perfeita e homocedasticidade.
Todas essas premissas foram explicadas detalhadamente na live de 27/05/2023:

 https://youtu.be/5W8xhnL39dw .

## 41 - 
