# Detecção de Anomalias em Transações de Cartão de Crédito

Este repositório reúne notebooks em Python que exploram técnicas de detecção de anomalias aplicadas ao conjunto de dados público de fraudes em cartões de crédito. O objetivo é comparar abordagens para identificar transações suspeitas de forma não supervisionada.

## Conteúdo
- `Isolation_Forest_and_LOF.ipynb`: demonstra Isolation Forest e Local Outlier Factor (LOF) para identificar pontos fora do padrão.
- `fraud_detection_anomaly.ipynb`: variação do experimento com ajustes de pré-processamento e avaliação.

## Pré-requisitos
- Python 3.9+ com acesso ao Jupyter (via `jupyter notebook` ou VS Code).
- Bibliotecas comuns de ciência de dados (numpy, pandas, scikit-learn, matplotlib, seaborn). Caso alguma falte, instale dentro do próprio notebook com `pip install <pacote>`.
- Conjunto de dados: [Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) em formato CSV.

## Como executar os notebooks
1. Baixe o arquivo `creditcard.csv` no link do Kaggle acima.
2. Abra o notebook desejado (`Isolation_Forest_and_LOF.ipynb` ou `fraud_detection_anomaly.ipynb`) em um ambiente Jupyter.
3. Faça o upload do CSV para o ambiente ou garanta que o caminho local esteja acessível.
4. Atualize o caminho do arquivo na célula de leitura de dados, por exemplo:
   ```python
   df = pd.read_csv("/caminho/para/creditcard.csv")
   ```
5. Execute as células em ordem. As etapas incluem:
   - Carregamento e inspeção dos dados.
   - Padronização/normalização das variáveis.
   - Treinamento dos modelos (Isolation Forest e LOF).
   - Avaliação básica com métricas e gráficos de distribuição de scores/anomalias.

## Objetivo dos códigos
- Ilustrar técnicas de detecção de anomalias em um cenário de dados extremamente desbalanceados.
- Comparar como Isolation Forest e LOF se comportam na separação de transações legítimas versus fraudulentas.
- Fornecer um ponto de partida simples para quem deseja adaptar esses modelos a outros conjuntos de dados ou incorporar etapas adicionais de avaliação.
