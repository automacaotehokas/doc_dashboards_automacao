# Dashboard: Status Projeto

O dashboard este dashboard aborda o status de entrega e de andamento dos projetos elétricos e mecânicos. O objetivo é medir o progresso e identificar possíveis impactos no cronograma de fabricação.

## Métricas e Informações

*   **Status Projetos Recebidos:** Número de projetos mecânicos que foram entregues com RISCO ("Com Atraso") e projetos que não foram entregues com RISCO ("Sem Atraso").
*   **Risco de Projetos em Andamento:** Número de projetos mecânicos que estão em andamento e que estão com RISCO ("Com Atraso") e projetos que não estão com RISCO ("Sem Atraso").

A regra gira em torno da Data Prevista de Projeto Mecânico, que varia de acordo com o tipo de produto:

|Tipo de Produto| Data de Referência| Dias|
|--------------|--------------------|-----|
BxBx| Primeira Data PCP |     15| 
Seco| Primeira Data PCP |     20|
QGBT| Primeira Data PCP |     40|
Skid| Primeira Data PCP |     40|
Óleo|   Primeira Data PCP |     40|
Sistema| Primeira Data PCP |     40|

Com esta data de referência, é possível calcular a data de entrega do projeto e granular o risco de atraso. Abaixo está a tabela de risco de atraso:



>**RISCO BAIXO:** Data de hoje menor que 20% de dias da data de referência.

>**RISCO MÉDIO:** Data de hoje entre 20% até o limite da data de referência.

>**RISCO ALTO:** Data de hoje maior que o limite da data de referência.

~~~python
Exemplo:
Tipo de Produto: BxBx
Dias: 15
Primeira Data PCP: 10/04/2024
Data Prevista de Projeto Mecânico: 25/04/2024
RISCO BAIXO: até 3 dias = 13/04;2024
RISCO MÉDIO: de 13/04/2024 até 25/04/2024
RISCO ALTO: maior que 25/04/2024
~~~

*   **Atraso por Mês:** % de atraso por mês (Data Prevista de Projeto Mecânico).
*   **Qtde de Projetos por Produto:** Quantidade de projetos elétricos dividido por produto e por Status, sendo:
    * Atraso: Projetos que estão em andamento e já ultrapassaram a Data Prevista de Projeto Elétrico.
    * No Prazo: Projetos que estão em andamento e não ultrapassaram a Data Prevista de Projeto Elétrico.
    * Entregue com Atraso: Projetos que já foram entregues, mas ultrapassaram a Data Prevista de Projeto Elétrico.
    * Entregue no Prazo: Projetos que já foram entregues e não ultrapassaram a Data Prevista de Projeto Elétrico.

*   **Valor e Quantidade por Etapa:** Valor e quantidade de projetos mecânicos e elétricos por etapa.



| Versão | Data       | Autor       | Descrição |
|--------|------------|-------------|-----------
| 1.0    |02/04/2025 | Eric Cangussu | Versão inicial.|