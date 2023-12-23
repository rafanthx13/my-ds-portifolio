# Yuki Stories - Pack 1

## Comapra Candidatos regulares com asinantes

Candidatos regulares: "Regressão linear é para obter causalidade entre x e y", "aí se tiver multicolinearidade a regressão tem predições prejudicadas", "eu aplico um scaler e one hot encoder, depois rodo uma árvore de decisão", "se tiver 
richchribr.chrirtMN. SMOTE resolve" 

Candidatos do Clube de Assinaturas: "Regressão linear não implica em causalidade, precisaríamos de um desenho específico para aí aplicar um modelo em painel", "multicolinearidade não afeta predições", "não preciso de scaler para árvores e one hot encoder vai prejudicar meu modelo", "desbalanceamento é, na maioria dos casos, uma questão de trade off, mas eu ainda mexo no peso das classes, no threshold da probabilidade e escolho a loss function ideal" 

Candidatos da mentoria de 3 mil reais: "MaS o MeU mEnToR diSsE qUe Eu NãO pRecISAva SaBER PytHoN oU MaChINe LEArNING" >,v)< 

## Target ENcodign (3 stories)

Lembra que eu falei para tomar cuidado com o OnE Hot Encoder? Além dele penalizar sua árvore, ele pode ser ruim mesmo para outros algoritmos quando tem muitas categorias diferentes na coluna. Uma das alternativas que eu mais recomendo aos meus alunos é o TARGET ENCODI NG

O target encoder, também conhecido como mean target encoder, é uma técnica de codificação de variáveis categóricas que é frequentemente usada em problemas de machine learning. A ideia básica por trás do target encoder é substituir as categorias de uma variável categórica pela média (ou outra estatística) do valor de destino correspondente para cada categoria. 
Por exemplo, suponha que temos uma variável categórica "Cor" e queremos prever o preço de um carro. Podemos calcular a média dos preços de carros para cada categoria de cor (por exemplo, vermelho, azul, verde) e substituir cada categoria pela média correspondente. Isso cria uma representação numérica da variável categórica que leva em consideração a relação com o valor de destino (neste caso, o preço). 

A vantagem do target encoding é que ele captura informações relevantes sobre a variável categórica em relação ao target. No entanto, é importante ter cuidado ao usar essa técnica, pois pode causar iffl problemas de overfitting, já que rola um target leakage (vc vaza informações do target para a feature). Para minimizar os riscos, use cross validation, split em treino-teste-validação, lembre-se de aplicar fit_transform apenas no treino e veja se cabe alguma regularização. 

**Passando para lembrar que pré-processamento, seja tratamento de missing, encoder ou scaler, é SEMPRE após a divisão em treino e teste! Sempre!**

## Precision x Recall


Em problemas desbalanceados,1 na maioria das vezes, a decisão é sobre qual métrica priorizar. 
Veja, nós temos duas métricas importantes na classificação: 

+ Precision = TP / (TP+FP)
+ Recall = TP / (TP* FN) 
+ TP = verdadeiro positivo 
+ FP = falso positivo FN = falso negativo 

Ou seja, o precision vai dizer: de todos que seu modelo disse que era verdade, quantos realmente eram. Enquanto o recall diz: de todos que sao verdade, quantos meu modelo acertou. 

Se liga na sutileza da parada, se vc prioriza precision é porque vc tem que acreditar no que seu modelo ta dizendo. Já no caso de recall, é porque vc quer pegar a maior parte dos eventos iguais a 1. 
Pensa num problema que inadimplência é o target igual a 1. Se vc priorizar precision, significa que vc quer garantir que quem o seu modelo disse que não vai pagar, realmente não paga. Ja no caso do recall, vc quer pegar a maior parte dos caloteiros. 
E olha que diferença, se vc prioriza precision, seu modelo vai acertar quem ele disse que é inadimplente, mas pode ser que tenha varios inadimplentes que ele deixou de fora. Ou seja, pode ter muitos falsos negativos. Se vc priorizar recall, vc vai pegar varios inadimplentes, mas pode acabar colocando adimplentes no bolo da previsão, ou seja, muitos falsos positivos. 

Veja como priorizar a métrica errada pode ser problematico. Imagina que vc quer prever os inadimplentes e prioriza o precision. Ou seja, quando seu modelo disser que é inadimplente, é porque é mesmo! Agora, isso não quer dizer que seu modelo tenha pego todos inadimplentes. Ou seja, sua ação de cobrança baseada no modelo vai deixar um monte de inadimplente passar! Prejuízo!! 

Por outro lado, vamos pensar num problema do direito onde vc quer prever se uma pessoa é culpada. Só que aí vc acabou priorizando o recall. Ou seja, vc quer pegar o maximo de culpados possível. Porém, ao priorizar o recall, vc negligenciou os falsos positivos. Em outras palavras, vc ta prendendo um monte de inocente, que é bem mais grave! 

Entende agora como é importante num problema saber bem o que priorizar? Busque sempre medir qual a ponta que causará mais dano. É claro que a gente nunca é maluco de priorizar muito uma metrica e ignorar outra, mas ainda é necessario saber qual o lado a ser priorizado! 
