# Manual de Controle de OS - Assistência Técnica (Qualidade)

## Rotina de Criação

Para criar uma nova OS, acesse o sistema **Controle de OS** e siga os passos abaixo:

1. Abra a tela principal do sistema
2. Clique no botão verde **"Novo"**
3. Preencha os campos conforme o tipo do processo

### Campos do Formulário

| Campo | Descrição |
|-------|-----------|
| **Divisão** | Centro de Custo responsável |
| **Gestor** | Responsável pelo Processo |
| **OV** | Numeração da Ordem de Serviço (preservado como OS para adequação com dados GC) |
| **Cliente** | Nome da empresa contratante |
| **Nome da Obra** | Denominação para referenciar a obra do cliente |
| **Descrição do Produto** | Especificação técnica detalhada do produto |
| **Tipo de Produto** | Família/categoria do produto |
| **Endereço de Entrega** | Endereço completo para envio do equipamento (modalidade CIF) |
| **Local de Entrega** | Cidade e Estado de destino |
| **Data de Emissão do Pedido** | Data de cadastro do pedido no sistema |
| **Data Prevista de Entrega do Pedido** | Data estimada para entrega final |
| **Data de Chegada do Contrato** | Data de recebimento do contrato |
| **Data EFETIVA de Entrega Engenharia** | Data de transferência do processo para engenharia |
| **Prazo p/ Desenhos Detalhados** | Prazo estabelecido para produção do projeto elétrico completo |

> **Importante:** Após o preenchimento completo dos campos, clique em **"Salvar"** para confirmar a criação da OS.

---

## Etapas do Processo

### 00. Comercial
**Objetivo:** Resolução de pendências comerciais antes do início do processo técnico.

**Critério de Conclusão:**
- Preenchimento do campo `DT_CHEGADA_EM_CONTRATO`

**Responsável:** Gestor do Processo

---

### 01. Inicial
**Objetivo:** Análise documental e verificação de requisitos iniciais.

**Atividades:**
- Análise da documentação pela Qualidade/Assistência Técnica
- Verificação do pagamento inicial
- Validação das informações técnicas fornecidas pelo cliente

**Critério de Conclusão:**
- Preenchimento do campo `DT_EFETIVA_ENTREGA_ENGENHARIA`

**Responsável:** Gestor do Processo

---

### 04. Projeto Elétrico (Desenhos Detalhados)
**Objetivo:** Desenvolvimento de projetos e estruturação de materiais.

**Atividades:**
- Elaboração de projetos elétricos detalhados
- Estruturação de materiais no ERP
- Preparação para aquisição e abertura de OP

**Critério de Conclusão:**
- Preenchimento do campo `DT_EFETIVA_DESENHO_DETALHADO`

**Responsável:** Gestor do Processo

---

### 05. Abertura OP
**Objetivo:** Formalização da produção e requisição de materiais.

**Atividades:**
- Abertura de Ordens de Produção (OP)
- Solicitação de compras de materiais necessários

**Critérios de Conclusão:**
- Preenchimento dos campos:
  - `DT_EFETIVA_ABERTURA_OP`
  - `NÚMERO_OP`
  - `DATA_INICIAL_PCP`

**Responsável:** PCP (Planejamento e Controle de Produção)

---

### 07. Fabricação
**Objetivo:** Produção física dos equipamentos com controle de qualidade.

**Atividades:**
- Montagem dos equipamentos em fábrica
- Realização de testes funcionais
- Inspeções de qualidade

**Critério de Conclusão:**
- Preenchimento do campo `DT_EFETIVA_FABRICAÇÃO`

**Responsável:** Laboratório

---

### 09. Logística
**Objetivo:** Preparação e despacho do equipamento.

**Atividades:**
- Cotação de frete
- Emissão de Nota Fiscal
- Liberação pela Qualidade
- Despacho do equipamento

**Critério de Conclusão:**
- Preenchimento do campo `DT_EFETIVA_LOGÍSTICA`

**Responsável:** Gestor do Processo

---

### 09.1 Armazenagem (Etapa Opcional)
**Objetivo:** Guarda temporária do equipamento quando necessário.

**Condições de Ativação:**
- `NECESSITA_ARMAZENAGEM = SIM`
- Campo `PRAZO_ARMAZENAGEM` preenchido

**Aplicação:** Quando o cliente não puder receber o equipamento imediatamente.

**Responsável:** Gestor do Processo

---

### 10. Em Trânsito
**Objetivo:** Transporte do equipamento até o cliente.

**Aplicação:** Pedidos com frete CIF (Custo, Seguro e Frete por conta do fornecedor)

**Critério de Conclusão:**
- Preenchimento do campo `DT_EFETIVA_ENTREGA`

**Responsável:** Logística

---

### 11. Entregue
**Objetivo:** Finalização completa do processo.

**Condição:** Confirmação do recebimento pelo cliente

**Critério de Conclusão:**
- Confirmação registrada no sistema

**Responsável:** Logística

---

## Rotina de Atualização

### Procedimento de Edição

1. **Seleção:** Marque a(s) linha(s) desejada(s) na tabela principal
2. **Edição:** Clique no botão **"Editar"** na página inicial
3. **Navegação:** Utilize os filtros da aba **"Parâmetros"** conforme necessário

### Filtros de Visualização

A aba **"Parâmetros"** oferece diferentes visões organizadas cronologicamente:

| Filtro | Descrição | Etapa Relacionada |
|--------|-----------|-------------------|
| **Geral** | Informações básicas do processo | Visão inicial padrão |
| **Eng** | Colunas da fase de engenharia | 04. Projeto Elétrico |
| **Fabricação** | Colunas da fase produtiva | 07. Fabricação |
| **Faturamento** | Colunas da fase fiscal | 08. Inspeção/Faturamento |
| **Logística** | Colunas das fases de envio | 09. Logística e 10. Em Trânsito |
| **Suspensos** | Processos temporariamente interrompidos | Visão geral de suspensões |

### Finalização da Atualização

Após selecionar o parâmetro adequado e as linhas correspondentes:

1. Preencha o formulário de atualização com as informações necessárias
2. Clique em **"Salvar"** para confirmar as alterações

---

> **Nota:** Este manual deve ser consultado sempre que houver dúvidas sobre os procedimentos de criação e atualização de OS no sistema de Controle de Assistência Técnica.