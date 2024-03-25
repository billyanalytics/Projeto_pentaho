Para fazermos essa dimensão utilizamos os steps na imagem Dim_vendedor e importamos as seguintges tabelas

TABELA PESSOA FISICA
```sql
SELECT
  id
, nome
, cpf
FROM ods.pessoa_fisica
order by id
```
TABELA VENDEDOR
```sql
SELECT DISTINCT id_vendedor 
FROM ods.nota_fiscal nf
ORDER BY 1; 
```
