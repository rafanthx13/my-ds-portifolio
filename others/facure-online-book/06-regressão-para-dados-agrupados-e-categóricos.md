# 06 - Regressão para dados Agrupados e Categóricos



## Regressão para dados Agrupados

O exemplo que vimos no cápitulo 5 (o de prever renda com base nos anos de educaçâo e etc) nós tinhamos o caso onde viamos todos os dados apra caa indivíduo.

Acntece que esse tpo de coisa énão é tão provavel quanto gostariamos.

Por exmeplo, no caso das notas do ENEM, nã temos  dados por estudadnote, e sim dados por escola.

**OS DADOS ESTÃO AGRUPADOS**

### Heterocedasticidade

![](https://matheusfacure.github.io/python-causality-handbook/_images/06-Grouped-and-Dummy-Regression_2_0.png)

Heterocedasticidade: Ocorre quando a variancia não constante para todo o conjunto de daos.

+ No exemplo dos dados do ENEM: Quanto mais alunos tem, menos registro tem no nosso dataset

E isso tem impacto sobre a confiança do dado:

+ Quanto menor a variância, mais confinça temos
+ No caso do ENEM
  + O ponto Amarelo não é tã confiavel. Aquela nota é alta, mas, para essa faixa de número de estudante, tende a ser mais baixa entre 40 e 60 de score
  + Agora o ponto vermelho é confiável porque não tem mais dados para comparar

### Como lidar com dados agrupados

Para lidar com dados agrupados e fazemros a mesma regresosa linear do cap , o que precisamos é de:

==> **MÉDIA e QUANTIDADE DE REGISTROS**

E entâo aplciadmos a regressão linear usando pesos que variam de acordo com a quantidade de registro spra cada grupo

```python
model_2 = smf.wls('lhwage ~ educ', data=group_wage, weights=group_wage["count"]).fit()
model_2.summary().tables[1]
```

A estimativa encontrada 'proxima da que seria se os dados nâo tivessem agrupados.

**Porque usar pesos**

+ Poruqe, sem pesos, daria mais ao ponto amarelo do que devria (e deveria ser pouco já que é um outlier)

> Para usar a regressão ponderada, você precisa de estatísticas médias. Não somas, nem desvios padrão, nem medianas, mas médias! Tanto para as covariáveis quanto para a variável dependente. Apenas tenha em mente que o resultado da regressão ponderada com dados agrupados não corresponderá exatamente ao da regressão em dados desagrupados, mas será bastante semelhante.

## RegresSâo cm categorical features

Geralmente variaveis one-hot-encoding



## Key Ideais

Começamos esta seção observando como alguns pontos de dados são mais importantes que outros. Ou seja, aqueles com maior tamanho de amostra e menor variância devem receber mais peso ao estimar um modelo linear. 

Em seguida, vimos como a regressão linear pode até lidar com dados anonimizados agrupados com elegância, desde que usemos pesos amostrais em nosso modelo.

Em seguida, passamos para a regressão fictícia. Vimos como é possível criar um modelo não paramétrico que não coloque quaisquer suposições sobre a forma funcional de como o tratamento impacta o resultado. 

Em seguida, exploramos a intuição por trás da regressão fictícia.