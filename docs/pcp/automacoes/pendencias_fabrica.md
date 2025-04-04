# ⚙️ Automação: Pendências de Fábrica

---

##  Informações Gerais

| Categoria             | Detalhe                                      |
| :-------------------- | :------------------------------------------- |
| **Nome da Empresa:** | Tehokas                                      |
| **Empresa Destino:** | Blutrafos                                    |
| **Criador:** | Eric Cangussu                                |
| **Data Elaboração:** | 03/04/2025                                   |
| **Departamento Dest.:**| PCP e Fábrica                                |
| **Tarefa Destino:** | Preenchimento e Análise de Pendências Fábrica|
| **Versão:** | 1.0                                          |
| **Prazo Revisão:** | 03/05/2025                                   |

---

##  Introdução

Esta automação visa apontar e analisar pendências identificadas na fábrica. Por meio dos apontamentos no quadro de pendências, é possível identificar problemas e implementar ações para otimizar a eficiência da produção.

---

##  Funcionamento

1.  **Envio de relatório Semanal:** Toda segunda-feira pela manhã, é enviado um e-mail a Diretoria com o relatório detalhado das pendências identificadas na fábrica.
2.  **Apontamentos do Quadro de Pendências:** O responsável de cada setor deve abrir o formulário para registrar as pendências identificadas. É necessário informar a data da identificação, a OV (Ordem de Venda/Produção) correspondente, o setor impactado, a situação ocorrida e uma descrição detalhada do problema.
3.  **Complemento das Informações:** O **Responsável pelo Indicador** deve complementar os dados através de uma **Sharepoint List** específica. O acesso a esta lista é restrito.
    * **Nome do Setor:** PCP
    * **Endereço do Formulário:** [Formulário de Pendências](https://solucoestehokas.sharepoint.com/:l:/s/Blutrafos_GestoCompartilhada/FCfdvca-O1xOl4MkwisOC-IBDYL5aTGkWKBTyA7sNSWkfQ?nav=M2U4MWIyM2QtODJjOC00Y2NkLTgyZjctOTA5MDA0Njg2MTNj)
    * **Nome da Sharepoint List:** `Plano de Ação - Fábrica`
    * **Endereço Sharepoint List:** [Plano de Ação - Fábrica](https://solucoestehokas.sharepoint.com/sites/Blutrafos_GestoCompartilhada/Lists/Plano%20de%20Ao%20%20Fbrica%20%20Blutrafos/Pendncias%20Abertas.aspx?env=WebViewList)
    * **Detalhes das Colunas:**

        | Nº | Coluna                       | Como Preencher                                                                                                  | Quem Preenche                               |
        | :- | :--------------------------- | :-------------------------------------------------------------------------------------------------------------- | :------------------------------------------ |
        | 1  | **Data Identificação** | Insira a data exata em que a pendência foi originalmente identificada.                                             | Responsável do Setor (via Formulário)       |
        | 2  | **OV (Ordem Venda/Prod.)** | Insira o número da OV/OP principal relacionada à pendência. (**Campo Crucial!**)                                  | Responsável do Setor (via Formulário)       |
        | 3  | **Cliente** | Nome do cliente associado à OV/OP impactada.                                                                      | **Sistema (Automático)** |
        | 4  | **Valor** | Valor monetário da OV/OP ou impacto estimado da pendência.                                                        | **Sistema (Automático)** |
        | 5  | **Setor Impactado** | Selecione na lista o setor da fábrica diretamente afetado.                                                      | Responsável pelo Indicador (via Sharepoint) |
        | 6  | **Desvio / Situação** | Selecione na lista o tipo de problema ocorrido (ex: Falta de material, Erro de processo).                         | Responsável pelo Indicador (via Sharepoint) |
        | 7 | **Descrição** | Relato detalhado sobre a pendência (o quê, onde, como). Seja claro e objetivo.                                | Responsável do Setor (via Formulário)       |
        | 8 | **Detrator** | Selecione a categoria principal do problema (ofensor) para análise (ex: Qualidade, Prazo, Custo).               | Responsável pelo Indicador (via Sharepoint) |
        | 9 | **Área Responsável** | Selecione a área/departamento responsável por analisar e implementar a solução.                                   | Responsável pelo Indicador (via Sharepoint) |
        | 10 | **Responsável** | Indique o(s) nome(s) da(s) pessoa(s) encarregada(s) de executar o plano de ação.                               | Responsável pelo Indicador (via Sharepoint) |
        | 11 | **Ação** | Descreva a ação corretiva ou o plano definido para solucionar a pendência.                                        | Responsável pelo Indicador (via Sharepoint) |
        | 12 | **1ª Data Prevista Solução** | Insira a data inicial estimada para a conclusão da ação corretiva.                                                 | Responsável pelo Indicador (via Sharepoint) |
        | 13 | **Data Efetiva Resolução** | Insira a data real em que a pendência foi resolvida. Preencher apenas na conclusão.                             | Responsável pelo Indicador (via Sharepoint) |
        | 14 | **Causa Raiz Detalhada** | Descreva a causa fundamental que originou a pendência, após análise.                                            | Responsável pelo Indicador (via Sharepoint) |
        | 15 | **Data Mapa** | Data de realização/atualização do mapa.                                                                           | **Sistema (Automático)** |
        | 16 | **Mapa** | Último mapa do item.                                                                                              | **Sistema (Automático)** |
        | 17 | **Situação** | **Calculado automaticamente.** Reflete o status atual (Aberta, Concluída, etc.). **Não preencher manualmente.** | **Sistema (Automático)** |
        | 18 | **Status Entrega** | **Calculado automaticamente.** Impacto no status da entrega (No Prazo, Atrasada, etc.). **Não preencher.** | **Sistema (Automático)** |
        | 19 | **Causa Raiz** | Selecione uma categoria mais ampla para a causa raiz identificada.                                                | Responsável pelo Indicador (via Sharepoint) |
        | 20 | **Raiz** | Selecione um nível mais específico ou sub-fator da Causa Raiz (se aplicável).                                     | Responsável pelo Indicador (via Sharepoint) |
        | 21 | **Prazo Montagem** | Insira o prazo (dias/data) da etapa de montagem relacionada, se aplicável.                                        | Responsável pelo Indicador (via Sharepoint) |
        | 22 | **Data Necessidade PCP** | **Calculado automaticamente.** Data limite para resolução sem impactar planejamento. **Não preencher.** | Responsável pelo Indicador (via Sharepoint) *[Nota: verificar se é sistema ou manual]* |
        | 23 | **1ª a 5ª Repactuação** | Caso a data prevista não seja cumprida, registre as novas datas acordadas sequencialmente.                        | Responsável pelo Indicador (via Sharepoint) |
        | 24 | **Dias Parados** | Registre o número total de dias em que a produção/processo ficou parado devido à pendência.                     | Responsável pelo Indicador (via Sharepoint) |
        | 25 | **Data Prevista Resolução** | **Calculado automaticamente.** Mostra a data de resolução atual (1ª prevista ou última repactuada). **Não preencher.** | **Sistema (Automático)** |
        | 26 | **Qtde Reprog** | **Calculado automaticamente.** Conta quantas vezes a data de solução foi reprogramada. **Não preencher.** | **Sistema (Automático)** |

4.  **Base para Dashboards e Automações:** Os dados salvos nesta lista servem como fonte para a atualização do dashboard "**Pendências de Fábrica**" e para outras automações relacionadas.

5. **Fim do processo**: Após a conclusão do processo, os dados salvos na lista são utilizados para atualizar o dashboard "**Pendências de Fábrica**" e para outras automações relacionadas.

---

##  Benefícios

* **Transparência:** Garante que as pendências estejam visíveis e acessíveis para todas as áreas interessadas.
* **Consistência:** Padroniza o processo de registro de desvios no processo produtivo.
* **Agilidade:** Otimiza a atualização do dashboard e a execução de outras automações dependentes destes dados.
* **Rastreabilidade:** Permite acompanhar o histórico das pendências e gerar indicadores de desempenho.

---

##  Responsáveis

* **Apontamento pela Fábrica:** O **Responsável de Setor** deve inserir as pendências *diariamente* no formulário designado.
* **Complemento das Informações:** O **Responsável pelo Indicador** deve enriquecer os registros na Sharepoint List com dados como causa raiz, plano de ação, prazos, etc.
* **Sistema (Automação):** O sistema preenche e atualiza automaticamente diversas colunas, reduzindo a necessidade de preenchimento manual e garantindo a consistência dos dados.

---

## ⚠️ Observações Importantes

* É **crucial** que o apontador da fábrica preencha o número da **OV** corretamente, pois a automação utiliza este campo para identificar e vincular informações.
* O **Responsável pelo Indicador** deve preencher as informações adicionais com base em seu conhecimento técnico e nas diretrizes estabelecidas, garantindo a qualidade da análise de causa raiz e do plano de ação.

---

##  Recursos
* É necessário que a fábrica possua pelo menos um computador disponível para acesso à internet.
* O formulário deve ser acessado pelo navegador de internet.
* O apontador deve ter acesso concedido aos formulários do Sharepoint.
* O responsável pelo indicador deve ter acesso concedido aos formulários do Sharepoint.
* Pelo menos um da empresa ou a empresa de consultoria deve ter uma licença Standarte ou superior da Microsoft 365.

---

## 📜 Histórico de Versões

| Versão | Data       | Autor         | Descrição      |
| :----- | :--------- | :------------ | :------------- |
| 1.0    | 03/04/2025 | Eric Cangussu | Versão inicial |