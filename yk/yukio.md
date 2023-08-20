# Yukio (Notas de maio a julho de 223)

https://docs.google.com/document/d/1PafszGngnmfcolkjHqILyT_dvo9uul3P1XKI-ejLvH4/edit?usp=sharing

## Videos


(28/03/2023)
+ ML e usando ChatGPT Link do 1° encontro, sobre portfólios: https://youtu.be/-_Nn1O6ZAgo
+ Link do 2° encontro, sobre machine learning usando chatGPT: https://youtu.be/hS1uTbQtQ9c

29/05/2023
Gravação da aula de Regressão Linear voltada para inferência: https://youtu.be/5W8xhnL39dw (1h24min)

## Esse projeto ficou show

https://github.com/Sampaio-Vitor/projeto_olx

## Index

## CUrsos que recomenda

+ DO ITA
+ do instagram @asn.rocks

## Quem seguir

+ Casseie Kozyrkov

## Livros

Recomendaçoes random
+ Think Bayes: Baysian Statistic in Pytohn
+ COmo mentri com estatitiscas - Darrel Huff
+ Analise pratica de séries temporias: Prediçao com estatisica e Aprendizado de maquina
+ O andar do bebado
+ Projetos de ciencia de dados com python - Stephen Klosterman
+ Freakcnomics
+ sem esforço: ele segue a rica para adminstrar o seu tempo
+ Analise d edados - Favero
+ Estatistica com CD Moretin
+ Pratical Data Science with Python
+ Factfulness
+ Prob: Curso moenro - Sheldon oss
- Estatistica basica - Bussab
+ O poder dos quietos

## meetup

Os do nubank

## Aprendez

+ Matematica e Estatisica
  - Calculo e Algebra linear da khan academy
  -  "Mathematics for Machine Lerning do Marc Peter Deseniroth
  - Estatistica - O que é e pra que serve - Charles Wheelan
  - AN introduction to Statisticla Learning - Gareth James (eu tenho)
+ Probabildiade
  - Noçoes de probabilidde e estatisca - Marcos Nascimento Magalhaes
  - Probabildiade: Um curso moderno com aplicaçoes do Sheldon ROss
  - PLayLis JB Statitsc sobre distribuiçoes e tesse de hiptese
+ SQL Avançado
  - SQL For Smarties (downloadded)
  - Advanced SQL Programing 
  - The art of SQL (downloadede)
  - SQL in Nutshell (mais apra iniciante do que os outros mas pode surpreender)
+ Aprender alg de ML
  - StatQuest with Josh Stamer
+ INferencia de causa
 - Casual INferen and discovery in pytohn

## A minha pergunta

Qual conceito de Estatíst você ahca improtante mas poucas pesosa relamnete ententem

Khan Academy - A ideia por tra do teste de hipotese

## Post interressantes

+ lnkd.in/djCw_xHU (Linkedin da pessoa - Matheus de ALmeida Cantarutti)

## Artigos

+ Porque modelos ensemble sao melhores que redes neuris para dados tabulares
=> arxiv.org/pdf/2207.08815.pdf
=> Why do three-based models still outperform deep learning on tabular data

+ Paper do CHat GPT
  - Attention is all you need

## Para portifolio

+ USE DADOS REAIS QUE NAO SEJA DA KAGLGE OU FEITO POR PIPELINE POR VOCÊ

## O que é entropia

Entropia é uma medida de incerteza. Qunato mais incerteza, mais entropia, ou seja pod ser tabembem medida de variabildaide dos dadoas

##  MALHAR isntagram

@jovi.treinador; _sciencefitness; edu_limocelli; jeffnippard; corpo.ciencia

## Teiter

Está salvo em listas:

Ylecun; Marktenenhjoltz; Diegocortiz; Geoffreyhinton; Dalianaliu; MetaAI; Jeffdean; Goodfellow_ian; Chelseabfinn; Becomingdatasci; Rphlbruce; Lucaswarwar; Karrem_carr

## Difenreça entre quem faz o clube de quem nao faz

Candidatos regulares: 
+ "Regressão linear é para obter causalidade entre x e y", 
+ "aí se tiver multicolinearidade a regressão tem predições prejudicadas", 
+ "eu aplico um scaler e one hot encoder, depois rodo uma árvore de decisão", 
+ "se tiver desbalancamento SMOTE resolve" 

Candidatos do Clube de Assinaturas: 
+ "Regressão linear não implica em causalidade, precisaríamos de um desenho específico para aí aplicar um modelo em painel", 
+ "multicolinearidade não afeta predições", 
+ "não preciso de scaler para árvores e one hot encoder vai prejudicar meu modelo", 
+ "desbalanceamento é, na maioria dos casos, uma questão de trade off, mas eu ainda mexo no peso das classes, no threshold da probabilidade e escolho a loss function ideal"

## Análise dos conteudos

- 03 - Onceitos teoricos importantes
- 05 - Video de 1h de calssificaçao
- 06 - Matplotlib interativo usando plotly nativamente no pandas
- 07 - Erros 1 e 2 + trade-off precission e recal
- 09 - + tecnico como fazer feaure-selection de formas muito legais
- 10 - PRICINGA (!!!!) ASSISITR
- 11 - RFC (Recencia, fereuqneic avalor) (!!! Executar) + EXEMPLO DE MELOR PORTIGOLIO QUE ELE JA VIU
- 13 - COmo ir bem em entrevista de Data Science
- 20 - COHORT com dataset da kagle
- 19, 22, e 23 - COmo fazer EDA de Ponta

## Casual Inferencin in Python

Serve para: Quando você precisa saber o impacto ao altera algo que você tem cotrnole sobre alumga métrica que você qestá investifgando ou quer infleunciar.

O livro é uma introduçao a inferencia casual

git: matheusfacure/casual-inference-in-pytohn-code

A grande questâo é: associaçao nao é causa.

Você pode por exemplo dizer que há uma associaçao entre os numero s de premios nobel de um pis como o consuo de chocolate per-capita (suiça), MAS ISSO Não é causa

Para que serve: Você quer saber as relaçôes de causa e efeito para você intervir e causar um efeito desejado. Entender s impactos que um interveçao de uma variavel faz, e prever isso.

ML nisso: Esas perguntas de inferecnia causual estâo mais apra. "E se eu mexer X  para X + c, qual o impacto dem Y.
+ ML é bom para fazer predição
+ ML usa associaço para predixer as coisas
+ Ela funciona bem  dede que você não altera as variaveis usadas apra a prediçao.
+ Muitos DSs sabem as ferramentas de ML mas nada de inferencia casual, que tratam coisa completamente difetnes.
  - Exemplo: Um dos objetivos de uma empresa é aumentar as vendas ou uso de serus serviços. Modelos de ML podem apenas prever as vendas em alguns casos, com falha, e ainda usadnso dados passadoas. Pode até mesmo conculir coisa non-sense.
+ Nâo sginifica que nâo serve, mas que deverá ter que usar ML por um outro anguçp. Tatno que na parte 3 vamos vr como ufazer isso com decision tree.


