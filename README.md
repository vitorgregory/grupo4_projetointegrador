Este projeto realiza a análise de gastos públicos com cultura e eventos musicais na cidade e no estado de São Paulo. Através de técnicas de Ciência de Dados e Machine Learning, buscamos identificar padrões de investimento, detectar anomalias em cachês e prever custos de eventos.

## 🚀 Site do Projeto
Acesse a plataforma interativa: [**Radar da Cultura**](https://radardacultura.lovable.app/)
*Mapa interativo, rankings e detecção de irregularidades em tempo real.*

---

## 📊 Estrutura do Projeto

O projeto está organizado para facilitar a reprodutibilidade das análises e modelos:

- **`Apresentação/`**: Materiais de suporte e slides do projeto.
- **`Codigo/`**: Notebooks Jupyter contendo o pipeline de análise e modelagem.
    - `pipeline_regressao_cultura.ipynb`: Pipeline completo de Regressão Linear comparando categorias de artistas.
- **`Datasets/`**: Bases de dados brutas e tratadas (CSVs e XLSX).
    - Divisão por categorias (G1: Pequenos, G2: Médios, G3: Super Artistas).
- **`Relatorios/`**: Saídas automatizadas em PDF com métricas e diagnósticos dos modelos.
- **`Escopo.md`**: Definição detalhada dos objetivos e entregas.

---

## 🧠 Metodologia de Modelagem

Para garantir previsões precisas, dividimos o dataset da Secretaria de Cultura de SP em três variantes baseadas na faixa de cachê (`Valor_dia`):

| Variante | Perfil do Artista | Faixa de Cachê |
| :--- | :--- | :--- |
| **G1** | Pequenos Artistas | R$ 0,00 a R$ 9.999,99 |
| **G2** | Artistas Médios | R$ 10.000,00 a R$ 49.999,99 |
| **G3** | Super Artistas | Acima de R$ 50.000,00 |

### Pipeline de Dados (executado no Notebook):
1.  **Exploração**: Análise estatística e distribuição de valores.
2.  **Detecção de Anomalias**: Uso de **IQR** e **K-Means** (distância ao centróide) para identificar cachês fora do padrão.
3.  **Tratamento**: Limpeza de outliers e imputação de dados ausentes.
4.  **Engenharia de Features**: *Target Encoding* para fornecedores e *One-Hot Encoding* para regiões/zonas.
5.  **Regressão Linear**: Treinamento e avaliação (R², MAE, RMSE) comparando treino e teste para mitigar overfitting.

---

## 🛠️ Tecnologias Utilizadas

- **Linguagem**: Python 3.x
- **Análise de Dados**: Pandas, Numpy
- **Machine Learning**: Scikit-learn (LinearRegression, KMeans, StandardScaler)
- **Visualização**: Matplotlib, Seaborn, Plotly
- **Relatórios**: PyPDF (Consolidação de diagnósticos)

---

## 👥 Integrantes do Grupo 4

- Douglas da Silva Esteves
- Ricardo Stevanatto Calvoso
- Thiago Americo Lima de Lima Moreton
- Vitor Gregory Bezerra Lins

---

## 📈 Resultados Esperados

- **Ranking Transparente**: Identificação dos artistas e empresas que mais recebem verba pública.
- **Mapa de Calor**: Visualização de investimentos por Região e Zona de São Paulo.
- **Modelo Preditivo**: Estimativa de custo justo para eventos com base no histórico e perfil do fornecedor.
- **Auditoria**: Identificação automatizada de casos suspeitos para análise de órgãos competentes.



