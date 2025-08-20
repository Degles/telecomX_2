# 🤖 Análise Preditiva de Churn em Telecomunicações 📡

**Autor:** Degles Siqueira

> Um projeto completo de Data Science para prever a evasão de clientes (churn), identificar seus principais fatores e gerar insights acionáveis para estratégias de retenção.

-----

## 🎯 Problema de Negócio

A evasão de clientes, ou churn, é um dos desafios mais críticos para empresas de serviços recorrentes, como as de telecomunicações. Adquirir um novo cliente custa significativamente mais do que reter um existente.

Este projeto ataca diretamente esse problema, respondendo a três perguntas-chave:

1.  **Por quê?** Quais são os principais motivos que levam um cliente a cancelar o serviço?
2.  **Quem?** Qual é o perfil do cliente com maior probabilidade de evasão?
3.  **Como?** Que ações estratégicas podemos tomar para retê-los?

## 📚 Índice

  * [Visão Geral](https://www.google.com/search?q=%23-vis%C3%A3o-geral)
  * [Tecnologias Utilizadas](https://www.google.com/search?q=%23-tecnologias-utilizadas)
  * [Como Executar o Projeto](https://www.google.com/search?q=%23-como-executar-o-projeto)
  * [Metodologia Aplicada](https://www.google.com/search?q=%23-metodologia-aplicada)
  * [Resultados em Destaque](https://www.google.com/search?q=%23-resultados-em-destaque)
  * [Recomendações Estratégicas](https://www.google.com/search?q=%23-recomenda%C3%A7%C3%B5es-estrat%C3%A9gicas)
  * [Autor](https://www.google.com/search?q=%23-autor)
  * [Licença](https://www.google.com/search?q=%23-licen%C3%A7a)

-----

## 💡 Visão Geral

Este repositório contém o notebook e os dados necessários para replicar uma análise de churn de ponta a ponta. A análise se aprofunda nos dados demográficos, de contrato e de uso de serviços dos clientes para construir um modelo de classificação de alta performance com o algoritmo **Random Forest**. O resultado final não é apenas um modelo, mas um conjunto de insights claros e estratégias criativas para o negócio.

## 🛠️ Tecnologias Utilizadas

O projeto foi desenvolvido utilizando as seguintes tecnologias e bibliotecas:

  * **Python 3.9+**
  * **Pandas:** Para manipulação e análise de dados.
  * **NumPy:** Para operações numéricas eficientes.
  * **Matplotlib & Seaborn:** Para visualização de dados e insights gráficos.
  * **Scikit-learn:** Para pré-processamento, modelagem preditiva e otimização.
  * **Imbalanced-learn:** Para balanceamento de classes com a técnica SMOTE.
  * **Jupyter Notebook / Google Colab:** Como ambiente de desenvolvimento interativo.

## 🚀 Como Executar o Projeto

Para replicar este projeto em seu ambiente local ou no Google Colab, siga os passos abaixo:

1.  **Clone o repositório:**

    ```bash
    git clone [https://github.com/Degles/telecomX_2]
    cd [telecomX_2]
    ```

2.  **Instale as dependências:**

    ```bash
    pip install -r requirements.txt
    ```

    *(**Nota:** Um arquivo `requirements.txt` é a melhor prática. Se estiver no Colab, a célula de instalação no notebook (`!pip install ...`) é suficiente).*

3.  **Prepare o ambiente:**

      * Abra o notebook `TelecomX_2_BR_Novo.ipynb`.
      * Certifique-se de que o arquivo `dados_telecom_tratados_2025.csv` está no mesmo diretório ou faça o upload para o ambiente.

4.  **Execute o notebook:**

      * Rode as células em sequência para executar todo o fluxo de trabalho, desde a análise até a modelagem.

## 🔬 Metodologia Aplicada

O projeto seguiu um fluxo de trabalho estruturado, cobrindo todas as etapas de um ciclo de vida de Data Science:

1.  **Definição do Problema e Exploração:** Carregamento dos dados e análise inicial para entender as variáveis e a distribuição do churn.
2.  **Pré-processamento e Limpeza:** Tratamento de valores ausentes, renomeação de colunas e transformação de variáveis categóricas em numéricas (One-Hot Encoding).
3.  **Análise Exploratória (EDA):** Investigação aprofundada com visualizações gráficas (correlação, boxplots) para extrair os primeiros insights sobre os fatores de churn.
4.  **Engenharia de Features:** Divisão dos dados em treino/teste e aplicação de **SMOTE** no conjunto de treino para corrigir o desbalanceamento de classes, garantindo que o modelo aprenda com os casos de churn de forma eficaz.
5.  **Modelagem e Otimização:** Treinamento dos modelos `Random Forest` e `KNN`. Otimização do Random Forest com `GridSearchCV` para encontrar a melhor combinação de hiperparâmetros, maximizando a métrica `f1-score`.
6.  **Interpretação e Conclusão:** Análise da importância das variáveis e consolidação dos resultados em um relatório com recomendações acionáveis.

## 📈 Resultados em Destaque

O modelo **Random Forest Otimizado** foi o campeão, demonstrando uma excelente capacidade de identificar clientes em risco.

| Métrica                 | Permaneceu (0) | **Cancelou (1)** | Geral (Acurácia) |
| ----------------------- | -------------- | ---------------- | ---------------- |
| **Precisão (Precision)** | 0.90           | **0.57** | \\multirow{3}{\*}{81%} |
| **Recall (Sensibilidade)** | 0.82           | **0.73** |                  |
| **F1-Score** | 0.86           | **0.64** |                  |

> **Insight-chave:** O modelo consegue identificar corretamente **73%** de todos os clientes que realmente iriam cancelar, dando à empresa uma chance real de agir.

#### Fatores Mais Importantes para Prever o Churn:

![Gráfico de Importância das Variáveis](imagens/importancia_variaveis.png)

#### Matriz de Confusão do Modelo Final:

![Matriz de Confusão do Modelo Otimizado](imagens/matriz_confusao.png)

## 💡 Recomendações Estratégicas

Com base nos dados, foram propostas 5 estratégias criativas de retenção:

1.  **Gamificação da Lealdade:** Lançar o programa **"Maratona de Permanência"** para recompensar clientes por marcos de tempo.
2.  **Oferta Contextual:** Criar o **"Combo Upgrade Protetor"** (Suporte + Segurança) para clientes de alto risco que migrarem para contratos anuais.
3.  **Suporte Proativo:** Implementar o **"Esquadrão Check-up Fibra"** para contatar clientes do serviço premium antes que eles reclamem.
4.  **Redução de Atrito:** Criar a **"Intervenção Pagamento Inteligente"** para incentivar a troca do Cheque Eletrônico por métodos mais estáveis.
5.  **Inovação de Produto:** Lançar o **"Contrato Flex Anual"**, que une a segurança do plano anual com a flexibilidade de poder "congelar" a assinatura por um mês.

## ✒️ Autor

  * **Degles Siqueira**
      * [](https://www.linkedin.com/in/degles-siqueira/)
      * [](https://github.com/Degles)
      * [](mailto:degles@gmail.com)

## 📜 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](https://www.google.com/search?q=LICENSE) para mais detalhes.
