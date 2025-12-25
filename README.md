# Análise de Estabilidade de Hardware: Datasets Backblaze 💾📊

Este projeto realiza o processamento e análise estatística de dados de monitoramento de unidades de armazenamento (HDDs e SSDs), utilizando uma base de dados real de **1.26 GB** fornecida pela Backblaze. O objetivo principal é identificar padrões de falha e classificar a estabilidade operacional de diferentes fabricantes e modelos de hardware.

## 🚀 Destaques do Projeto

* **Processamento de Big Data:** Implementação de uma pipeline de ingestão de dados via Python, utilizando a técnica de *chunking* para processar arquivos que excedem a memória RAM disponível.
* **Arquitetura SQL:** Migração de dados brutos (CSV) para um banco de dados estruturado (**SQLite**), permitindo consultas performáticas em milhões de registros.
* **Métricas de Estabilidade:** Aplicação de conceitos estatísticos para calcular a Taxa de Estabilidade, normalizando os dados para uma comparação justa entre diferentes volumes de uso.

## 📁 Gestão de Dados (Big Data vs. GitHub)

O dataset completo utilizado para a análise possui **1.26 GB**, o que excede o limite de upload do GitHub. Para viabilizar a demonstração do projeto neste repositório:
* **Arquivo de Amostra:** Disponibilizei o arquivo `harddrive.csv`, que contém uma amostra reduzida para testes rápidos de código.
* **Análise Real:** Os resultados e gráficos apresentados foram gerados localmente processando a base completa de 1.26 GB dentro do banco de dados `big_data.db`.

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python
* **Bibliotecas:** Pandas (Manipulação de dados), SQLite3 (Banco de dados), Matplotlib/Seaborn (Visualização)
* **Ferramentas:** Jupyter Notebook, Git, SQL

## 📈 Metodologia e Cálculo

Para determinar quais componentes apresentam maior estabilidade, foi utilizada a seguinte fórmula matemática:

$$\text{Taxa \%} = \frac{\text{Total de Falhas}}{\text{Total de Registros}} \times 100$$

Esta métrica permite identificar modelos que, embora tenham um número absoluto de falhas baixo, podem ser instáveis devido ao pouco tempo de uso registrado.

## 🔍 Resultados Obtidos

Abaixo, o resumo da estabilidade consolidado por fabricante (dados processados via SQL na base completa):

| Fabricante | Total de Falhas | Total de Amostras | Taxa de Estabilidade (%) |
| :--- | :--- | :--- | :--- |
| **Hitachi** | X | Y | 0.00XX% |
| **Seagate** | X | Y | 0.0XXX% |
| **Western Digital** | X | Y | 0.0XXX% |

> **Insight:** Modelos com taxas mais baixas são classificados como de **Alta Estabilidade Operacional**, sendo os mais indicados para ambientes críticos de servidores e storage.

## 📂 Como Executar

1. Para a análise completa, baixe o dataset `harddriver.csv` original no Kaggle.
2. Para testes rápidos, utilize o `harddriver_sample.csv` incluso neste repositório.
3. Execute o script de ingestão (o processo criará o arquivo `big_data.db`).
4. Rode as queries de análise para gerar os relatórios.

