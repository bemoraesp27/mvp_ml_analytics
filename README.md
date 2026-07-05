# MVP - ML & Analytics

Este repositório contém o notebook e a base de dados utilizados no projeto de Ciência de Dados aplicada à previsão de risco de fatalidade em acidentes de trânsito.

## 📂 Estrutura
- `Base_acidentes.xlsx` → dataset original
- `MVP_ML_Analytics_BernardoMoraes_4052025002069.ipynb` → notebook com todo o código e análises

## 🎯 Objetivo
Construir um modelo de classificação capaz de prever a probabilidade de um acidente resultar em fatalidade, superando o baseline ingênuo.

## 🚀 Técnica Utilizadas

Análise Exploratória de Dados (EDA): estatística descritiva, distribuição de atributos, tratamento de valores nulos.

Pré-processamento: discretização, feature engineering, padronização, codificação categórica.

Modelagem: baseline (DummyClassifier), Logistic Regression, Random Forest, Random Forest otimizado via RandomizedSearchCV.

Validação: StratifiedKFold, métricas F1-weighted e AUC para lidar com desbalanceamento.

Avaliação final: comparação com baseline, matriz de confusão, análise de erros e limitações.

Link para o notebook no Colab: https://colab.research.google.com/drive/1WElman4Dgb5CHQfi9mvlYZ0iYWsaeR9D?usp=sharing

## 📈 Resultados
Baseline: AUC = 0.50, F1 ≈ 0.78 (não aprende padrões).

Logistic Regression: AUC ≈ 0.76, F1 ≈ 0.85, rápido e interpretável.

Random Forest: AUC ≈ 0.74, F1 ≈ 0.84, mais pesado em tempo de treino.

Random Forest otimizado: AUC ≈ 0.76, F1 ≈ 0.845, recall da classe fatalidade ainda baixo (~0.24).

## ⚠️ Limitações
Baixo recall da classe fatalidade (classe minoritária).

Risco de generalização restrita a outros contextos.

Interpretabilidade limitada em modelos mais complexos.

## 🔮 Próximos Passos
Ajustar thresholds de decisão para aumentar recall da classe fatalidade.

Implementar estratificação em faixas de risco (baixo, moderado, alto).

Testar técnicas de balanceamento (SMOTE, oversampling, class_weight="balanced").

Avaliar generalização em bases de diferentes regiões e períodos.
