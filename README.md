# 💎 Projeto: Classificação da qualidade do corte de diamantes

# 📊 Resultados Esperados
O objetivo principal é comparar o desempenho dos diferentes algoritmos de classificação quanto à predição da qualidade do corte dos diamantes e analisar as variáveis mais importantes na decisão final dos modelos, com foco em interpretabilidade.

## 📂 Dados Utilizados

A base de dados contém **35.342 observações** e **10 variáveis**, sendo a variável alvo (`cut`) de natureza categórica. O projeto foi desenvolvido em **Python** no ambiente **Google Colab**, com integração ao **GitHub**.

📁 [Diamonds.csv](https://raw.githubusercontent.com/path/to/Diamonds.csv)

**Descrição das variáveis:**

| Variável  | Descrição |
|-----------|-----------|
| `price`   | Preço em dólares (US$326 - US$18.823) |
| `carat`   | Peso do diamante (0.2 - 5.01) |
| `color`   | Cor do diamante, de D (melhor) a J (pior) |
| `clarity` | Clareza do diamante (I1, SI2, SI1, VS2, VS1, VVS2, VVS1, IF) |
| `x`       | Comprimento (mm) |
| `y`       | Largura (mm) |
| `z`       | Profundidade (mm) |
| `depth`   | Percentual de profundidade total |
| `table`   | Largura do topo em relação ao ponto mais largo |
| `cut`     | Qualidade do corte (Ideal, Premium) - **Variável Alvo** |

---

## ✅ Etapas Realizadas no Notebook

1. **Importação da base de dados via link do GitHub** e carregamento em um DataFrame com `pandas`.
2. **Transformação das variáveis categóricas** (`clarity` e `color`) em **dummies**, com remoção das colunas originais.
3. **Visualização única** da distribuição da variável `cut`.
4. **Recodificação da variável alvo**, transformando 'Ideal' em 0 e 'Premium' em 1.
5. **Separação entre variáveis independentes e dependente**.
6. **Normalização das variáveis independentes** com `StandardScaler`.
7. **Divisão do dataset em treino e teste** na proporção 70-30%.
8. **Aplicação de modelo de Árvore de Decisão** com parâmetros padrão.
9. **Geração da matriz de confusão e relatório de classificação** para Árvore de Decisão.
10. **Aplicação de modelo Random Forest** com parâmetros padrão e geração do relatório.
11. **Execução de GridSearchCV** para otimizar os parâmetros `criterion`, `max_depth` e `max_features` do Random Forest.
12. **Relatório de classificação com os melhores parâmetros** encontrados para Random Forest.
13. **Aplicação de modelo XGBoost** com parâmetros padrão e relatório de classificação.
14. **Aplicação de modelo SVM** com parâmetros padrão e relatório de classificação.
15. **Execução de GridSearchCV no SVM** para encontrar melhores valores de `C` e `kernel`.
16. **Relatório de classificação com os melhores parâmetros** encontrados para o SVM.
17. **Visualização da importância das variáveis** no melhor modelo Random Forest.
18. **Identificação das 3 variáveis mais relevantes**, com justificativa baseada na análise de importância.
19. **Explicabilidade com LIME**: aplicação da técnica em 2 observações do conjunto de teste.
20. **Interpretação dos fatores mais influentes** na classificação das observações analisadas com LIME.

---

## 🛠️ Tecnologias Utilizadas

- Python 3.10+
- Google Colab
- Pandas, NumPy
- Scikit-learn
- XGBoost
- LIME
- Matplotlib / Seaborn

---

## 📎 Instruções para Execução

1. Clone o repositório:
   ```bash
   git clone https://github.com/usuario/repositorio-diamantes.git
