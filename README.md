# Mini Projeto - Análise de Dados com Python | Módulo 1
**Felipe Busarello**  
**Curso:** Análise de Dados com Python  
**Turma:** 05 - 2026  
**Professor:** Cláudio Neves


## 📌 Sobre o Projeto
Este repositório apresenta o **Mini Projeto Avaliativo do Módulo 1** do curso **Análise de Dados com Python - Turma 05**.

O projeto tem como objetivo aplicar, de forma prática, os conhecimentos adquiridos durante o módulo no processo de **Extração, Transformação e Análise de dados**, utilizando Python para preparar, explorar e analisar uma base de dados de varejo.

A atividade utiliza o arquivo `BaseVarejo.csv`, composto por informações relacionadas a compras realizadas por clientes de uma rede de supermercados.

O projeto contempla as principais etapas de uma análise exploratória de dados:  
**Carregamento → Inspeção → Tratamento → Análise → Interpretação**


## 🎯 Objetivos

O principal objetivo deste projeto é realizar uma **Análise Exploratória de Dados (AED)** utilizando Python, identificando características, padrões, possíveis inconsistências e relações existentes nos dados.

Durante o desenvolvimento serão realizadas atividades de:  
* Extração e carregamento dos dados;
* Inspeção inicial da base;
* Identificação de inconsistências;
* Verificação e tratamento de valores ausentes ou mascarados;
* Adequação dos tipos de dados;
* Remoção de colunas sem informações;
* Identificação e tratamento de registros duplicados;
* Validação da variável de data;
* Análise estatística descritiva;
* Agrupamentos e comparações entre categorias;
* Identificação de padrões nos dados;
* Elaboração de conclusões a partir dos resultados obtidos.


## 📊 Base de Dados
A base utilizada no projeto é a **Base Varejo**, disponibilizada no Kaggle.  

Fonte: Kaggle  
Dataset: [Base Varejo](https://www.kaggle.com/datasets/namespaiva/base-varejo/data)  

De acordo com a documentação fornecida para a atividade, a base representa informações de compras realizadas por clientes de uma rede de supermercados no período de 2010 a 2022.  

A base possui inicialmente **830.000 registros e 14 colunas**, sendo que quatro colunas (`Unnamed: 10` a `Unnamed: 13`) foram identificadas como completamente vazias e posteriormente removidas durante o processo de preparação dos dados.

Após essa etapa, a base passou a conter **830.000 registros e 10 colunas** com informações úteis para a análise

**🗂️ Dicionário de Dados**  
| Campo | Descrição |
|---------|----------|
| `DATA` | Data da compra | 
| `CO_ID` | Identificação da compra / número da nota fiscal | 
| `CL_ID` | Identificação do cliente | 
| `CL_GENERO` | Sexo biológico informado pelo cliente | 
| `CL_EC` | Estado civil do cliente | 
| `CL_FHL` | Número de filhos do cliente | 
| `CL_SEG` |  Segmentação econômica do cliente | 
| `PR_ID` | Código do produto (SKU) | 
| `PR_CAT` | Categoria do produto | 
| `PR_NOME` | Nome do produto | 



**Estado Civil**  
A variável `CL_EC` utiliza códigos numéricos para representar o estado civil:  

| Código | Descrição |
|---------|----------|
| 1 | Casado ou união estável |
| 2 | Divorciado |
| 3 | Separado |
| 4 | Solteiro |
| 5 | Viúvo |


## 🔎 Processo de ETL e Preparação dos Dados
Antes da realização da análise exploratória, os dados passam por uma etapa de inspeção e preparação.

### 1. Extração
O arquivo `BaseVarejo.csv` é carregado utilizando o módulo `csv` do Python, por meio do `csv.DictReader`, e também utilizando a biblioteca Panda.

Durante a importação inicial com `csv.DictReader`, foi identificado que o arquivo utilizava `;` como delimitador. O delimitador foi então configurado corretamente para realizar a leitura estruturada dos campos.

Posteriormente, a base foi carregada utilizando `pandas.read_csv()` para facilitar as etapas de tratamento e análise.

### 2. Transformação
Durante a etapa de transformação foram realizadas validações e tratamentos relacionados à qualidade dos dados.

**Colunas sem informações**
Foram identificadas quatro colunas completamente vazias:
* `Unnamed: 10`
* `Unnamed: 11`
* `Unnamed: 12`
* `Unnamed: 13`

Como essas colunas não apresentavam informações úteis, foram removidas da base utilizada para análise.

**Valores ausentes e inconsistências**
Foram realizadas verificações para identificar:
* Valores nulos;
* Valores vazios;
* Valores contendo apenas espaços;
* Valores mascarados como #N/D.

Os valores `#N/D` encontrados na coluna `PR_CAT` foram substituídos por `Sem Categoria`, enquanto os valores `#N/D` encontrados na coluna `PR_NOME` foram substituídos por `Sem Nome`.

Essa abordagem permite preservar os registros e evitar a perda de informações válidas nas demais colunas.

**Tipos de dados**
Os tipos das variáveis foram ajustados de acordo com sua finalidade.

Os identificadores `CO_ID`, `CL_ID` e `PR_ID` foram convertidos para `string`, enquanto a coluna `DATA` foi convertida para o tipo `datetime`.

A conversão da data foi realizada com validação de possíveis datas inválidas.

**Registros duplicados**
Foi realizada uma análise para identificação de registros duplicados.

Na primeira verificação foram identificados **96.553 registros duplicados**, que serão avaliados e tratados antes da geração da base final utilizada nas análises.

### 3. Carga
Após as etapas de preparação e tratamento, a base final será utilizada para a **Análise Exploratória de Dados (AED)**, geração das estatísticas, agrupamentos e identificação dos principais insights.


## 📈 Análise Exploratória de Dados
Seção a ser *complementada* após a conclusão das análises.

Serão realizadas análises relacionadas a:
* Distribuição do número de filhos dos clientes;
* Comportamento das compras por gênero;
* Distribuição das compras por categoria de produto;
* Outros agrupamentos relevantes identificados durante a exploração dos dados.


## 📊 Estatística Descritiva
*Seção a ser complementada após a conclusão das análises.*

Será realizada uma análise estatística da variável CL_FHL (número de filhos dos clientes), contemplando:
* Contagem;
* Média;
* Mediana;
* Desvio padrão;
* Moda;
* Mínimo;
* Máximo;
* Quartis.


## 📊 Agrupamentos
*Seção a ser complementada após a conclusão das análises.*

Serão realizados pelo menos dois agrupamentos para identificar padrões de comportamento e distribuição das compras.

Os agrupamentos serão definidos a partir das características disponíveis na base e dos resultados obtidos durante a análise exploratória.


## 💡 Principais Insights
*Seção a ser preenchida após a conclusão da análise.*

* Insight 1: A preencher após a análise dos dados.
* Insight 2: A preencher após a análise dos dados.
* Insight 3: A preencher após a análise dos dados.
* Insight 4: A preencher após a análise dos dados.
* Insight 5: A preencher após a análise dos dados.
* Insight 6: A preencher após a análise dos dados.


## 📋 Resultados
*Seção a ser complementada após a conclusão do projeto.*

Os resultados finais serão apresentados por meio das estatísticas descritivas, agrupamentos e conclusões obtidas durante a análise exploratória.


## 🛠️ Tecnologias e Bibliotecas
O projeto foi desenvolvido em Python (versção 3.13.14), utilizando as seguintes bibliotecas e módulos:
* **CSV** - utilizado para carregamento e leitura estruturada do arquivo `.csv` por meio do `DictReader`;
* **Pandas** - utilizado para leitura, tratamento, transformação e análise dos dados;
* **NumPy** - utilizado como suporte às operações numéricas;
* **Matplotlib** - utilizado para criação de visualizações.


## 📁 Estrutura do Projeto
```text
Mini_Projeto_Felipe_Busarello/
│ 
├── 📂 dataset/
│   └── BaseVarejo.csv
│
├── 📂 graficos/
│   └── *Complementar*
│
├── 📓 Mini_Projeto_Felipe_Busarello.ipynb
│
├── README.md
└── df.limpo.csv
```
*Complementar*


## 🚧 Desafios encontrados
Durante o desenvolvimento do projeto foram identificados alguns desafios relacionados à qualidade e estrutura da base de dados, entre eles:
* Arquivo CSV utilizando ; como delimitador;
Quatro colunas completamente vazias;
* Identificação de valores mascarados como `#N/D`;
* Necessidade de adequação dos tipos de dados;
* Identificação de registros duplicados;
* Necessidade de validação da consistência das datas e dos identificadores.


## 💡 Principais aprendizados
*Seção a ser complementada após a conclusão do projeto.*

Entre os principais aprendizados estão:
* Importação e inspeção de arquivos CSV;
* Utilização do `csv.DictReader`;
* Manipulação de dados com Pandas;
* Identificação e tratamento de problemas de qualidade dos dados;
* Conversão e validação de tipos de dados;
* Análise estatística descritiva;
* Utilização de agrupamentos para identificação de padrões;
* Aplicação prática do conceito de ETL.


## 🚀 Como Executar o Projeto Localmente
### 1. Clonar o Repositório
No terminal, execute:
```
git clone https://github.com/FelipeBusa/mini_projeto_turma05.git
```

Depois, acesse a pasta do projeto:
```
cd curso-sctec/ProjetoAvaliativoM1/Mini_Projeto_Felipe_Busarello
```

### 2. Instalar as Bibliotecas
Caso necessário, instale as bibliotecas utilizadas:
```
%pip install pandas numpy matplotlib seaborn
```

### 3. Executar o Projeto
Abra o arquivo:  
`Mini_Projeto_Felipe_Busarello.ipynb`  
O projeto deve ser executado utilizando VS Code.  
Execute as células do notebook em sequência para reproduzir as etapas de importação, tratamento e análise dos dados.


## 🎯 Próximos Passos
* Finalizar o tratamento dos registros duplicados;
* Validar a regra do identificador `CO_ID`;
* Finalizar a validação da qualidade dos dados;
* Gerar as estatísticas descritivas de `CL_FHL`;
* Realizar os dois agrupamentos obrigatórios;
* Elaborar os principais insights da análise;
* Gerar e salvar a base `df_limpo`;
* Finalizar o README;
* Organizar o histórico de commits;
* Publicar a versão final do projeto no GitHub.

## 👨‍💻 Autor
**Felipe Busarello**  
**Curso:** Análise de Dados com Python  
**Turma:** 05 - 2026  
**Professor:** Cláudio Neves  
**Projeto:** Mini Projeto — Módulo 1  
**Data:** 17/08/2026