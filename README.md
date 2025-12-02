## 📊 Padrões de Mortalidade no Brasil – Repositório do Artigo

Este repositório contém o código-fonte (Jupyter Notebook) utilizado para a análise de dados que subsidiou o artigo científico:

- **Título**: Padrões de Mortalidade no Brasil: Uma Análise Exploratória por Sexo e Faixa Etária

**DADOS GERAIS**
- **Digital Object Identifier (DOI®)**: 10.5281/zenodo.17794076
- **País de publicação**: Brasil
- **Meio de divulgação**: Meio digital
- **Home page de publicação (URL)**: https://zenodo.org/records/17794076

**DETALHAMENTO DO EVENTO**
- **Classificação do evento**: Nacional.
- **Nome do evento**: II Congresso Nacional de Saúde Coletiva (II CIECT).
- **Ano**: 2025.

**DETALHAMENTO DA PUBLICAÇÃO**
- **Título dos anais do evento**: Anais do II Congresso Nacional de Saúde Coletiva (II CONSAC).
- **Volume**: 1.
- **ISBN**: 978-65-01-65696-0.
- **Nome da responsável pelo evento**: Scienceduc Eventos.
- **Cidade da editora**: Natal.
- **Autores**: Amanda Ferreira Gomes, Carlos Eduardo de Melo Nunes Garcia.

--------------------------------------
### 📘 Sobre o Projeto
O estudo analisa padrões de mortalidade no Brasil utilizando dados oficiais do DATASUS (2022), com ênfase em sexo, faixa etária e capítulos do CID-10. <br> 
A pesquisa explora tendências epidemiológicas com suporte de estatística descritiva, correlação de Pearson e visualizações como boxplots e mapas de calor.

--------------------------------------
### 🗂️ Estrutura do Projeto
O notebook padroes_mortalidade.ipynb realiza a preparação, limpeza e integração de dois conjuntos de dados de mortalidade, gerando um DataFrame final para análises epidemiológicas.

**Etapas principais**:
- Leitura e limpeza dos dados por faixa etária (`obitos-idade.csv`)
- Leitura e limpeza dos dados por sexo (`sexo-obitos.csv`)
- Mesclagem dos conjuntos pela coluna `"Capítulo CID-10"`
--------------------------------------
### 🧠 Objetivos do Estudo
- Investigar como os óbitos se distribuem por faixa etária no Brasil.
- Identificar diferenças de mortalidade entre homens e mulheres.
- Avaliar causas de morte segundo a classificação CID-10.
- Relacionar padrões estatísticos aos fatores demográficos e epidemiológicos brasileiros.
--------------------------------------
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

**🔹 Processamento dos Dados**
- Limpeza e tratamento de dados brutos
- Conversão de colunas categóricas para formatos numéricos

- **Análises estatísticas**:
  - Médias, medianas, proporções
  - Correlação de Pearson

- **Visualizações**:
  - Boxplots para comparação entre sexos
  - Mapas de calor por faixa etária
  - Gráficos de causas de morte (CID-10)
--------------------------------------
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
--------------------------------------
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
--------------------------------------
### 🛠️ Requisitos
Para executar o notebook, é necessário ter instalado:
- Python 3.9+
- `pandas`: Essencial para a manipulação, limpeza e mesclagem dos dados.
- `matplotlib`: Utilizada para a geração de visualizações de dados (gráficos e boxplots).
- Jupyter Notebook (ou Google Colab: serviço gratuito do Google que permite escrever e executar código Python diretamente no navegador, sem necessidade de instalação).
 --------------------------------------
### 🔁 Como Reproduzir a Análise
O processo de execução do Jupyter Notebook (`padroes_mortalidade.ipynb`) deve seguir os seguintes passos para garantir a correta preparação dos dados e a reprodutibilidade da análise:

1. **Configuração do Ambiente**: Salve o Jupyter Notebook (`padroes_mortalidade.ipynb`) e os dois arquivos de dados (`obitos-idade.csv` e `sexo-obitos.csv`) em um diretório de trabalho comum.

2. **Execução do Notebook**: Abra o arquivo `padroes_mortalidade.ipynb` em um ambiente Jupyter de sua preferência (Jupyter Lab, VS Code, Google Colab).

3. **Processamento**: Execute sequencialmente todas as células do notebook para realizar o carregamento, a limpeza e a integração dos dados, gerando o DataFrame unificado para análise.
