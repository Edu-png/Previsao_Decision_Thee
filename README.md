<p align="center">
  <a href="https://github.com/Edu-png">
    <img src="https://img.shields.io/badge/Autor-Eduardo%20Coqueiro-purple?style=flat&logo=github" alt="Autor">
  </a>
  <a href="mailto:eduardocoqueiro@gmail.com">
    <img src="https://img.shields.io/badge/Email-eduardocoqueiro%40gmail.com-purple?style=flat&logo=gmail" alt="Email">
  </a>
  <a href="https://linkedin.com/in/eduardocoqueiro/">
    <img src="https://img.shields.io/badge/LinkedIn-Eduardo%20Coqueiro-purple?style=flat&logo=linkedin" alt="LinkedIn">
  </a>
  <a href="https://kaggle.com/EduardoCoqueiro">
    <img src="https://img.shields.io/badge/Kaggle-Eduardo%20Coqueiro-blue?style=flat&logo=kaggle" alt="Kaggle">
  </a>
</p>

![CAPAS - PROJETOS (2)](https://github.com/user-attachments/assets/2c349ae3-3892-478d-94c7-b0ec6b34a162)

# Pipeline do processamento dos dados 🎲
![CAPAS - PROJETOS (3)](https://github.com/user-attachments/assets/8c9a0f99-f07f-45fb-b3a3-777bfd4e96ef)

## 📋 Sumário

1. [Problema de Negócio](#-problema-de-negócio)
2. [Dados](#-dados)
3. [Ferramentas e Bibliotecas](#-ferramentas-e-bibliotecas)
4. [Análise Exploratória de Dados (EDA)](#-análise-exploratória-de-dados-eda)
5. [Pré-processamento de Dados](#-pré-processamento-de-dados)
6. [Modelagem](#-modelagem)
7. [Ajuste de Hiperparâmetros](#-ajuste-de-hiperparâmetros)
8. [Validação e Resultados](#-validação-e-resultados)
9. [Exportação do Modelo](#-exportação-do-modelo)
10. [Como Executar o Projeto](#-como-executar-o-projeto)
11. [Contribuição](#-contribuição)
12. [Referências](#-Referências)


# 🏦 Previsão de Investimentos Bancários com Machine Learning usando Decision Tree

Este projeto foi desenvolvido por Eduardo Coqueiro como parte dos estudos na plataforma ALURA. O objetivo principal é prever se os clientes de um banco irão aderir a uma oferta de investimento com base em características demográficas e comportamentais, utilizando técnicas de Machine Learning.

## 📊 Problema de Negócio

A previsão da adesão a investimentos é crucial para o sucesso das campanhas de marketing bancário. A capacidade de prever se um cliente potencialmente investirá ou não pode otimizar os recursos da empresa e aumentar as taxas de conversão. Isso permite que os bancos direcionem melhor suas estratégias de marketing, economizando recursos e maximizando o retorno sobre o investimento.

## 📚 Dados

Os dados utilizados neste projeto foram extraídos de uma campanha de marketing bancário e contêm as seguintes características:
- **Idade**: Idade do cliente.
- **Estado Civil**: Estado civil do cliente (Solteiro, Casado, Divorciado).
- **Escolaridade**: Nível de escolaridade do cliente.
- **Inadimplência**: Indica se o cliente já foi inadimplente.
- **Saldo Bancário**: Saldo bancário do cliente.
- **Número de Contatos**: Número de contatos feitos durante a campanha.
- **Tempo desde o Último Contato**: Tempo em dias desde o último contato com o cliente.
- **Aderência ao Investimento**: Indica se o cliente aderiu ou não à oferta de investimento.

## 🛠️ Ferramentas e Bibliotecas

Para a análise e modelagem dos dados, foram utilizadas as seguintes ferramentas e bibliotecas:

- **Python**: Linguagem de programação principal utilizada no projeto.
- **Pandas**: Para manipulação e análise de dados.
- **Scikit-learn**: Biblioteca para aprendizado de máquina, usada para construção e avaliação dos modelos.
- **Plotly**: Ferramenta de visualização interativa utilizada para criar gráficos.
- **Matplotlib**: Biblioteca usada para criar visualizações estáticas dos dados.

## 🔍 Análise Exploratória de Dados (EDA)

Antes de iniciar a modelagem, foi realizada uma análise exploratória dos dados (EDA) para compreender melhor a distribuição das variáveis e identificar possíveis inconsistências. Durante essa fase, foram gerados gráficos como histogramas e boxplots para cada variável:

### 📊 Gráficos de Distribuição

- **Estado Civil vs. Aderência ao Investimento**: A distribuição dos clientes casados apresentou uma maior tendência a não aderir ao investimento.

![Estado Civil vs. Aderência ao Investimento]![newplot (5)](https://github.com/user-attachments/assets/a4bfa366-ce5f-4303-918a-45a391842b26)

- **Escolaridade vs. Aderência ao Investimento**: Clientes com escolaridade média foram os que mais aderiram ao investimento.

![Escolaridade vs. Aderência ao Investimento]![newplot (6)](https://github.com/user-attachments/assets/f374dccf-5b39-4219-99d8-4cab6fd13c6f)

- **Fez Empréstimo vs. Aderência ao Investimento**: A maioria dos clientes que não fez empréstimo não aderiu ao investimento.

![Fez Empréstimo vs. Aderência ao Investimento]![newplot (7)](https://github.com/user-attachments/assets/a4237e68-ee99-4915-a8e5-6d50b5c375b8)


## 🧹 Pré-processamento de Dados

Para preparar os dados para a modelagem, foram realizados os seguintes passos:

1. **Transformação de Variáveis Categóricas**: As variáveis categóricas foram transformadas em variáveis numéricas usando OneHotEncoder.
2. **Conversão da Variável Alvo**: A variável alvo (Aderência ao Investimento) foi convertida em formato numérico utilizando LabelEncoder, essencial para que os modelos de Machine Learning possam processá-la.
3. **Divisão de Dados**: Os dados foram divididos em conjuntos de treino e teste para avaliação dos modelos.

## 🤖 Modelagem

Três modelos de classificação foram testados para prever a aderência ao investimento:

1. **Dummy Classifier**: Utilizado como baseline para comparação. Obteve uma acurácia de 60%, indicando que a maioria das previsões eram simples e baseadas em heurísticas básicas.
   
2. **Decision Tree**: A Decision Tree obteve um desempenho significativamente melhor, com uma acurácia de 74% após ajustes de hiperparâmetros.

![Árvore de Decisão]![download](https://github.com/user-attachments/assets/9ba539f9-3b2b-439f-a554-1d82b9529f3a)

   
3. **K-Nearest Neighbors (KNN)**: Testado como alternativa, o KNN obteve uma acurácia de 68%, inferior à Decision Tree.

## 📈 Ajuste de Hiperparâmetros

Para melhorar o desempenho do modelo de Decision Tree, utilizamos o GridSearchCV para ajustar os principais hiperparâmetros:

- **max_depth**: Determinamos que a profundidade ideal da árvore é 3, equilibrando entre complexidade e capacidade de generalização.
- **min_samples_split**: Ajustado para 2, o que melhorou a acurácia e a estabilidade do modelo.

## 🧪 Validação e Resultados

### 1. Modelo Baseline
   - **Dummy Classifier**: Utilizado como modelo de referência, o Dummy Classifier obteve uma acurácia de **60%**. Esse resultado serve como um benchmark para avaliar a eficácia dos modelos mais complexos.

### 2. Modelo de Árvore de Decisão (Decision Tree)
   - **Acurácia Inicial**: Após o treinamento inicial, o modelo de Decision Tree alcançou uma acurácia de **66%** no conjunto de teste.
   - **Ajuste de Hiperparâmetros**: Utilizando GridSearchCV, os parâmetros como `max_depth` e `min_samples_split` foram otimizados. Após esses ajustes, a acurácia do modelo aumentou para **74%**.
   - **Interpretação do Modelo**: A visualização da árvore de decisão indicou que variáveis como `tempo desde o último contato`, `idade`, e `escolaridade` foram determinantes para prever a adesão ao investimento.

### 3. Modelo K-Nearest Neighbors (KNN)
   - **Acurácia**: O modelo KNN, após a normalização dos dados, obteve uma acurácia de **68%**. Embora tenha superado o Dummy Classifier, o desempenho foi inferior ao modelo de Decision Tree.

### 4. Comparação de Modelos
   - **Melhor Modelo**: O modelo de Decision Tree foi identificado como o mais eficaz, com uma acurácia final de **74%**, superando tanto o Dummy Classifier quanto o KNN.
   - **Validação Cruzada**: A validação cruzada do modelo de Decision Tree mostrou estabilidade, com baixo desvio padrão nas acurácias das diferentes divisões dos dados.

### 5. Aplicabilidade
   - **Impacto Potencial**: Com uma acurácia de **74%**, o modelo de Decision Tree se mostrou útil para ajudar bancos a direcionar campanhas de marketing com maior precisão, otimizando recursos e aumentando as taxas de conversão em ofertas de investimento.

A validação cruzada (cross-validation) foi realizada para garantir a robustez do modelo de Decision Thee: 

- **Acurácia Média**: 74%
- **Desvio Padrão**: O modelo demonstrou estabilidade, com baixo desvio padrão nas acurácias das diferentes divisões dos dados.

![Aderência ao Investimento]![newplot (4)](https://github.com/user-attachments/assets/d98f0b26-74ee-4039-8d32-cf1d8ed19fd2)


## 📦 Exportação do Modelo

Finalmente, o modelo treinado foi exportado para uso em produção, utilizando a biblioteca `pickle`. Isso permite que o modelo seja carregado e usado para previsões em outros ambientes que não sejam o Google Colab.

      ```python
      import pickle
      
      with open('modelo_arvore.pkl', 'wb')  as arquivo:
          pickle.dump(arvore, arquivo)
        ```

## 🚀 Como Executar o Projeto

1. Clone o repositório:

```python
  git clone https://github.com/seu-usuario/previsao-investimentos-bancarios.git
```

2. Instale as dependências:

```python
pip install -r requirements.txt
```

3. Execute o notebook para gerar as análises e previsões:

```python
jupyter notebook previsao_de_investimentos_bancarios.ipynb
```

## 🤝 Contribuição

Contribuições para melhorias do projeto são bem-vindas! Sinta-se à vontade para abrir pull requests e ajudar a melhorar este projeto.

## 📚 Referências

1. **Pandas Documentation**: [Pandas Documentation](https://pandas.pydata.org/docs/) - Guia oficial para manipulação e análise de dados em Python.
   
2. **Scikit-learn Documentation**: [Scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html) - Documentação oficial da biblioteca Scikit-learn, usada para Machine Learning em Python.
   
3. **Plotly Documentation**: [Plotly Documentation](https://plotly.com/python/) - Guia para criar gráficos interativos usando Plotly em Python.
   
4. **Machine Learning Yearning**: Andrew Ng. [Machine Learning Yearning](https://www.deeplearning.ai/machine-learning-yearning/) - Guia prático sobre como estruturar projetos de Machine Learning, escrito por um dos maiores especialistas na área.
   
5. **Introduction to Statistical Learning**: Gareth James, Daniela Witten, Trevor Hastie, Robert Tibshirani. [Introduction to Statistical Learning](https://www.statlearning.com/) - Livro que aborda conceitos básicos de estatística e Machine Learning.
   
6. **Alura Cursos**: [Alura](https://www.alura.com.br) - Plataforma de cursos online onde este projeto foi desenvolvido, com foco em Data Science e Machine Learning.

## Agradecimentos 🙏

Gostaria de expressar minha sincera gratidão às seguintes contribuições e recursos que tornaram este projeto possível

<div align="center">
  <img src="https://github.com/user-attachments/assets/54afb33c-97be-40b6-8c96-0f12852e946f" alt="thank-you" width="500">
</div>

## 📞 Contato
- **LinkedIn:** [Eduardo Coqueiro](https://www.linkedin.com/in/eduardocoqueiro/)
- **Site:** [Eduardo Coqueiro](https://dataguy.my.canva.site/eduardo-coqueiro)
- **Kaggle:** [Eduardo Coqueiro](https://www.kaggle.com/eduardocoqueiro)
