Para fazermos a dimensão produto foi feitas as seguintes importações e na imagem as steps utilizadas

TABELA PRODUTO
```sql
SELECT
  id
, id_fornecedor
, id_categoria
, nome
, valor_venda
, valor_custo
FROM ods.produto
```
TABELA CATEGORIA 
```sql
SELECT
  id
, descricao
FROM ods.categoria
```
TABELA PESSOA JURÍDICA
```sql
SELECT
  id
, razao_social
, cnpj
FROM ods.pessoa_juridica
```
