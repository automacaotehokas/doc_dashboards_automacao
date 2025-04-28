# Proposta Automatizada para Solar

Esta seção descreve como criar uma proposta automatizada para sistemas de energia solar (UFV's para GD ou GC). Estas propostas podem incluir equipamentos fornecidos pela Blutrafos e/ou itens de revenda de parceiros (formando um KIT).

## Acessando a tela de criação de proposta

O processo para iniciar a criação de uma proposta automatizada solar é o mesmo das propostas de transformadores:

1.  Identifique a linha correspondente na tela principal de propostas.
2.  Clique na linha para abrir a tela de ações.
3.  Selecione a opção "Revisão".
4.  Na tela de listagem de revisões, selecione "Configurar Proposta" (se for a primeira revisão automatizada) ou clique no ícone "Revisar no aplicativo" em uma revisão existente.

![Tela Principal](img/tela_principal.png)
![Tela de Ações](img/tela_acao.png)
![Tela de Listagem/Criação de Revisões](img/tela_listagem_revisoes.png) <!-- Sugestão: Usar a imagem da tela de revisões -->

## Principais Campos e Parâmetros:

### Campos de Percentuais e Margens:

![Sidebar de Impostos e Margens](img/nav_impostos_proposta_solar.png) <!-- **Sugestão:** Usar uma imagem específica se a sidebar for diferente para solar -->

Estes campos definem as bases para os cálculos de valores e são comuns a diferentes tipos de propostas.

| Campo                         | Descrição                                                                                                                               |
| :---------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------- |
| Lucro                         | Percentual do lucro desejado sobre o custo (ex: 4,5%).                                                                                  |
| ICMS                          | Percentual do ICMS aplicável (ex: 12%).                                                                                                 |
| Comissão                      | Percentual da comissão do agente (ex: 10%).                                                                                             |
| Tipo de Frete                 | Seleção: "CIF" (Custo, Seguro e Frete inclusos) ou "FOB" (Livre a Bordo - frete por conta do cliente).                                    |
| Local de Frete                | Seleção do local de destino ou origem para cálculo do frete.                                                                            |
| Frete                         | Percentual ou valor do frete (ex: 10%).                                                                                                 |
| Cliente Contribuinte do ICMS? | Seleção: "Sim" ou "Não". Se "Não", habilita os campos "DIFAL" (Diferencial de Alíquota) e "Fundo de Pobreza" para preenchimento (ex: 10%). |

---

### Configuração dos Itens Solares:

Diferente dos transformadores, a proposta solar é montada adicionando componentes específicos (Inversores, Módulos, etc.). A combinação desses itens definirá o escopo e valor total.

![Tela de Configuração de Itens Solares](img/campos_proposta_solar.png) <!-- **Sugestão:** Adicionar imagem da tela de configuração solar -->

#### 1. Inversores

| Campo      | Descrição                                    |
| :--------- | :------------------------------------------- |
| Marca      | Seleção ou digitação da marca do inversor.   |
| Potência   | Potência nominal do inversor (ex: kW).       |
| Valor      | Custo ou valor de venda unitário.            |
| Quantidade | Número de inversores deste tipo a incluir. |

#### 2. Módulos Fotovoltaicos

| Campo      | Descrição                                    |
| :--------- | :------------------------------------------- |
| Marca      | Seleção ou digitação da marca do módulo.     |
| Potência   | Potência de pico do módulo (ex: Wp).         |
| Valor      | Custo ou valor de venda unitário.            |
| Quantidade | Número de módulos deste tipo a incluir.    |

#### 3. Estruturas de Montagem

| Campo   | Descrição                                                                 |
| :------ | :------------------------------------------------------------------------ |
| Marca   | Seleção ou digitação da marca da estrutura.                               |
| Modelo  | Tipo da estrutura (ex: Solo, Telhado Cerâmico, Telhado Metálico, Laje). |
| Valor   | Custo ou valor de venda total para a estrutura necessária.                |

#### 4. Cabos

| Campo | Descrição                                                              |
| :---- | :--------------------------------------------------------------------- |
| Marca | Seleção ou digitação da marca/tipo dos cabos (ex: CC, CA).             |
| Valor | Custo ou valor de venda total estimado para os cabos do projeto.       |

#### 5. Cabine / Subestação (Opcional - Geralmente para GC)

| Campo         | Descrição                                                              |
| :------------ | :--------------------------------------------------------------------- |
| Concessionária| Nome da concessionária de energia (relevante para padrões de conexão). |
| Potência      | Potência da cabine/subestação (ex: kVA).                               |
| Valor         | Custo ou valor de venda da cabine/subestação.                          |

#### 6. Itens Blutrafos (Ex: Quadros, Eletrocentro Solar - se aplicável)

*   *(Esta seção precisaria ser detalhada se houver itens específicos fabricados pela Blutrafos que entram na proposta solar automatizada, similar aos transformadores BT/MT, com seus próprios campos e acessórios)*

---

## Rotina para Configurar Itens na Proposta Solar Automatizada:

1.  **Configure Percentuais e Margens:** Ajuste os valores na aba lateral conforme necessário.
2.  **Verifique Cabeçalho:** Confirme se o número da proposta e o cliente no topo da tela estão corretos.
3.  **Adicione Componentes:** Navegue pelas abas ou seções correspondentes a cada tipo de item (Inversores, Módulos, Estruturas, etc.).
    *   Preencha os campos específicos para cada componente (Marca, Potência, Quantidade, Valor).
    *   Clique em "Adicionar Item" (ou similar) para cada componente que fará parte da proposta.
4.  **Repita:** Adicione todos os componentes necessários para formar o sistema solar ofertado. O sistema calculará os totais (Escopo Solar, Valor Solar, etc.) com base nos itens adicionados.

!!! info "Tipo Solar (KIT vs Skid)"
    O sistema pode classificar automaticamente a proposta como **KIT** se ela incluir itens marcados como revenda/parceiros, ou como **Skid** se todos os componentes principais forem fornecidos diretamente pela Blutrafos (depende da configuração dos itens no sistema).

---

## Configuração de Prazos de Entrega e Eventos de Pagamento

Após adicionar todos os itens, configure as condições comerciais na aba "Entrega/Pagamento/Desvios" (ou similar).

![Aba de Prazos e Pagamentos Solar](img/prazos_eventos_proposta_solar.png) <!-- **Sugestão:** Usar imagem específica se a tela for diferente -->

### Parâmetros:

#### Prazos Gerais

*   **Prazo Aprovação Desenho (Cliente):** Dias que o cliente tem para aprovar.
*   **Prazo Entrega Desenho (Engenharia):** Dias para a engenharia fornecer.
*   **Prazo Fabricação/Entrega:** Prazo total para disponibilizar os equipamentos.

#### Eventos de Pagamento

*   Adicione ou remova marcos de pagamento.
*   Para cada marco, defina:
    *   **Percentual:** % do valor total a ser pago.
    *   **Dias:** Prazo em dias para o pagamento.
    *   **Evento:** Condição que dispara o pagamento (ex: Assinatura Contrato, Entrega Material, Conexão).
*   **Validação:** O sistema verificará se a soma dos percentuais é igual a 100%.

#### Desvios

*   Campo livre para registrar quaisquer condições ou itens não padrão considerados na proposta.

---

## Finalização da Proposta

1.  **Navegue até Resumo:** Vá para a aba "Resumo" (ou similar).
2.  **Revise:** Confira o resumo dos itens, valores totais, escopo (potência total calculada) e condições.
3.  **Adicione Comentários:** Insira observações gerais sobre a proposta, se necessário.
4.  **Confirme:** Clique em "Confirmar" (ou "Gerar Proposta").
5.  **Download:** O sistema gerará o documento da proposta (ex: WORD). Faça o download e salve-o no local apropriado.

![Aba de Finalização Solar](img/finalizacao_proposta_solar.png) <!-- **Sugestão:** Usar imagem específica se a tela for diferente -->
