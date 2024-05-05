
# Curso 
Pós Gradução de IA para Devs da Fiap 

# Aluno
 - RM 355027 - José Hélio Araujo Andrade  - helioandrade@hotmail.com
    
# Entregável
 - Link video de apresentação no Youtube -  A fazer
  - [Arquivo Notebook - versão preview](https://colab.research.google.com/drive/1t3tepdSvGgPNjXI3fKD6yaQQoxi_vtND#scrollTo=FqU3kmaXY6XB) 

# Introdução

Este projeto tem como objetivo a solução de um problema de um modelo preditivo de custo de seguro de saúde, relacionado ao Tech Challenge Fase 1, do curso de Pós Gradução de IA para Devs da Fiap.

# O Problema
Você é um profissional encarregado de desenvolver um modelo preditivo de regressão para prever o valor dos custos médicos individuais cobrados pelo seguro de saúde.
A base de dados para esse desafio pode ser algo como um arquivo CSV contendo os as colunas(idade,genero,imc, filhos,regiao, encargos).

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
-cUtilize métricas estatísticas para validar a eficácia do modelo(p-value, intervalo de confiança);

### O que avaliaremos
- Apresente resultados visuais, como gráficos de previsões vs valores reais.
 - Elabore um relatório que inclua uma análise de resultados, insigts obtidos e validação estatística.

### Observações
- Esperamos que o modelo seja capaz de fazer predições confiáveis dos custos médicos individuais com base nas caractéricas fornecidas.


# A Solução implementada
A Solução implementada é composta por 5 partes:

## Seção 1 - Importando bibliotecas
- Utilizaremos as bibliotecas numpy, pandas, matplotlib, seaborn esklearn.

## Seção 2 - Coleta e análise de dados
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

## Seção 3 - Análise de dados

## Seção 4 - Pré-processamento de dados

## Seção 5 - Treinamento de modelo

## Seção 5 - Conclusões

