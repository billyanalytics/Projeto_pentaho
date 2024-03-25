[![Autor](https://img.shields.io/badge/Autor-AlanBilly-blue.svg)](https://www.linkedin.com/in/alanbillyteixeirareis)
![Assunto](https://img.shields.io/badge/Assunto-Data_warehouse-yellow.svg)
![Assunto](https://img.shields.io/badge/Assunto-SQL-green.svg)
![Assunto](https://img.shields.io/badge/Assunto-ETL-red.svg)
![Assunto](https://img.shields.io/badge/Assunto-Pentaho-brown.svg)
<!-- Imagem redimensionada -->
<img src="https://digitalcollege.com.br/wp-content/uploads/2022/05/logo-digital-1536x578.png" alt="texto alt" width="100">
<!-- Imagem redimensionada -->
<img src="https://dadosaocubo.com/wp-content/uploads/2021/02/ETLcomPentahoV3-1280x720.png" alt="texto alt" width="600">

## Status
![Badge em Desenvolvimento](https://img.shields.io/static/v1?label=STATUS&message=EM_DESENVOLVIMENTO&color=GREEN&style=for-the-badge)

# Projeto - Unid 2 - PENTAHO - SQL - ETL -  Data Warehouse ⚙️🗜️

## Breve introdução 📖

Nesta era digital, a capacidade de extrair, transformar e carregar (ETL) dados de forma eficiente tornou-se crucial para organizações de todos os setores. A demanda por insights acionáveis e tomadas de decisão baseadas em dados impulsionou a necessidade de estruturas de armazenamento de dados robustas e escaláveis, como os data warehouses.

Este projeto tem como objetivo desenvolver um data warehouse utilizando a plataforma Pentaho para ETL. O Pentaho oferece uma ampla gama de ferramentas e recursos que facilitam o processo de extração, transformação e carregamento de dados de diversas fontes para um ambiente centralizado de armazenamento de dados. Ao criar este data warehouse, pretendemos oferecer uma solução que não apenas integra dados de várias fontes, mas também os transforma em informações significativas e prontas para análise.

## 1. Introdução 🚀

O objetivo deste projeto é demonstrar como o Pentaho pode ser utilizado para facilitar e automatizar o processo de ETL. Pentaho é uma suíte de ferramentas de código aberto que oferece soluções para várias necessidades de business intelligence, incluindo ETL, geração de relatórios, análise de dados e muito mais.

O próximo passo será detalhar cada etapa do projeto, desde a extração e transformação dos dados até a apresentação visual dos resultados, promovendo uma compreensão abrangente do trabalho a ser desenvolvido.

### 1.1 Fontes de Dados 📊

- **Base:** Dados são extraídos do Banco de Dados `corporativo_final`
> [Download](Download)

### 1.2 Tecnologias Utilizadas 🛠️
- Pentaho Data Integration (PDI)
- PostgreSQL
- SQL
  
## 2. **Banco de dados** 📥

Para realizar a importação do dump/backup para um banco de dados relacional (SQL), siga os passos abaixo:

1. **Preparação do Ambiente:**
   - Garanta que o sistema de gerenciamento banco  de dados (SGBD) SQL esteja devidamente instalado e configurado.
   - Tenha o dump/backup disponível no sistema (downlaod disponível acima item 1.1).
2. **Acesso e criação do Banco de Dados:**
   - Abra a interface do SGBD
   - Como o banco de dados ainda não existe, crie um novo banco de dados.
3. **Importação do dump/backup :**
   - Clica no banco criado com o botão direito do mouse, na aba que aparece clica em restore
   - Na opção `filename` especifica o caminho onde colocou o arquivo dump/backup aperta em `restore` e espera acabar a execução do processo.  
4. **Verificação :**
   - Verificando se os dados foram importados corretamente, executando consultas no banco de dados.

### 2.1 **Processo de ETL**

#### 2.1.1 **Extração**
Depois de criado o banco e realizado a restauração, foi criado uma nova `Schemas` chamada `ODS` e feito uma cópia do `corporativo_final` para manter o banco original intacto e não trabalharmos no ambiente de produção tornando tanto o processo de ETL lento como o sistema da empresa.
     
> [Extração]()

### 2.1.2 **Tratamento e Carga**
Nesse passo começamos a montar as Dimensões e a tabela Fato já carregando o resultado para o DW. O DW foi modelado usando um esquema Snowflake, com tabelas de fato e dimensão projetadas para otimizar consultas analíticas. Para tornar o tratamento mais organizado e limpo montamos um JOB que também será usado para automatizar a atualização do Data Warehouse integrado com envio de um e-mail para informar que o DW foi atualizado

> [Modelagem Lógica](https://github.com/billyanalytics/Projeto_SQL/blob/main/Extra%C3%A7%C3%A3o/Modelagem%20L%C3%B3gica/Diagrama%20_tabela_financeiro.pdf)
> [Modelagem Lógica](https://github.com/billyanalytics/Projeto_SQL/blob/main/Extra%C3%A7%C3%A3o/Modelagem%20L%C3%B3gica/Diagrama%20_tabela_financeiro.pdf)
> [Modelagem Lógica](https://github.com/billyanalytics/Projeto_SQL/blob/main/Extra%C3%A7%C3%A3o/Modelagem%20L%C3%B3gica/Diagrama%20_tabela_financeiro.pdf)
> [Modelagem Lógica](https://github.com/billyanalytics/Projeto_SQL/blob/main/Extra%C3%A7%C3%A3o/Modelagem%20L%C3%B3gica/Diagrama%20_tabela_financeiro.pdf)
> [Modelagem Lógica](https://github.com/billyanalytics/Projeto_SQL/blob/main/Extra%C3%A7%C3%A3o/Modelagem%20L%C3%B3gica/Diagrama%20_tabela_financeiro.pdf)








### 2.3 Análise Exploratória dos Dados 🔍
Detalhes sobre a análise exploratória, padrões identificados, tratamento de nulos, descobertas e demais observações.

> [Análise Exploratoria](https://github.com/billyanalytics/Projeto_SQL/blob/main/Extra%C3%A7%C3%A3o/Analise%20Explorat%C3%B3ria/README.md)

### 2.4 Limpeza Inicial 🧹
Explicação de cada etapa da limpeza realizada, com justificativas baseadas na fase anterior de exploração.

> [limpeza](https://github.com/billyanalytics/Projeto1/tree/main/2.Extra%C3%A7%C3%A3o/2.4.Limpeza)

## 3. Transformação 🔄
### 3.1 Modelagem Dimensional
Uso do BrModelo para criar a modelagem dimensional dos dados.

> [Modelagem Dimensional](https://github.com/billyanalytics/Projeto1/tree/main/3.Transforma%C3%A7%C3%A3o/3.1.Modelagem_Dimensional)

### 3.2 Importação e Padronização
Descrição do processo de importação, padronizações e nomenclaturas amigáveis para o modelo dimensional.


> [Importação e Padronização](https://github.com/billyanalytics/Projeto1/tree/main/3.Transforma%C3%A7%C3%A3o/3.2.Importa%C3%A7%C3%A3o_e_Padroniza%C3%A7%C3%A3o)

### 3.3 Aferição de Medidas 📊
- Totais Gerais de Valor Original (Empenho)
- Totais Gerais Pago
- Totais Gerais a Pagar
   - medidas acima por:
      - Período (ano, bimestre e mês);
      - Órgão;
      - Item: Item Elemento, Item Categoria, Item Grupo;
      - Modalidade: item modalidade, modalidade licitação
        
> [Medidas](https://github.com/billyanalytics/Projeto1/tree/main/3.Transforma%C3%A7%C3%A3o/3.3.Aferi%C3%A7%C3%A3o_de_Medidas)

## 4. Load / Documentação e Apresentação 📊
### 4.1 Dataviz
- Importação dos Dados para a Plataforma de Dataviz (PowerBI, Tableau, etc.)
- Apresentação dos Dados em Gráficos

> [PowerBI](https://github.com/billyanalytics/Projeto1/tree/main/3.Transforma%C3%A7%C3%A3o/3.3.Aferi%C3%A7%C3%A3o_de_Medidas)

### 4.2 Documentação 📄
- [Modelagem Lógica](https://github.com/billyanalytics/Projeto1/blob/main/2.Extra%C3%A7%C3%A3o/2.2.Modelagem%20L%C3%B3gica/Diagrama%20_tabela_financeiro.pdf) , [Modelagem Dimensioanal](https://github.com/billyanalytics/Projeto1/tree/main/3.Transforma%C3%A7%C3%A3o/3.1.Modelagem_Dimensional)  e [Scripts](https://github.com/billyanalytics/Projeto1/tree/main/Script)
- [Dicionários de Dados](https://github.com/billyanalytics/Projeto1/tree/main/Documenta%C3%A7%C3%A3o)


## 5. GitHub Repository 🐙
Criação de um repositório no GitHub com linguagem de marcação Markdown para documentar todo o projeto.

### 5.1 Estrutura de Pastas 💼
- Extracao
- Transformacao
- Apresentação
- Documentacao
- Script


## Contribuições

Sinta-se à vontade para contribuir adicionando novos comandos SQL ou aprimorando os existentes. Basta criar um fork do repositório, fazer suas alterações e enviar um pull request.

## 🎁 Expressões de gratidão

* Compartilhe com outras pessoas esse projeto para mais pessoas terem acesso a esse repositório 📢;
* Quer saber mais sobre o projeto? Entre em contato para tomarmos um :coffee:;
> [!NOTE]
> Lembre-se sempre de usar comandos SQL com responsabilidade e em ambientes apropriados. Não nos responsabilizamos pelo uso indevido dos comandos contidos neste repositório.

---

<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=8F0D87&height=120&section=footer"/>


