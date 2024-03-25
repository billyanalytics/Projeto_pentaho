Para fazermos essa dimensão utilizamos os steps na imagem Dim_funcionario e importamos as seguintges tabelas 

TABELA PESSOA FISICA
```sql
SELECT
  id
, nome
, cpf
FROM ods.pessoa_fisica
order by id
```
TABELA FUNCIONARIO
```sql
SELECT *
FROM ods.funcionario f 
FULL JOIN ods.lotacao l ON f.id = l.id 
FULL JOIN ods.cargo c ON c.id = l.id_cargo 
FULL JOIN ods.departamento d ON d.id = l.id_departamento 
JOIN ods.escolaridade e ON f.id_escolaridade = e.id  
ORDER BY f.id 
```
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
