importação tabela `Nota_Fiscal` e da tabela `Item_nota_fiscal`. Na imagem as steps utilizadas para a criação da `Dim_fato`

```sql
SELECT
  id
, id_vendedor
, id_cliente
, id_forma_pagto
, data_venda
, numero_nf
, total
FROM ods.nota_fiscal
```
<br>

```sql
SELECT
  id
, id_produto
, id_nota_fiscal
, quantidade
, valor_venda_real
FROM ods.item_nota_fiscal
``` 
