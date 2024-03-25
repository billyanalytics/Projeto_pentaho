Esse foi o cidogo SQL usado para a exporta o banco de dados da produção para o `schema ODS` e na imagem `Criação_ods` esta a step utilizada para a transformação
```sql
DROP TABLE IF EXISTS ods.bairro;
CREATE TABLE ods.bairro AS
SELECT DISTINCT *
FROM geral.bairro;

DROP TABLE IF EXISTS ods.cidade;
CREATE TABLE ods.cidade AS
SELECT DISTINCT *
FROM geral.cidade;

DROP TABLE IF EXISTS ods.contato;
CREATE TABLE ods.contato AS
SELECT DISTINCT *
FROM geral.contato;

DROP TABLE IF EXISTS ods.endereco;
CREATE TABLE ods.endereco AS
SELECT DISTINCT *
FROM geral.endereco;

DROP TABLE IF EXISTS ods.estado;
CREATE TABLE ods.estado AS
SELECT DISTINCT *
FROM geral.estado; 

DROP TABLE IF EXISTS ods.pessoa;
CREATE TABLE ods.pessoa AS
SELECT DISTINCT *
FROM geral.pessoa;

DROP TABLE IF EXISTS ods.pessoa_fisica;
CREATE TABLE ods.pessoa_fisica AS
SELECT DISTINCT *
FROM geral.pessoa_fisica;

DROP TABLE IF EXISTS ods.pessoa_juridica;
CREATE TABLE ods.pessoa_juridica AS
SELECT DISTINCT *
FROM geral.pessoa_juridica;

DROP TABLE IF EXISTS ods.responsavel_juridico;
CREATE TABLE ods.responsavel_juridico AS
SELECT DISTINCT *
FROM geral.responsavel_juridico;

DROP TABLE IF EXISTS ods.tipo_contato;
CREATE TABLE ods.tipo_contato AS
SELECT DISTINCT *
FROM geral.tipo_contato;

DROP TABLE IF EXISTS ods.cargo;
CREATE TABLE ods.cargo AS
SELECT DISTINCT *
FROM rh.cargo;

DROP TABLE IF EXISTS ods.departamento;
CREATE TABLE ods.departamento AS
SELECT DISTINCT *
FROM rh.departamento;

DROP TABLE IF EXISTS ods.escolaridade;
CREATE TABLE ods.escolaridade AS
SELECT DISTINCT *
FROM rh.escolaridade;

DROP TABLE IF EXISTS ods.funcionario;
CREATE TABLE ods.funcionario AS
SELECT DISTINCT *
FROM rh.funcionario;

DROP TABLE IF EXISTS ods.lotacao;
CREATE TABLE ods.lotacao AS
SELECT DISTINCT *
FROM rh.lotacao;

DROP TABLE IF EXISTS ods.categoria;
CREATE TABLE ods.categoria AS
SELECT DISTINCT *
FROM vendas.categoria;

DROP TABLE IF EXISTS ods.forma_pagamento;
CREATE TABLE ods.forma_pagamento AS
SELECT DISTINCT *
FROM vendas.forma_pagamento;

DROP TABLE IF EXISTS ods.item_nota_fiscal;
CREATE TABLE ods.item_nota_fiscal AS
SELECT DISTINCT *
FROM vendas.item_nota_fiscal;

DROP TABLE IF EXISTS ods.nota_fiscal;
CREATE TABLE ods.nota_fiscal AS
SELECT DISTINCT *
FROM vendas.nota_fiscal;

DROP TABLE IF EXISTS ods.produto;
CREATE TABLE ods.produto AS
SELECT DISTINCT *
FROM vendas.produto;
```
