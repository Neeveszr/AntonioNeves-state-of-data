# Análise de salários de profissionais de dados no Brasil em 2024

**Integrantes:**  
- Antonio Neves Aguiar Neto

**Dashboard interativo:**  
[Dashboard no Google Looker Studio](https://datastudio.google.com/reporting/1dd0ad0a-b6b5-4daf-8d78-fe5317022a49)

---

## Sobre o projeto

Este projeto analisa os dados da pesquisa **State of Data Brazil 2024/2025**, realizada pela comunidade Data Hackers em parceria com a Bain & Company, com o objetivo de responder à pergunta:

> **Quais fatores mais influenciam o salário de um profissional de dados no Brasil em 2024?**

A análise foi desenvolvida como trabalho final da disciplina **Análise Avançada de Dados**, utilizando Python para limpeza, tratamento e análise estatística, além de um dashboard interativo no Google Looker Studio e um relatório narrativo em PDF.

---

## Resposta à pergunta central

A análise indica que os fatores mais associados ao salário dos profissionais de dados no Brasil são **senioridade, experiência na área de dados e cargo ocupado**. Profissionais em níveis mais avançados, com mais tempo de atuação e em funções mais especializadas tendem a apresentar salários medianos superiores.

A senioridade mostrou uma progressão clara: profissionais Júnior, Pleno e Sênior aparecem em faixas salariais crescentes. A experiência reforça esse padrão, pois respondentes com mais anos de atuação na área de dados apresentam remunerações medianas maiores. O cargo ocupado também ajuda a explicar diferenças salariais, especialmente em funções ligadas à engenharia de dados, ciência de dados, machine learning, analytics engineering e liderança.

Outros fatores, como região e gênero, também foram analisados, mas exigem interpretação cuidadosa. Diferenças salariais observadas entre grupos podem refletir diferenças de composição em termos de cargo, senioridade e experiência. Por isso, os resultados devem ser lidos como **associações** e não como prova de causalidade direta.

---

## Principais resultados

- **Salário médio estimado:** aproximadamente R$ 12.028.
- **Salário mediano estimado:** aproximadamente R$ 10.000.
- **Respondentes analisados:** 4.863 profissionais com salário válido.
- **Fatores mais associados ao salário:** senioridade, experiência na área de dados e cargo ocupado.
- **Região e gênero:** analisados como variáveis de contexto, com cautela na interpretação.

---

## Decisões de limpeza e tratamento dos dados

A base original possui mais de 400 colunas, com nomes pouco intuitivos e respostas em diferentes formatos. Para tornar a análise possível, foram selecionadas e renomeadas as colunas mais relevantes para a pergunta central.

As principais decisões foram:

1. **Conversão das faixas salariais**  
   O salário estava informado em faixas de texto, como “de R$ 4.001 a R$ 6.000”. Para permitir cálculos estatísticos, cada faixa foi convertida para o **ponto médio do intervalo**. Por exemplo, a faixa de R$ 4.001 a R$ 6.000 foi representada por R$ 5.000,50.

2. **Uso da mediana como medida principal**  
   Como salários costumam ter assimetria e valores altos que puxam a média para cima, a mediana foi usada como principal medida comparativa nos gráficos e interpretações.

3. **Padronização de cargos e senioridade**  
   Cargos semelhantes foram agrupados em categorias padronizadas, como Analista de Dados, Cientista de Dados, Engenheiro de Dados, Analytics Engineer e Gestão/Liderança. A senioridade foi organizada em Júnior, Pleno e Sênior.

4. **Tratamento de valores ausentes**  
   Valores ausentes foram tratados de acordo com o tipo de variável. Em campos sensíveis, como gênero e raça/cor, os dados não foram imputados, respeitando a possibilidade de não-resposta intencional.

5. **Criação de base tratada para o dashboard**  
   Foi criada uma versão reduzida da base, contendo apenas as colunas necessárias para o dashboard no Looker Studio. O CSV original da base não é incluído no repositório.

---

## Entregáveis do projeto

- `notebook/` — Notebook Python com limpeza, análise univariada, análise bivariada e gráfico-síntese.
- `relatorio/` — Relatório narrativo em PDF com os principais achados e interpretação.
- `dados/README.md` — Instruções para baixar a base original no Kaggle.
- `README.md` — Documentação principal do projeto.
- Dashboard publicado no Google Looker Studio.

---

## Estrutura do repositório

```text
AntonioNeves-state-of-data/
├── README.md
├── notebook/
│   └── AntonioNeves-analise.ipynb
├── relatorio/
│   └── AntonioNeves-relatorio.pdf
└── dados/
    └── README.md
```

---

## Ferramentas e bibliotecas utilizadas

- Python
- pandas
- numpy
- matplotlib
- seaborn
- Google Colab
- Google Sheets
- Google Looker Studio

---

## Referências

- **State of Data Brazil 2024/2025** — Data Hackers e Bain & Company.  
  Disponível em: https://www.kaggle.com/datasets/datahackers/state-of-data-brazil-20242025

- Dicionário oficial da base, disponível na página do dataset no Kaggle.

- Documentação das bibliotecas:
  - pandas: https://pandas.pydata.org/
  - numpy: https://numpy.org/
  - matplotlib: https://matplotlib.org/
  - seaborn: https://seaborn.pydata.org/

---

## Observações éticas

Os resultados relacionados a gênero, raça/cor e região foram tratados com cautela. Essas variáveis podem refletir desigualdades importantes, mas também podem estar associadas a diferenças de composição da amostra, como cargo, senioridade, experiência, localização e tipo de empresa.

Por isso, o trabalho evita afirmar causalidade direta e comunica os achados como padrões observados na amostra analisada.
