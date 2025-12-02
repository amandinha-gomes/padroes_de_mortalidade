## 📊 Padrões de Mortalidade no Brasil – Repositório do Artigo

Este repositório contém o código-fonte (Jupyter Notebook) utilizado para a análise de dados que subsidiou o artigo científico:

- **Título**: Padrões de Mortalidade no Brasil: Uma Análise Exploratória por Sexo e Faixa Etária
- **Status**: Aceito e publicado
- **Evento**: II Congresso Nacional de Saúde Coletiva (II CONSAC)
- **Área Temática**: AT01 – Saúde Pública

### 📘 Sobre o Projeto
O estudo analisa padrões de mortalidade no Brasil utilizando dados oficiais do DATASUS (2022), com ênfase em sexo, faixa etária e capítulos do CID-10. <br> 
A pesquisa explora tendências epidemiológicas com suporte de estatística descritiva, correlação de Pearson e visualizações como boxplots e mapas de calor.

### 🗂️ Estrutura do Projeto
O notebook padroes_mortalidade.ipynb realiza a preparação, limpeza e integração de dois conjuntos de dados de mortalidade, gerando um DataFrame final para análises epidemiológicas.

**Etapas principais**:
- Leitura e limpeza dos dados por faixa etária (obitos-idade.csv)
- Leitura e limpeza dos dados por sexo (sexo-obitos.csv)
- Mesclagem dos conjuntos pela coluna "Capítulo CID-10"

### 🧠 Objetivos do Estudo
- Investigar como os óbitos se distribuem por faixa etária no Brasil.
- Identificar diferenças de mortalidade entre homens e mulheres.
- Avaliar causas de morte segundo a classificação CID-10.
- Relacionar padrões estatísticos aos fatores demográficos e epidemiológicos brasileiros.

### 📊 Metodologia

🔹 **Base de Dados**
- **Fonte**: DATASUS – Sistema de Informações sobre Mortalidade (SIM)
- **Ano**: 2022


| Arquivo            | Conteúdo                                       | Finalidade                     |
| ------------------ | ---------------------------------------------- | ------------------------------ |
| `obitos-idade.csv` | Mortalidade por faixa etária e Capítulo CID-10 | Criação do DataFrame `df`      |
| `sexo-obitos.csv`  | Mortalidade por sexo e Capítulo CID-10         | Criação do DataFrame `df_sexo` |



**Formato esperado dos arquivos**
- Separador: ;
- Ignorar as 3 primeiras linhas (skiprows=3)

- **Variáveis usadas**:
  - Sexo
  - Faixa etária
  - Capítulos do CID-10
  - Total de óbitos por categoria

🔹 **Ferramentas Utilizadas**
- Python
  - pandas
  - matplotlib

🔹 **Processamento dos Dados**
- Limpeza e tratamento de dados brutos
- Conversão de colunas categóricas para formatos numéricos

- **Análises estatísticas**:
  - Médias, medianas, proporções
  - Correlação de Pearson

- **Visualizações**:
  - Boxplots para comparação entre sexos
  - Mapas de calor por faixa etária
  - Gráficos de causas de morte (CID-10)

### 🧾 Principais Resultados

**🔸 1. Mortalidade por Idade**
- Maior volume de óbitos concentra-se em adultos e idosos (35+ anos).
- Crianças e jovens têm padrões distintos, com baixa correlação com os grupos mais velhos.
- A idade é o fator mais determinante no risco de morte.

**🔸 2. Diferenças por Sexo**
- **Homens apresentam**:
  - Maior variabilidade na distribuição de óbitos
  - Mais outliers
  - Predomínio em causas externas (73,9%)

- **Mulheres concentram mortalidade**:
  - Em doenças geniturinárias
  - Em causas relacionadas à gestação, parto e puerpério

**🔸 3. Causas de Morte (CID-10)**
- Doenças do aparelho circulatório são as principais causas de óbito no país.
- Causas externas são especialmente relevantes entre os homens.
- Neoplasias têm distribuição equilibrada entre os sexos.

### 📌 Conclusões
- A mortalidade no Brasil continua fortemente associada ao **envelhecimento populacional** e ao aumento das **doenças crônicas não transmissíveis.**
- Causas externas afetam principalmente **jovens do sexo masculino.**
- Apesar dos avanços na saúde pública, ainda existem desafios relacionados a:
  - Violência
  - Adoção de hábitos saudáveis
  - Desigualdades regionais
- Sugere-se ampliar futuras análises com:
  - Variáveis socioeconômicas
  - Séries temporais
  - Modelos estatísticos avançados e machine learning

Como Reproduzir a Análise
