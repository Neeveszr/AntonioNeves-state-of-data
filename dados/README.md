# Base de Dados

A base utilizada neste projeto é a pesquisa **State of Data Brazil 2024/2025**, realizada pela comunidade Data Hackers em parceria com a Bain & Company.
Para reproduzir a análise, faça o download diretamente pelo Kaggle.

## Download da base

Acesse a base pelo link abaixo:
https://www.kaggle.com/datasets/datahackers/state-of-data-brazil-20242025

---

## Como reproduzir a análise

1. Faça o download da base no Kaggle.

2. Salve o arquivo CSV localmente ou no Google Drive.

3. Abra o notebook localizado na pasta:

```text
notebook/
```

4. Atualize o caminho do arquivo CSV nas células de carregamento dos dados.

Exemplo:

```python
CAMINHO_CSV = "caminho/para/o/arquivo.csv"
```

5. Execute o notebook do início ao fim.

---

## O que o notebook realiza

Ao executar o notebook, serão feitas as seguintes etapas:

- Carregamento e reconhecimento da base;
- Seleção e renomeação das colunas relevantes;
- Tratamento de valores ausentes;
- Conversão das faixas salariais para valores numéricos estimados;
- Padronização de cargos;
- Padronização de senioridade;
- Organização da experiência na área de dados;
- Geração das estatísticas descritivas;
- Análises univariadas e bivariadas;
- Criação do gráfico-síntese;
- Exportação do CSV tratado usado no dashboard.

---

## Arquivo usado no dashboard

O notebook gera uma base tratada e reduzida para uso no Google Sheets e no Google Looker Studio.
