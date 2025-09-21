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
