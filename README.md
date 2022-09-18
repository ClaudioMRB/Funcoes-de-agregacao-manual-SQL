# Funcoes-de-agregacao-manual-
FUNÇÕES COUNT, SUM, AVG, MIN E MAX



## -----The SQL COUNT(), AVG() and SUM() Functions--------

##            As funções SQL COUNT(), AVG() e SUM()

[SQL COUNT(), AVG() and SUM() Functions (w3schools.com)](https://www.w3schools.com/sql/sql_count_avg_sum.asp#gsc.tab=0&gsc.q=min%2Fmax)



A função retorna o número de linhas que corresponde a um critério especificado.`COUNT()`

### COUNT() Sintaxe

SELECT COUNT(*column_name*)
FROM *table_name*
WHERE *condition*;

A função retorna o valor médio de uma coluna numérica. `AVG()`

**EXEMPLO 1**

**SELECT COUNT**(id) **FROM** tb_sale **WHERE** price > 500

(valor retorna a quantidade de linhas na coluna id com valores maiores que 500)

### AVG() Sintaxe

SELECT AVG(*column_name*)
FROM *table_name*
WHERE *condition*;

A função retorna a soma total de uma coluna numérica. `SUM()`

**EXEMPLO 1**

(SUPONDO QUE EU QUEIRA O PREÇO MÉDIO, ELE PEGARÁ TODAS AS LINHAS CUJO VALOR ESTEJA ACIMA DE 500 E ME RETORNA O PREÇO MÉDIO)

**SELECT AVG**(price) **FROM** tb_sale **WHERE** price > 500

### SUM() Sintaxe

SELECT SUM(*column_name*)
FROM *table_name*
WHERE *condition*;

**EXEMPLO 1**

(SUPONDO QUE EU QUEIRA A SOMA DOS PREÇOS QUE ESTÃO ACIMA DE 500, A FUNÇÃO SOMA VAI AGREGAR OS VALORES EM UM VALOR TOTAL)

**SELECT SUM**(price) **FROM** tb_sale **WHERE** price > 500



------

## Banco de dados de demonstração

Abaixo está uma seleção da tabela "Produtos" no banco de dados de amostras northwind:

| ProductID | ProductName                  | SupplierID | CategoryID | Unit                | Price |
| :-------- | :--------------------------- | :--------- | :--------- | :------------------ | :---- |
| 1         | Chais                        | 1          | 1          | 10 boxes x 20 bags  | 18    |
| 2         | Chang                        | 1          | 1          | 24 - 12 oz bottles  | 19    |
| 3         | Aniseed Syrup                | 1          | 2          | 12 - 550 ml bottles | 10    |
| 4         | Chef Anton's Cajun Seasoning | 2          | 2          | 48 - 6 oz jars      | 22    |
| 5         | Chef Anton's Gumbo Mix       | 2          | 2          | 36 boxes            | 21.35 |

------



## EXEMPLO DE CONTAGEM()

A seguinte instrução SQL encontra o número de produtos:

### Exemplo

SELECT COUNT(ProductID)
FROM Products;

**Nota:** Os valores NULL não são contados.

------

## Exemplo AVG()

A seguinte instrução SQL encontra o preço médio de todos os produtos:

### Exemplo

SELECT AVG(Price)
FROM Products;

**Nota:** Os valores NULL são ignorados.

------

## Banco de dados de demonstração

Abaixo está uma seleção da tabela "OrderDetails" no banco de dados de amostras northwind:

| OrderDetailID | OrderID | ProductID | Quantity |
| :------------ | :------ | :-------- | :------- |
| 1             | 10248   | 11        | 12       |
| 2             | 10248   | 42        | 10       |
| 3             | 10248   | 72        | 5        |
| 4             | 10249   | 14        | 9        |
| 5             | 10249   | 51        | 40       |

------

## Exemplo de SOMA()

A seguinte instrução SQL encontra a soma dos campos "Quantidade" na tabela "OrderDetails":

### Exemplo

SELECT SUM(Quantity)
FROM OrderDetails;

**Nota:** Os valores NULL são ignorados.



## ---------------------As funções SQL MIN() e MAX()----------------------

[Funções SQL MIN() e MAX() (w3schools.com)](https://www.w3schools.com/sql/sql_min_max.asp)



A função retorna o menor valor da coluna selecionada.`MIN()`

A função retorna o maior valor da coluna selecionada.`MAX()`

### Min() Sintaxe

SELECT MIN(*column_name*)
FROM *table_name*
WHERE *condition*;

### Sinttaxa MAX()

SELECT MAX(*column_name*)
FROM *table_name*
WHERE *condition*;



**EXEMPLO 1**

Me retorna a linha que tenha o menor valor de price.

**SELECT MIN**(price) **FROM** tb_sale **WHERE** price > 500

------

## Banco de dados de demonstração

Abaixo está uma seleção da tabela "Produtos" no banco de dados de amostras northwind:

| ProductID | ProductName                  | SupplierID | CategoryID | Unit                | Price |
| :-------- | :--------------------------- | :--------- | :--------- | :------------------ | :---- |
| 1         | Chais                        | 1          | 1          | 10 boxes x 20 bags  | 18    |
| 2         | Chang                        | 1          | 1          | 24 - 12 oz bottles  | 19    |
| 3         | Aniseed Syrup                | 1          | 2          | 12 - 550 ml bottles | 10    |
| 4         | Chef Anton's Cajun Seasoning | 2          | 2          | 48 - 6 oz jars      | 22    |
| 5         | Chef Anton's Gumbo Mix       | 2          | 2          | 36 boxes            | 21.35 |

------

## Min() Exemplo

A seguinte declaração SQL encontra o preço do produto mais barato:

### Exemplo

SELECT MIN(Price) AS SmallestPrice
FROM Products;

------

## Exemplo MAX()

A seguinte declaração SQL encontra o preço do produto mais caro:

### Exemplo

SELECT MAX(Price) AS LargestPrice
FROM Products;

**EXEMPLO 1**

Me retorna a linha que tenha o maior valor de price.

**SELECT MAX**(price) **FROM** tb_sale **WHERE** price > 500
