# Classificação de Elementos Transponíveis  

Este repositório contém o código e os arquivos utilizados no projeto **"Identificação e Classificação de Elementos Transponíveis"**, que tem como objetivo identificar e classificar elementos transponíveis (TEs) em sequências genômicas utilizando ferramentas bioinformáticas e algoritmos de aprendizado supervisionado.

## **Descrição do Projeto**  
O projeto utiliza técnicas de aprendizado de máquina para classificar elementos transponíveis em duas categorias principais:  
- **Classe I:** Retrotransposons.  
- **Classe II:** DNA Transposons.  

A abordagem inclui coleta de dados genômicos, predição de elementos transponíveis, redução de redundância e classificação automatizada. Os resultados incluem uma análise comparativa de diferentes algoritmos, como Naive Bayes, SVM e Random Forest.  

## **Metodologia**  
1. **Coleta de Dados:**  
   - Sequências genômicas bacterianas foram coletadas do banco de dados público **NCBI**.  
   - Bibliotecas curadas, como **TREP** e **Dfam**, foram utilizadas para treinar o modelo de classificação.  

2. **Pré-processamento:**  
   - Sequências genômicas consolidadas em um único arquivo **multifasta**.  
   - Predição inicial de TEs com **RepeatModeler2 (RM2)**.  
   - Redução de redundância com o software **cd-hit-est**.  

3. **Classificação:**  
   - Modelos de aprendizado supervisionado, como **Naive Bayes Multinomial**, **SVM** e **Random Forest**, foram utilizados para classificar os TEs preditos.  

4. **Avaliação:**  
   - Métricas como **Precision**, **Recall**, **F1-Score** e **Matriz de Confusão** foram usadas para avaliar o desempenho.  

## **Resultados**  
Os resultados comparativos entre os algoritmos estão descritos no arquivo [resultados.md](resultados.md). Em resumo:  
- O **Random Forest** apresentou o melhor equilíbrio entre precisão e revocação.  
- O **SVM** teve melhora significativa após otimização com **grid search**.  
- O **Naive Bayes** teve desempenho limitado, especialmente em revocação para DNA-transposons.  

Para mais detalhes, consulte o arquivo de resultados ou o artigo associado ao projeto.  

## **Como Usar Este Repositório**  

### **Pré-requisitos**  
Certifique-se de ter instalado:  
- **Python 3.8+**  
- Dependências listadas no arquivo `requirements.txt`.  

### **Instalação**  
1. Clone este repositório:  
   ```bash
   git clone https://github.com/agl77/Classificacao_mineracao_bioinfo.git
   cd Classificacao_mineracao_bioinfo

