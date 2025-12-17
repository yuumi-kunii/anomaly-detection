# Detecção de Anomalias em Transações de Cartão de Crédito

Este repositório reúne notebooks em Python que exploram técnicas de detecção de anomalias aplicadas ao conjunto de dados público de fraudes em cartões de crédito. O objetivo é comparar abordagens para identificar transações suspeitas de forma não supervisionada.

## Conteúdo
- `Isolation_Forest_and_LOF.ipynb`: demonstra Isolation Forest e Local Outlier Factor (LOF) para identificar pontos fora do padrão, incluindo visualização de scores e comparação direta entre os algoritmos.
- `fraud_detection_anomaly.ipynb`: versão estendida com normalização dos dados, ajustes de hiperparâmetros e um autoencoder implementado em TensorFlow/Keras para detecção de anomalias.

## Pré-requisitos
- Python 3.9–3.12 com acesso ao Jupyter (via `jupyter notebook` ou VS Code com a extensão Jupyter instalada). Essa faixa garante compatibilidade com as versões sugeridas das bibliotecas abaixo.
- Bibliotecas comuns de ciência de dados (numpy, pandas, scikit-learn, matplotlib, seaborn) e TensorFlow/Keras para o autoencoder. Caso precise instalar, use versões mínimas sugeridas:
  ```bash
  pip install -U "numpy>=1.24" "pandas>=1.5" "scikit-learn>=1.3" "matplotlib>=3.7" "seaborn>=0.12" "tensorflow>=2.11" "jupyter>=1.0"
  ```
  Recomenda-se criar e ativar um ambiente virtual (`python -m venv .venv && source .venv/bin/activate`) e, se quiser registrar as dependências, salvar essas versões em um `requirements.txt`.
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
   - Treinamento dos modelos (Isolation Forest, LOF e Autoencoder com TensorFlow/Keras).
   - Avaliação básica com métricas e gráficos de distribuição de scores/anomalias.

## Objetivo dos códigos
- Ilustrar técnicas de detecção de anomalias em um cenário de dados extremamente desbalanceados.
- Comparar como Isolation Forest e LOF se comportam na separação de transações legítimas versus fraudulentas.
- Fornecer um ponto de partida simples para quem deseja adaptar esses modelos a outros conjuntos de dados ou incorporar etapas adicionais de avaliação.
