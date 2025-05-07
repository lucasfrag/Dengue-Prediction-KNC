# Previsão de casos de dengue com KNN

Durante minha Pós-Graduação em Inteligência Artificial, fui desafiado a desenvolver uma solução para prever casos de dengue utilizando o algoritmo K-Nearest Neighbors. O projeto parecia complicado no início, mas com muita pesquisa e dedicação, consegui implementar uma solução eficaz!

### 💻 O que foi feito?

- Carreguei e transformei dados categóricos de uma base de casos de dengue.
- Apliquei técnicas de Machine Learning com Python, Pandas e scikit-learn.
- Treinei um modelo de classificação utilizando KNeighborsClassifier.
- Avaliei o desempenho com matriz de confusão e acurácia.



### 📚 Por que isso importa? 

A previsão de doenças como a dengue é crucial para a saúde pública, e aplicar Machine Learning nessa área pode trazer insights poderosos e ajudar na tomada de decisões.


🔗 Confira o artigo completo no [Medium](https://medium.com/@lucasfrag/previsão-de-casos-de-dengue-com-inteligência-artificial-58a146c445e6)



## O problema... 🤔
<i>O texto abaixo trata-se do contexto apresentado para a prática do Projeto Integrado.</i> 💬 

1) Para realizarmos um projeto de mineração de dados, o primeiro é selecionar a base de dados e explorar dos dados desta base, no intuito de obtermos um entendimento inicial sobre o problema. Diante disto, utilize a biblioteca Pandas do Python para criar um <i>Data Frame</i> a partir da base de dados da dengue disponibilizada e exiba os 5 primeiros elementos deste conjunto usando o comando <i>head()</i>.

2) O segundo passo de um projeto de mineração de dados é o da transformação dos dados para posterior utilização no modelo de aprendizagem. 
Para o problema de diagnóstico da dengue será utilizado o modelo <b>K-Nearest Neighbors</b>. Para usar este modelo, transforme os registros que possuem os valores ‘sim’ e ‘nao’ da base de dados da dengue em binários 1 e 0, respectivamente. Exiba os registros atualizados utilizando o comando head() da biblioteca Pandas.

3) Logo após a transformação, tem-se, finalmente, o passo de mineração de dados. Para esta etapa, divida a base de dados da dengue em treinamento e teste. Logo após, selecione o algoritmo <i>K-Nearest Neighbors()</i>, utilize o comando fit para treinar o modelo e o comando predict para aplicar o método de predição. 
Apresente a matriz de confusão e a acurácia do modelo.  


## ... A SOLUÇÃO! 😍


### 1. Transformação dos Dados

Os valores nas colunas `dor_muscular`, `falta_apetite`, `manchas_vermelhas` e `dengue` são categóricos, com valores 'sim' e 'nao'. Para utilizar esses dados em um modelo de machine learning, foi necessário transformar esses valores em binários:

- `'sim'` foi substituído por `1`.
- `'nao'` foi substituído por `0`.

### 2. Divisão dos Dados

Após a transformação, os dados foram divididos em conjuntos de treinamento e teste. O conjunto de treinamento é utilizado para treinar o modelo, enquanto o conjunto de teste é usado para avaliar seu desempenho.

### 3. Treinamento do Modelo

O modelo `K-Nearest Neighbors` foi treinado usando os dados de treinamento. Este algoritmo classifica novos exemplos com base nas classes mais frequentes entre os vizinhos mais próximos.

### 4. Avaliação do Modelo

O modelo foi avaliado usando a matriz de confusão e a acurácia.

#### Matriz de Confusão

A matriz de confusão gerada foi:

<table>
  <tr>
    <th></th>
    <th>Previsto: Não Dengue</th>
    <th>Previsto: Dengue</th>
  </tr>
  <tr>
    <td>Real: Não Dengue</td>
    <td>2</td>
    <td>1</td>
  </tr>
  <tr>
    <td>Real: Dengue</td>
    <td>0</td>
    <td>1</td>
  </tr>
</table>


- **True Negatives (2)**: Pacientes que realmente não tinham dengue e foram corretamente classificados como "não dengue".
- **False Positives (1)**: Paciente que não tinha dengue, mas foi incorretamente classificado como tendo dengue.
- **False Negatives (0)**: Pacientes que tinham dengue, mas foram incorretamente classificados como "não dengue".
- **True Positives (1)**: Pacientes que realmente tinham dengue e foram corretamente classificados como "dengue".

#### Acurácia

A acurácia do modelo foi de **75%**. Ela é calculada como a proporção de previsões corretas (True Positives + True Negatives) sobre o total de previsões:

<code>Acurácia = ( 2 + 1 ) / 4 = 0.75</code>

Isso significa que o modelo acertou 75% das previsões no conjunto de teste.




## Capturas de tela 📸

<b>1. Carregar a base de dados seleciona e explorar os dados</b><br>
<img src="https://github.com/lucasfrag/UNA-PI-IA/blob/main/Screenshots/Screenshot_01.jpg" style="width: 800px">

<b>2. Transformar os valores da base de dados</b><br>
<img src="https://github.com/lucasfrag/UNA-PI-IA/blob/main/Screenshots/Screenshot_02.jpg" style="width: 800px">

<b>3. Mineração de dados</b><br>
<img src="https://github.com/lucasfrag/UNA-PI-IA/blob/main/Screenshots/Screenshot_03.jpg" style="width: 800px">


## Construído com...
- Python
- Pandas
- scikit-learn

## Conclusão
Este projeto demonstra como aplicar o classificador K-Nearest Neighbors para diagnosticar dengue com base em sintomas registrados em uma base de dados. A acurácia obtida foi de 75%, o que indica um desempenho razoável para este conjunto de dados simples.



