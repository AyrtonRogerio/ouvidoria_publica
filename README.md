# Implementação do Estudo: "Intelligent Ombudsman: An AI-Based Approach to Demand Classification"

Este repositório contém o **dataset sintético** e o **código-fonte** utilizados no estudo *"Intelligent Ombudsman: An AI-Based Approach to Demand Classification"*. O projeto implementa uma abordagem de aprendizado de máquina aplicada ao **Processamento de Linguagem Natural (PLN)** para classificar automaticamente manifestações enviadas a ouvidorias públicas.

## Citação/Citation

Se utilizar este dataset ou código em sua pesquisa, por favor, cite o artigo correspondente assim que for publicado.
Por enquanto, recomendamos referenciar este repositório da seguinte forma:

```bibtex
@misc{ouvidoria_inteligente,
  title        = {Intelligent Ombudsman: An AI-Based Approach to Demand Classification},
  year         = {2025},
  note         = {Dataset e código disponíveis para fins de pesquisa.}
}
```

## Metodologia

O processo foi dividido em quatro etapas principais:

1. **Aquisição e Aumento de Dados**: A partir de um pequeno conjunto de manifestações reais anonimizadas, foi realizado um processo de *Data Augmentation* com Modelos de Linguagem (LLMs), gerando um conjunto sintético balanceado em seis categorias oficiais:

   * Elogio
   * Sugestão
   * Reclamação/Crítica
   * Solicitação
   * Denúncia
   * Pedido de Acesso à Informação (LAI)

2. **Pré-processamento**: Normalização textual, lematização (spaCy), remoção de *stopwords* e *label encoding* das categorias.

3. **Treinamento e Avaliação**: Foram testados diferentes algoritmos de aprendizado de máquina, incluindo Logistic Regression, Naive Bayes, Linear SVM, FastText e BERTimbau.

4. **Validação**: A avaliação foi conduzida com *cross-validation*, utilizando como métricas principais: acurácia, precisão, recall e F1-score.

## Dataset

* Tamanho total: **720 registros (120 por categoria)**
* Formato: CSV
* Campos disponíveis:

  * `ID`
  * `Categoria`
  * `Texto da Demanda`
  * `Canal de Entrada`
  * `Data`
  * `Status da Resposta`
  * `Nível de Instrução`
  * `Localização`

⚠️ **Observação importante**:
O conjunto de dados é **inteiramente sintético** e **não representa manifestações reais de ouvidorias**. Ele foi desenvolvido **exclusivamente para fins de pesquisa e experimentação científica**. Não deve, em hipótese alguma, ser utilizado em sistemas de produção, análises institucionais ou para fundamentar políticas públicas.

## Ferramentas e Bibliotecas

* Python 3.10
* Pandas, NumPy
* NLTK, spaCy
* Scikit-learn
* Optuna
* FastText
* Hugging Face Transformers

## Licença

Este projeto está licenciado sob a Creative Commons Attribution 4.0 International (CC BY 4.0).
O uso do dataset ou do código exige a citação obrigatória dos autores.
