# 📊 Análise de Clustering RFV para E-commerce

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0.2-orange)
![Pandas](https://img.shields.io/badge/Pandas-1.4.0-red)

Projeto de segmentação de clientes utilizando análise RFV (Recência, Frequência, Valor) e múltiplos algoritmos de clustering.

## 🎯 Objetivo
Identificar padrões de comportamento de compra em clientes de e-commerce através de técnicas de clusterização para:
- Personalizar campanhas de marketing
- Reduzir churn
- Aumentar valor médio do ticket

## 📂 Dataset
**Fonte**: Kaggle (Transações de e-commerce 2010-2011)  
**Variáveis-chave**:
- `Recência (R)`: Dias desde última compra
- `Frequência (F)`: Número de compras únicas
- `Valor (M)`: Ticket médio por cliente

**Pré-processamento**:
- Tratamento de outliers (5% superiores)
- Normalização dos dados
- Exclusão de valores negativos/inconsistentes

## 🔍 Análise Exploratória

### Distribuição Geográfica
![Distribuição por País](https://i.imgur.com/geo_distribution.png)
*Concentração de clientes por país*

### Correlação RFV
![Matriz de Correlação](https://i.imgur.com/rfv_correlation.png)
*Relação entre as variáveis RFV*

## 🤖 Modelagem Comparativa

### Desempenho dos Algoritmos
| Algoritmo | Silhouette | Davies-Bouldin | N° Clusters |
|-----------|------------|----------------|-------------|
| K-Means | 0.52 | 0.81 | 4 |
| Hierárquico | 0.49 | 0.85 | 4 |
| DBSCAN | 0.31 | 1.12 | 6 |
| MeanShift | 0.45 | 0.93 | 3 |

### Visualização 3D dos Clusters (K-Means)
![Clusters 3D](https://i.imgur.com/kmeans_3dview.png)
*Segmentação por R-F-V com K-Means*

## 📌 Segmentação de Clientes (K-Means)

### Perfil dos Clusters
| Cluster | Recência | Frequência | Valor | Interpretação |
|---------|----------|------------|-------|---------------|
| 0 | Alta | Baixa | Baixo | Clientes inativos |
| 1 | Média | Baixa | Alto | Compradores ocasionais |
| 2 | Baixa | Média | Médio | Clientes regulares |
| 3 | Baixa | Alta | Médio | Clientes fiéis |

## 💡 Insights Estratégicos

### Ações Recomendadas por Segmento:
1. **Cluster 0 (Inativos)**:
   - Campanhas de reativação
   - Pesquisa de satisfação
   - Ofertas especiais

2. **Cluster 1 (Ocasionais)**:
   - Produtos premium
   - Atendimento VIP
   - Comunicação sazonal

3. **Cluster 2 (Regulares)**:
   - Programas de fidelidade
   - Cross-selling
   - Descontos progressivos

4. **Cluster 3 (Fiéis)**:
   - Recompensas exclusivas
   - Acesso antecipado
   - Relacionamento personalizado

## 📈 Visualizações Complementares

### Importância das Variáveis
![Feature Importance](https://i.imgur.com/feature_importance_rfv.png)
*Contribuição de cada variável na formação dos clusters*

### Comparativo de Métricas
![Metric Comparison](https://i.imgur.com/metrics_comparison.png)
*Desempenho dos algoritmos em diferentes indicadores*
