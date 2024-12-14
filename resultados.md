# Resultados do Projeto de Classificação de Elementos Transponíveis (TEs)

Este documento apresenta os resultados do projeto de classificação de elementos transponíveis (TEs) utilizando diferentes algoritmos de aprendizado supervisionado. Os modelos foram avaliados com base em métricas como **Precision**, **Recall**, **F1-Score** e **Accuracy**. A tabela abaixo resume os resultados comparativos.

## Tabela 1: Comparativo entre Algoritmos de Classificação de TEs

| Modelo               | Categoria         | Precision | Recall | F1-Score | Support |
|----------------------|-------------------|-----------|--------|----------|---------|
| **Naive Bayes**      | DNA-transposon   | 0.92      | 0.26   | 0.40     | 172     |
|                      | Retrotransposon  | 0.58      | 0.98   | 0.73     | 182     |
|                      | **Accuracy**     |           |        |          | **0.63**|
| **SVM**              | DNA-transposon   | 0.85      | 0.62   | 0.72     | 172     |
|                      | Retrotransposon  | 0.71      | 0.90   | 0.80     | 182     |
|                      | **Accuracy**     |           |        |          | **0.76**|
| **Random Forest**    | DNA-transposon   | 0.88      | 0.89   | 0.88     | 172     |
|                      | Retrotransposon  | 0.89      | 0.88   | 0.89     | 182     |
|                      | **Accuracy**     |           |        |          | **0.89**|
| **SVM (após tuning)** | DNA-transposon   | 0.87      | 0.84   | 0.85     | 172     |
|                      | Retrotransposon  | 0.85      | 0.88   | 0.86     | 182     |
|                      | **Accuracy**     |           |        |          | **0.86**|

## Discussão dos Resultados

1. **Naive Bayes:**
   - O modelo apresentou alta **Precision** para DNA-transposons (0.92), mas desempenho limitado em **Recall** (0.26), resultando em um **F1-Score** baixo (0.40). Isso sugere dificuldades do modelo em capturar corretamente todas as instâncias dessa classe.
   - Para retrotransposons, a **Precision** foi menor (0.58), mas o **Recall** alto (0.98) indica que o modelo conseguiu identificar a maioria dos exemplos desta classe, ainda que com menor precisão.

2. **SVM:**
   - Apresentou melhoria significativa em relação ao Naive Bayes, com um **F1-Score** de 0.72 para DNA-transposons e 0.80 para retrotransposons. O **Accuracy** também foi maior (0.76), indicando um desempenho mais equilibrado entre as classes.

3. **Random Forest:**
   - Obteve os melhores resultados gerais, com **Precision**, **Recall** e **F1-Score** superiores a 0.88 para ambas as classes, e um **Accuracy** global de 0.89. Este modelo demonstrou ser o mais confiável para classificação equilibrada entre as categorias.

4. **SVM (após tuning):**
   - A aplicação de **grid search** para otimização de parâmetros no SVM resultou em melhorias significativas. O **F1-Score** foi elevado para 0.85 e 0.86 para DNA-transposons e retrotransposons, respectivamente. O **Accuracy** final de 0.86 evidencia o impacto positivo do ajuste fino no desempenho do modelo.

## Conclusão
Os resultados demonstram que algoritmos como **Random Forest** e **SVM** são altamente eficazes na classificação de elementos transponíveis, com destaque para o Random Forest, que apresentou os melhores resultados em termos de consistência e desempenho geral. No entanto, a aplicação de tuning no SVM também revelou-se uma estratégia promissora para melhorar a classificação.

Os próximos passos incluem:
- Investigar as causas do desequilíbrio de classes no Naive Bayes.
- Explorar outras técnicas de aprendizado de máquina, como redes neurais e ensembles.
- Refinar os conjuntos de dados de treinamento para minimizar vieses e redundâncias.


