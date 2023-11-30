## Projeto de Análise de Dados - Tipos de Parto no DATASUS

* **Autores**: André Bergmann Lisboa e Lucas Cardoso Azevedo

### Descrição da Investigação

Este repositório contém o trabalho final de análise de dados realizado por André Bergmann Lisboa e Lucas Cardoso Azevedo. A análise focou nos tipos de parto (Cesáreo e Vaginal) nos estados da Região Sul do Brasil (RS, PR e SC) nos anos de 2018 a 2021. O objetivo principal foi verificar as relações com o perfil das mães e analisar o comportamento e evolução ao longo desse período. Utilizamos a base SINASC (Sistema de Informação sobre Nascidos Vivos) da biblioteca pySUS para facilitar a obtenção dos dados em Python.

### Material do Projeto

Todo o material, incluindo código-fonte, conjuntos de dados e visualizações, está disponível e aberto [aqui](https://github.com/LucasAzeved/analise_partos_datasus).

### Escolha de Colunas

As colunas foram escolhidas com base na relevância para o estudo, considerando a porcentagem de valores não nulos e as informações pertinentes à análise.

### Integração, Limpeza e Transformação dos Dados

O processo envolveu o uso de bibliotecas como Pandas, Numpy, datetime e pySUS. O tratamento dos dados ocorreu em três etapas:

1. **Transformação de Colunas Numéricas:** `IDADEMAE` e `PESO` foram convertidos para o tipo inteiro.
2. **Mapeamento de Colunas Categóricas:** Diversas colunas, como `CODMUNNASC`, `ESTCIVMAE`, `GESTACAO`, `GRAVIDEZ`, `PARTO`, `CONSULTAS`, `RACACOR`, `ESCMAE2010` e `RACACORMAE`, foram mapeadas para identificadores textuais.
3. **Tratamento de Datas e Horas Especiais:** Algumas colunas de data e hora foram ajustadas, e colunas adicionais `ANONASC` e `MESNASC` foram criadas.

### Dashboard e Resultados

Após o pré-processamento, os dados foram exportados para formato CSV e utilizados para criar visualizações no Power BI Desktop. Duas páginas foram criadas: uma para analisar os tipos de parto pelo perfil da mãe e outra para uma análise evolutiva ao longo do período.

#### Insights Principais:

- **Relação com Idade:** Cesáreas ocorrem mais frequentemente em mães mais velhas, enquanto partos vaginais são mais comuns em mães mais jovens.
- **Estado Civil e Escolaridade:** Maiores diferenças entre os tipos de parto foram observadas em mães casadas; aumento de cesáreas com maior escolaridade materna.
- **Análise Evolutiva:** Diferenças consistentes nos tipos de parto ao longo dos anos, com padrões sazonais notáveis.

### Conclusões

1. **Relação entre Parto Cesáreo e Peso do Recém-Nascido:** Contrariamente à hipótese inicial, não há correlação significativa; o peso do bebê não determina o tipo de parto.
2. **Influência da Idade da Mãe:** Cesáreas são mais comuns em mães mais velhas; partos vaginais, em mães mais jovens.
3. **Impacto do Estado Civil e Escolaridade:** Diferenças mais pronunciadas em mães casadas; aumento de cesáreas com maior escolaridade materna.
4. **Análise Evolutiva:** Diferenças consistentes ao longo dos anos, com variações notáveis; padrões sazonais nos nascimentos.

### Ferramentas Utilizadas

O estudo demonstrou a eficácia do uso de ferramentas como Python, Jupyter Notebook e Power BI para obtenção, tratamento e visualização de dados. O código-fonte está disponível para transparência e revisão no [GitHub](https://github.com/LucasAzeved/analise_partos_datasus).

### Referências

1. [Documentação PySUS](https://pysus.readthedocs.io/en/latest/)
2. [Dicionário de dados SINASC](https://svs.aids.gov.br/daent/cgiae/sinasc/documentacao/dicionario_de_dados_SINASC_tabela_DN.pdf)
3. [DTB - Divisão Territorial Brasileira (IBGE)](https://www.ibge.gov.br/geociencias/organizacao-do-territorio/estrutura-territorial/23701-divisao-territorial-brasileira.html?=&t=downloads)

### Agradecimentos

Agradecemos a todos que contribuíram e compartilharam insights ao longo deste projeto. Se tiver alguma pergunta ou sugestão, sinta-se à vontade para abrir uma *issue* neste repositório.

--- 

## Dashboard

![dash1](./img/Dashboard_1.png)

![dash2](./img/Dashboard_2.png)
