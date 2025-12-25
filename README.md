# Análise de Estabilidade de Hardware: Datasets Backblaze 💾📊

Este projeto realiza o processamento e análise estatística de dados de monitoramento de unidades de armazenamento (HDDs e SSDs), utilizando uma base de dados real de **1.26 GB** fornecida pela Backblaze. O objetivo principal é identificar padrões de falha e classificar a estabilidade operacional de diferentes fabricantes e modelos de hardware.

## 🚀 Destaques do Projeto

* **Processamento de Big Data:** Implementação de uma pipeline de ingestão de dados via Python, utilizando a técnica de *chunking* para processar arquivos que excedem a memória RAM disponível.
* **Arquitetura SQL:** Migração de dados brutos (CSV) para um banco de dados estruturado (**SQLite**), permitindo consultas performáticas em milhões de registros.
* **Métricas de Confiabilidade:** Aplicação de conceitos estatísticos e de física de materiais para calcular a Taxa de Estabilidade, normalizando os dados para uma comparação justa entre diferentes volumes de uso.

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python
* **Bibliotecas:** Pandas (Manipulação de dados), SQLite3 (Banco de dados), Matplotlib/Seaborn (Visualização)
* **Ferramentas:** Jupyter Notebook, Git, SQL

## 📈 Metodologia e Cálculo

Para determinar quais componentes apresentam maior estabilidade, foi utilizada a seguinte fórmula matemática para normalizar as falhas em relação ao tempo de operação (registros):

$$\text{Taxa \%} = \frac{\text{Total de Falhas}}{\text{Total de Registros}} \times 100$$

Esta métrica permite identificar modelos que, embora tenham um número absoluto de falhas baixo, podem ser instáveis devido ao pouco tempo de uso registrado.

## 🔍 Resultados Obtidos

Abaixo, o resumo da estabilidade consolidado por fabricante (dados processados via SQL):

| Fabricante | Total de Falhas | Total de Amostras | Taxa de Estabilidade (%) |
| :--- | :--- | :--- | :--- |
| **Hitachi** | X | Y | 0.00XX% |
| **Seagate** | X | Y | 0.0XXX% |
| **Western Digital** | X | Y | 0.0XXX% |

> **Insight:** Modelos com taxas mais baixas são classificados como de **Alta Estabilidade Operacional**, sendo os mais indicados para ambientes críticos de servidores e storage.

## 📂 Como Executar

1. Baixe o dataset `harddriver.csv` no Kaggle.
2. Certifique-se de que o arquivo está na mesma pasta do notebook.
3. Execute o script de ingestão (o processo criará o arquivo `big_data.db`).
4. Rode as queries de análise para gerar os relatórios.

