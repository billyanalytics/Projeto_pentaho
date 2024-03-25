Para fazermos essa dimensão utilizamos os steps na imagem Dim_cliente e importamos as seguintges tabelas

TABELA ENDERECO
```sql
SELECT e.id_pessoa 
	 , e.rua AS endereco
	 , b.descricao  AS bairro
	 , c.descricao  AS cidade 
	 , e2.descricao AS estado 
FROM ods.endereco e
JOIN ods.bairro b ON e.id_bairro = b.id 
JOIN ods.cidade c ON c.id = b.id_cidade 
JOIN ods.estado e2 ON e2.id = c.id_estado 
ORDER BY e.id_pessoa 
```
TABELA CONTATO
```sql
SELECT
  id
, id_tipo_contato
, id_pessoa
, valor
, principal
FROM ods.contato
```
TABELA PESSOA
```sql
SELECT id, nome AS nome_ou_razao_social, cpf AS cpf_cnpj
FROM ods.pessoa_fisica pf 
UNION
SELECT id, razao_social AS nome_ou_razao_social, cnpj AS cpf_cnpj
FROM ods.pessoa_juridica pj 
order by 1
```
TABELA CLIENTE
```sql
SELECT DISTINCT id_cliente 
FROM ods.nota_fiscal nf
ORDER BY 1; 
```
