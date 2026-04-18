# analise-ideb-2023-fortaleza
Análise dos determinantes do IDEB 2023 nas escolas municipais de Fortaleza utilizando regressão linear múltipla.


Análise do IDEB 2023 - Escolas Municipais de Fortaleza

Este repositório apresenta uma análise quantitativa dos fatores associados ao desempenho educacional das escolas municipais de Ensino Fundamental II de Fortaleza, utilizando como variável principal o Índice de Desenvolvimento da Educação Básica (IDEB) referente ao ano de 2023.

Objetivo

O objetivo do estudo é identificar os principais determinantes do IDEB, considerando variáveis socioeconômicas, pedagógicas, docentes e organizacionais, por meio de um modelo de regressão linear múltipla.

Base de Dados

Os dados utilizados são provenientes de fontes oficiais:

- Instituto Nacional de Estudos e Pesquisas Educacionais Anísio Teixeira (INEP)
  - Censo Escolar 2023
  - Indicadores Educacionais (INSE, TDI, IED, IRD, ICG, entre outros)
- Sistema Permanente de Avaliação da Educação Básica do Ceará (SPAECE)
  - Dados de proficiência em Língua Portuguesa e Matemática

Todos os dados são públicos e foram tratados para construção de uma base integrada.

Metodologia

A análise foi realizada em etapas:

1. **Tratamento e integração dos dados**
   - Limpeza das bases
   - Padronização de variáveis
   - Integração via ID da escola

2. **Estatística descritiva**
   - Médias, desvios-padrão e distribuição das variáveis

3. **Análise de correlação**
   - Coeficiente de Pearson

4. **Modelagem estatística**
   - Regressão linear múltipla
   - Método de seleção de variáveis: *stepwise*
   - Nível de significância: 5%

5. **Validação do modelo**
   - Teste de multicolinearidade (VIF)
   - Análise dos resíduos
   - Testes de normalidade e independência

---

Variáveis do Modelo Final

O modelo final foi composto pelas seguintes variáveis explicativas:

- Nível Socioeconômico (INSE)
- Distorção Idade-Série (TDI)
- Esforço Docente (IED)
- Complexidade da Gestão Escolar (ICG)
- Rendimento Escolar (REN)
- Regularidade Docente (IRD)

---

Observações Metodológicas

- O indicador SPAECE não foi incluído no modelo devido à sua alta correlação com o IDEB, sendo utilizado apenas para comparação externa.
- A amostra final foi composta por 126 escolas, atendendo aos critérios de robustez de Tabachnick e Fidell (2019).

---

Estrutura do Projeto

nalise-ideb-2023-fortaleza/
│
├── data/
│ ├── raw/ # dados originais
│ ├── processed/ # base final tratada
│
├── notebooks/
│ ├── 01_limpeza.ipynb
│ ├── 02_analise.ipynb
│ ├── 03_modelo.ipynb
│
├── outputs/
│ ├── graficos/
│ ├── tabelas/
│
├── artigo/
│ ├── artigo.docx
│
├── requirements.txt
└── README.md

Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib / Seaborn
- Statsmodels
- Scikit-learn

Reprodutibilidade

Todos os códigos utilizados estão disponíveis neste repositório, permitindo a replicação completa dos resultados apresentados no estudo.

Resultados

Os resultados indicam que fatores relacionados às condições docentes e ao fluxo escolar possuem forte influência sobre o desempenho educacional, destacando-se:

- Impacto negativo do esforço docente (IED)
- Impacto positivo da regularidade docente (IRD)
- Influência significativa da distorção idade-série (TDI)

Próximos Passos

- Atualização da análise com dados do IDEB 2025
- Comparação temporal entre 2023 e 2025
- Expansão do modelo para novas variáveis

## 👨‍💻 Autor

Projeto desenvolvido por Landson Victor Gomes de Almeida


Licença

Este projeto utiliza dados públicos e tem fins acadêmicos.
