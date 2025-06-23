# Manual de Documentação: Rotina de Agendamento de Inspeções GC

| Categoria             | Detalhe                                      |
| :-------------------- | :------------------------------------------- |
| **Nome da Empresa:** | Tehokas                                      |
| **Empresa Destino:** | Blutrafos                                    |
| **Criador:** | Eric Cangussu                                |
| **Data Elaboração:** | 16/04/2025                                   |
| **Departamento Dest.:**| GC , PCP e Engenharia                             |
| **Tarefa Destino:** | Controle de Inspeções GC                            |
| **Versão:** | 1.0                                          |
| **Prazo Revisão:** | 16/05/2025                                   |

---

Bem-vindo ao manual de documentação para a rotina de **Agendamento e Acompanhamento de Inspeções da Gestão Compartilhada (GC)**.
Este documento serve como guia central para entender, executar e gerenciar esta atividade.

Utilize o índice abaixo para navegar rapidamente para a seção desejada neste documento.


---

# 1. Introdução

### 1.1. Propósito da Rotina

O objetivo central desta rotina e da documentação associada é **organizar e garantir o agendamento eficiente das inspeções de Ordens de Venda (OV) junto aos clientes**, através de um sistema de alertas proativos direcionados aos Gestores de Contratos.

Além disso, visa centralizar e comunicar eficientemente a programação dessas inspeções, assegurando a visibilidade necessária para as equipes de Laboratório e PCP (Planejamento e Controle da Produção).

### 1.2. Escopo e Limitações

**Escopo:**
* Esta rotina cobre o processo desde a identificação da necessidade de inspeção para uma OV (marcada como `Inspeção = "Sim"` e com prazo definido) até a confirmação do agendamento e notificação das partes interessadas (Laboratório e PCP).
* Inclui automações para lembretes de agendamento e e-mails de confirmação.
* Inclui o uso do aplicativo Power Apps para registro dos detalhes da inspeção.

**Fora do Escopo:**
* A execução da inspeção em si.
* O processo de faturamento associado.
* A gestão de OVs que não requerem inspeção.

### 1.3. Público-Alvo do Manual

Este manual destina-se aos seguintes públicos:
* **Gestores de Contrato (GC):** Principais usuários do processo para agendar e confirmar inspeções.
* **Equipe de PCP:** Para consulta de programação e planejamento.
* **Equipe do Laboratório:** Para consulta de programação e preparação para os ensaios.
* **Equipe de TI/Suporte:** Para entendimento do fluxo e manutenção das automações e aplicativo.
* **Gestores de Área:** Para visão geral do processo e acompanhamento.

### 1.4. Visão Geral do Processo

O fluxo de trabalho desta rotina envolve as seguintes etapas principais, suportadas por automações e interações no aplicativo Power Apps:

1.  **Monitoramento e Alerta:** Uma automação identifica OVs que necessitam de inspeção (`Inspeção = "Sim"`) e calcula a data limite para agendamento. Próximo a essa data, dispara alertas automáticos via e-mail e notificação no App para o Gestor responsável.
2.  **Agendamento da Inspeção:** O Gestor utiliza o aplicativo Power Apps para registrar a data/hora da inspeção, selecionar os equipamentos, ensaios e laboratório. O status inicial é "Pendente".
3.  **Atualização e Comunicação:** O agendamento registrado atualiza a lista SharePoint principal ("Base GC") e cria um registro na lista de inspeções (`base_inspecao_gc_blutrafos`), que alimenta a visão de Calendário compartilhada.
4.  **Confirmação e Notificação:** Após confirmação (via app ou SharePoint), o Status muda para "Confirmado", o que dispara um e-mail automático com o extrato da inspeção para o Laboratório e PCP.

<br>

---
# 2. Pré-requisitos

Antes de executar ou interagir com esta rotina, certifique-se de que os seguintes pré-requisitos são atendidos:

### 2.1. Sistemas e Ferramentas Necessárias
* Acesso à rede corporativa e Internet.
* Navegador web atualizado.
* Cliente de E-mail (Outlook).
* Acesso ao aplicativo Power Apps de Agendamento de Inspeções GC.
* Acesso às listas SharePoint relevantes (com permissão de leitura/escrita conforme o papel).

### 2.2. Dados e Informações de Entrada
* **Na Lista `Base OV - GC - BLUTRAFOS - REV01` (ou similar):**
    * OV corretamente cadastrada.
    * Campo `Inspeção` definido como "Sim".
    * Campo `Prazo Inspeção` (ou similar) preenchido com o número de dias de antecedência para agendamento.
    * Campo `Data Operacional` preenchido corretamente.
    * Campo `Gestor (GC)` atribuído corretamente.
    * Campos `OV`, `Cliente`, `Equipamento` (ou `field_15`, `field_16`) preenchidos.
* **No Aplicativo Power Apps:**
    * Listas de Laboratórios e Gestores (GC) disponíveis para seleção.
    * Opções de Ensaios (Rotina, Tipo) disponíveis.

### 2.3. Permissões e Acessos Requeridos
* **Gestor de Contratos:** Permissão de Leitura/Escrita na lista `Base OV - GC - BLUTRAFOS - REV01` (para ver OVs e ter `Data Programada Inspeção` atualizada) e permissão de Contribuição na lista `base_inspecao_gc_blutrafos` (para criar/editar agendamentos). Acesso ao Power App.
* **PCP e Laboratório:** Permissão de Leitura (pelo menos) na lista `base_inspecao_gc_blutrafos` e acesso à exibição de Calendário. Acesso aos e-mails de notificação.
* **Administrador/TI:** Permissões para gerenciar as listas SharePoint, o Power App e os fluxos do Power Automate associados.

### 2.4. Conhecimentos Necessários
* Entendimento do fluxo comercial e de produção que exige a inspeção.
* Familiaridade com o uso básico do SharePoint e do Power Apps.
* Conhecimento dos procedimentos internos para contato com cliente e laboratório para definição de datas.

<br>

---
# 3. Procedimento de execução

Esta seção detalha as etapas sequenciais da rotina.

### 3.1. Etapa 1: Automação - Lembrete para Programar Inspeção

Esta automação (provavelmente um fluxo do Power Automate) é responsável por iniciar o processo, lembrando o Gestor da necessidade de agendar inspeções pendentes.

* **Fonte de Dados Monitorada:** Lista SharePoint: `Base OV - GC - BLUTRAFOS - REV01` (Confirmar nome se diferente)
* **Gatilho da Automação:** Execução agendada (ex: diariamente).
* **Lógica de Processamento por Item:** Para cada item na lista fonte, a automação verifica:
    1.  Se `[Inspeção]` é igual a `"Sim"`.
    2.  Se `[Data Programada Inspeção]` (ou nome similar que indica agendamento) está **em branco**.
    3.  Se o `[Prazo Inspeção]` (ou nome similar, indicando prazo para *agendar*) é maior que zero.
* Se as condições acima forem verdadeiras, calcula:
    * `Data Limite para Programar = [Data Operacional] - [Prazo Inspeção]` (dias)
    * `Data de Início dos Lembretes = Data Limite para Programar - 10` (dias)
* Compara a `Data de Início dos Lembretes` com a data atual.
* **Ação Desencadeada:** Se a data atual for **maior ou igual** à `Data de Início dos Lembretes`:
    * Enviar E-mail para o `[Gestor (GC)]` do item. (Conteúdo: Lembrar sobre pendência, OV, Cliente, Prazo Limite).
    * Enviar Notificação via Aplicativo Power Apps para o `[Gestor (GC)]`. (Conteúdo: Similar ao e-mail).
* **Frequência dos Alertas:** Definida na automação (ex: diária). Cessam quando `[Data Programada Inspeção]` é preenchida.

<br>

### 3.2. Agendamento e Confirmação da Inspeção (Via Aplicativo Power Apps)

Esta etapa é realizada pelo Gestor de Contratos através do aplicativo Power Apps dedicado.

* **Passos no Aplicativo:**
    1.  **Seleção de Itens:** O Gestor seleciona um ou mais itens da OV (`colMinhaColecaoPowerBI`) que farão parte da inspeção. A validação de mesma OV é feita ao tentar adicionar itens à coleção `itensinspecao`. Pode usar a opção "Selecionar Tudo por OV" (`selecionar_tudo_ov_inspecao`). É necessário selecionar pelo menos um item manualmente para definir a OV alvo.
    2.  **Preenchimento dos Dados:** O Gestor informa os detalhes da programação no formulário (`nova_insp`) do aplicativo: Data/Hora Início, Data/Hora Fim, Laboratório, Gestor (GC), Ensaios (Rotina/Tipo), Observações.
    3.  **Criação do Registro (Botão Salvar/Submit):**
        * O App valida se `itensinspecao` não está vazia.
        * Determina a `colecaoFonte` (baseado no checkbox "Selecionar Tudo").
        * Valida se `colecaoFonte` não está vazia.
        * Valida se todos os campos obrigatórios do formulário estão preenchidos.
        * Se todas as validações passarem, executa `Patch` na lista `base_inspecao_gc_blutrafos` para criar um novo registro com status inicial "Pendente".
        * Executa `UpdateIf` na lista `Base OV - GC - BLUTRAFOS - REV01` para preencher a `Data Programada Inspeção` nos itens da `colecaoFonte`.
        * Limpa a seleção (`itensinspecao`) e reseta o formulário (`ResetForm(nova_insp)`).
    4.  **Visibilidade:** O novo item aparece no Calendário.

<br>

### 3.3. Confirmação da Inspeção e E-mail Automático

Esta etapa finaliza o agendamento e notifica as partes interessadas.

1.  **Alteração de Status:** O Gestor ou responsável altera o `Status` do registro correspondente na lista `base_inspecao_gc_blutrafos` de "Pendente" para **"Confirmado"**. Isso pode ser feito via Power Apps (se houver funcionalidade de edição) ou diretamente no SharePoint.
2.  **Gatilho de E-mail:** Uma segunda automação (Power Automate) monitora a lista `base_inspecao_gc_blutrafos`.
    * **Gatilho:** Quando um item é modificado e o campo `Status` é igual a "Confirmado".
    * **Ação:** Enviar e-mail para o Laboratório (baseado no campo `Laboratório`) e para a lista de e-mails do PCP.
    * **Conteúdo do E-mail:** Um extrato formatado da inspeção confirmada (OV, Cliente, Datas, Equipamentos, Ensaios, Laboratório, Observações).

<br>

*(Adicione outras subseções de procedimento conforme necessário)*

---
# 4. Frequência e saídas

### 4.1. Frequência
* **Automação de Lembrete:** Execução Agendada (ex: Diariamente).
* **Uso do Aplicativo (Agendamento):** Sob demanda, conforme necessidade dos Gestores de Contrato.
* **Automação de Confirmação:** Disparada por Evento (Modificação de item na lista `base_inspecao_gc_blutrafos` com Status = "Confirmado").

### 4.2. Saídas (Resultados)
* Registros criados na lista `base_inspecao_gc_blutrafos` com detalhes do agendamento.
* Atualização do campo `Data Programada Inspeção` na lista `Base OV - GC - BLUTRAFOS - REV01`.
* Visão de Calendário atualizada para Laboratório e PCP.
* E-mails de lembrete enviados aos Gestores.
* E-mails de confirmação enviados ao Laboratório e PCP.
* (Opcional) Dados disponíveis para análise e relatórios em Power BI.

<br>



<br>

---