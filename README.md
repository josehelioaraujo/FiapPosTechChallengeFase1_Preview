
# Curso 
Pós Graduação de IA para Devs da Fiap 

# Grupo 27
 - RM 355027  - José Hélio Araújo Andrade - helioandrade@hotmail.com
 - RM 356210  - Bernardo Guimarães Tinti - betinti@hotmail.com
 - RM XXXXX   - Thiago Henrique Nunes de Souza - thiagohnds@gmail.com
 - RM XXXXX   - Ana Paula de Sa Lopes de Simone - analopes@correios.com.br 
    
# Entregável
 - Link video de apresentação no Youtube -  A fazer
 - Arquivo Notebook no Colab Versão 1.0 4:   https://colab.research.google.com/drive/1t3tepdSvGgPNjXI3fKD6yaQQoxi_vtND?usp=sharing
 - Github: https://github.com/josehelioaraujo/FiapPosTechChallengeFase1_Preview

# Introdução

Este projeto tem como objetivo a solução de um problema de um modelo preditivo de custo de seguro de saúde, relacionado ao Tech Challenge Fase 1, do curso de Pós Gradução de IA para Devs da Fiap.

# O Problema
Você é um profissional encarregado de desenvolver um modelo preditivo de regressão para prever o valor dos custos médicos individuais cobrados pelo seguro de saúde.
A base de dados para esse desafio pode ser algo como um arquivo CSV contendo os as colunas(idade,gênero,imc, filhos,região, encargos).

Você precisa apenas alimentar ela com mais informações ou utilizar uma outra de sua preferência.

## Tarefas

### Exploração de dados
- Carregue a base de dados e explore suas características.
- Analise estatísticas descritivas e visualize distribuições revelantes.

### Pré-processamento de dados
- Realize a limpeza dos dados, tratando valores ausentes(se necessário)
- Converta variáveis categóricas em formatos adequados para a modelagem.

### Modelagem
- Crie um modelo preditivo de regressão utilizando uma técnica a sua escolha(por exemplo, Regressão Linear, Árvores de Decisão, etc)
- Treinamento e avaliação do modelo:
- Treine o modelo com o conjunto de treinamento.
 
### Validação estatísticas
- Utilize métricas estatísticas para validar a eficácia do modelo(p-value, intervalo de confiança);

### O que avaliaremos
- Apresente resultados visuais, como gráficos de previsões vs valores reais.
- Elabore um relatório que inclua uma análise de resultados, insigts obtidos e validação estatística.

### Observações
- Esperamos que o modelo seja capaz de fazer predições confiáveis dos custos médicos individuais com base nas características fornecidas.


# A Solução implementada
A Solução implementada é composta por 7 partes, e em cada parte são descritas os passos e instruções realizadas.

## Seção 1 - Importando bibliotecas
- Utilizaremos as bibliotecas numpy, pandas, matplotlib, seaborn esklearn.

## Seção 2 - Coleta de dados
Fonte dos dados: https://www.kaggle.com/datasets/mirichoi0218/insurance

O arquivo insurance.csv foi carregado para o ambiente do Google Colab, conforme visto abaixo, por exemplo:
![image](https://github.com/josehelioaraujo/FiapPosTechChallengeFase1_Preview/assets/168944366/42cccbf8-737d-477c-9429-5a831970bd1f)

O dataset é composto pelas seguintes colunas:

- age: idade do beneficiário principal
- sex: gênero do contratante de seguros, feminino, masculino
- bmi: Índice de massa corporal, fornecendo uma compreensão do corpo, pesos relativamente altos ou baixos em relação à altura, índice objetivo de peso corporal (kg/m ^ 2) usando a relação entre altura e peso, idealmente 18,5 a 24,9
- children: Número de filhos cobertos por seguro saúde / Número de dependentes
- smoker: Se tem o hábito de fumar ou não
- region: Localidade residencial do beneficiário nos EUA, nnortheast, southeast, southwest, northwest.
- charges : Os encargos ou custos médicos individuais cobrados pelo seguro de saúde

 Foram realizados as seguintes passos:
 
 - carregando os dados do arquivo csv para um DataFrame do Pandas
 - exibindo nomes das colunas do datase
 - primeiras 5 linhas do dataframe
 - obtendo número de linhas e colunas - existem 1138 linhas e 7 colunas
 - obtendo informações dos data type do conjunto de dados
 - As variáveis categóricas são: sex, smoker e region
 - verificando valores ausentes, e observa-se que não existem
 - verificando se existem linhas duplicadas, e observa-se que existe uma linha
 - removendo linhas duplicadas, e observa-se que agora existem 1337 linhas

## Seção 3 - Análise de dados
- exibindo as medidas estatísticas do dataset
- exibindo quantidades de pessoas  por: idade, exo, imc, filhos, fumante, região
- exibindo os gráficos de distribuição de quantidades de pessoaspor: idade, exo, imc, filhos, fumante, região

## Seção 4 - Pré-processamento de dados
- transformando as variáveis categóricas(sexo, fumante e região) em númericas
- dividindo as variáveis features e target ou alvo(encargos)

## Seção 5 - Treinamento de modelo
Usaremos 3 modelos de predição de regressão linear, e em seguida escolheremos o que teve melhor eficácia, conforme
métricas aplicadas(R2):

### 5.1 Usando o modelo Regressão Linear
    - carregando o modelo de regressão linear
    - fazendo predição de treinamento do modelo de regressão linear
    - predição de treinamento do modelo de regressão linear
    - aplicando métrica R squared

### 5.2 Usando o modelo random forest
   - treinando com dados de treinamento do modelo randon forest
   - fazendo predição do modelo random forest usando os dados de teste
   - aplicando métrica r2 no modelo random forest

### 5.3 Usando o modelo Regressão XGBoost
   - carregando o modelo XGBoost
   - fazendo predição do modelo XGBoost usando os dados de teste
   - aplicando a métrica r2 do modelo xgBoost

### 5.4 Comparação dos modelos usando a métrica R2
  - Exibindo os resultados da métrica R2 para os 3 modelos treinados conforme os tipos utilizados
  - Escolhendo o melhor modelo conforme métrica R2
  - O melhor modelo foi XG Boost com valor R2 0.8662432902515654

  ### 5.5 Gráficos estatísticos - dúvidas perguntar prof. Ana raquel
       - Usar  gráficos estatísticos comparandos como as variáves característos impactam na varável target(encargos)
         Exemplos: Histrogramas, matriz de confusão, etc 
		 
    - Observações: usar lib statmodels.api  Link https://www.statsmodels.org/stable/regression.html
		
	- Estudar assuntos apresentados na mentoria pela prof. Ana Raquel
	 - shapiro,statsmodel,mann whitney u test,p-value e intervalo de confiança, etc

 
## Seção 6 - Conclusões

Conforme a métrica R2 aplicada para os modelos utilizad, o melhor modelo preditivo do valor do custo de seguro, é o modelo XG Boost, conforme tabela exbida abaixo:

- Regressão Linear - R2: 0.7447273869684076
- Random Forest - R2: 0.8370748848709408
- XG Boost - R2: 0.8662432902515654

- etc
- etc
- etc

 
 ### Seção 7 - Testando o modelo construido usando um formulário simples

Usando o form abaixo para selecionar os dados que seráo
usado no cálculo do custo do seguro.

![image](https://github.com/josehelioaraujo/FiapPosTechChallengeFase1_Preview/assets/168944366/4f84b295-8001-470a-acbe-8fc19424d750)


Custo do segurado para os parâmtros abaixo:

Idade: 44

Sexo: Male

IMC: 24.1

Qtde Filhos: 1

Fumante: Yes

Região: Southeast

Custo Seguro(USD): 10091.169
