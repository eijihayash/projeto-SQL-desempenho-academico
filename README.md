# Projeto SQL Desempenho Academico

## 1. Introdução

Este projeto tem como objetivo analisar o desempenho acadêmico de alunos a partir de um dataset contendo informações pessoais, acadêmicas e de hábitos de estudo.  

O trabalho foi dividido em duas etapas principais:  
- **Limpeza dos dados crus**  
- **Análises exploratórias em SQL**  


----------------------------------------------------------------------------------------------------------------------------------------------------------------------


## 2. Limpeza dos Dados

Os dados originais apresentavam inconsistências e ruídos que precisavam ser tratados. Algumas ações principais foram:  

- **Padronização de nomes**: substituição de caracteres especiais (`ø → o`, `æ → ae`, `ü → u`).  
- **Uniformização de gênero**: convertendo abreviações (`M`/`F`) para `Male` e `Female`.  
- **Residência**: agrupando residências diferentes em três categorias — `Private`, `Sognsvann`, `BI Residence`.  
- **Educação anterior**: corrigindo erros de digitação como `HighSchool → High School`, `Diplomaaa → Diploma`, `Barrrchelors → Bachelors`.  
- **Notas inválidas**: substituindo valores nulos/vazios em `Python` por `0` e garantindo que todas as notas estivessem entre `0 e 100`.  

**Resultado**: foi criada a tabela `student_dataset_cleaned`, servindo como base confiável para as análises.


----------------------------------------------------------------------------------------------------------------------------------------------------------------------


## 3. Análises Exploratórioas e Insights

**Distribuição de alunos por país**

Mais de 60% dos alunos são da Noruega, mostrando predominância de um país no dataset.

**Idades dos alunos**

O aluno mais jovem tem 21 anos e o mais velho 71 anos, com média de 35 anos.

**Gênero**

- **55%** são mulheres
- **44%** são homens

**Residência**

- **42%** são da Private
- **41%** da BI Residence
- **15%** da Sognsvann

**Desempenho acadêmico médio**

- Média em Python: **75**
- Média em Banco de Dados: **69**

Mulheres tiveram nota levemente superior em Python, mas os homens se saíram melhor em Banco de Dados.

**Ranking dos alunos**

- Top 10 da média (Python + DB) contém 5 homens e 5 mulheres
- Média de idade do Top 10: 36 anos

**Educação anterior x desempenho**

Alunos com **Masters** e **Bachelors** apresentam as melhores notas médias em Python e Banco de Dados.

**Horas de estudo x desempenho**

- Quanto maior o tempo de estudo, maior a média das notas.
- Alunos com mais de 150 horas apresentaram os melhores desempenhos.

**Faixa etária x desempenho**

- Alunos entre **25-45** anos apresentam melhor desempenho.
- Alunos com menos de **25** anos ficam abaixo da média.

**Residência x desempenho**

Alunos de **Sognsvann** apresentam médias ligeiramente superiores em comparação com outras residências.

**Notas vs exame de entrada**

Cerca de **25%** dos alunos superaram a nota do exame de entrada.

**Alunos que estudaram muito mas não performaram bem**

**23%** dos alunos que estudaram mais de 150 horas ficaram abaixo da média, mostrando que tempo de estudo sozinho não garante desempenho.


----------------------------------------------------------------------------------------------------------------------------------------------------------------------


**Quartis de desempenho**

Ao dividir os alunos em 4 quartis, conseguimos visualizar os melhores e piores desempenhos do dataset.

## 4. Conclusão

O projeto revelou que educação anterior, idade e tempo de estudo influenciam significativamente o desempenho acadêmico.
Contudo, exceções existem, como alunos que estudaram muito e ficaram abaixo da média, reforçando a importância de analisar múltiplos fatores ao mesmo tempo.
