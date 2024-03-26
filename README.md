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
![Badge em FInalizado](https://img.shields.io/static/v1?label=STATUS&message=FINALIZADO&color=GREEN&style=for-the-badge)

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
     
> [Extração](https://github.com/billyanalytics/Projeto_pentaho/tree/main/Extra%C3%A7%C3%A3o)

### 2.1.2 **Tratamento e Carga**
Nesse passo começamos a montar as Dimensões e a tabela Fato já carregando o resultado para o DW. O DW foi modelado usando um esquema Snowflake, com tabelas de fato e dimensão projetadas para otimizar consultas analíticas. Para tornar o tratamento mais organizado e limpo montamos um JOB que também será usado para automatizar a atualização do Data Warehouse integrado com envio de um e-mail para informar que o DW foi atualizado

> [fat_notafiscal](https://github.com/billyanalytics/Projeto_pentaho/tree/main/fat_notafiscal)
> 
> [Dimensão_data](https://github.com/billyanalytics/Projeto_pentaho/tree/main/Dim_data)
> 
> [Dimensão_produto](https://github.com/billyanalytics/Projeto_pentaho/tree/main/Dim_produto)
> 
> [Dimensão_pagamento](https://github.com/billyanalytics/Projeto_pentaho/tree/main/Dim_forma_de_pagamento)
> 
> [Dimensão_funcionario](https://github.com/billyanalytics/Projeto_pentaho/tree/main/Dim_funcionario)
> 
> [Dimensão_vendedor](https://github.com/billyanalytics/Projeto_pentaho/tree/main/Dim_vendedor)
> 
> [Dimensão_cliente](https://github.com/billyanalytics/Projeto_pentaho/tree/main/Dim_cliente)
> 
> [JOB](https://github.com/billyanalytics/Projeto_pentaho/tree/main/Job)

### 3. **Documentação** 📄
#### 3.1 **Banco de dados**
- [Modelagem Dimensioanal_BD](https://github.com/billyanalytics/Projeto_pentaho/blob/main/Documentacao/Relacional_bd.png)
- [Modelagem Dimensioanal_ODS](https://github.com/billyanalytics/Projeto_pentaho/blob/main/Documentacao/Relacional_ods.png)
#### 3.2 **DW**
- [Modelagem Dimensioanal_DW](https://github.com/billyanalytics/Projeto_pentaho/blob/main/Documentacao/Relacional_DW.png)
- [E-mail_de_atualização_automático](https://github.com/billyanalytics/Projeto_pentaho/blob/main/Documentacao/email.png) : Programado para o dia 26/03/24 as 11:10 🕦

## Contribuições

Sinta-se à vontade para contribuir adicionando novos comandos SQL ou aprimorando os existentes. Basta criar um fork do repositório, fazer suas alterações e enviar um pull request.

## 🎁 Expressões de gratidão

* Compartilhe com outras pessoas esse projeto para mais pessoas terem acesso a esse repositório 📢;
* Quer saber mais sobre o projeto? Entre em contato para tomarmos um :coffee:;
> [!NOTE]
> Lembre-se sempre de usar comandos SQL com responsabilidade e em ambientes apropriados. Não nos responsabilizamos pelo uso indevido dos comandos contidos neste repositório.

---

<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=8F0D87&height=120&section=footer"/>


