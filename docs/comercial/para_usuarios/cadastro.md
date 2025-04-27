# Cadastros 

Nesta secção iremos abordar em como inserir novas propostas, clientes e contatos.

## Acesso Rápido
- [Cadastro de Propostas](#propostas)
- [Cadastro de Clientes](#cliente)
- [Cadastro de Contatos](#contato)


## Propostas

#### Principais Campos e Parâmetros:

| Campo  | Descrição |
| ------ | --------- |
| Número |Número sequêncial único para identificar a proposta.Gerado automaticamente ao selecionar o tipo de proposta |
| Tipo   |Referse-se ao tipo de produto predominante da proposta. Ex: "Solar GC","T", "P". Mais sobre o significado das siglas descrito abaixo.|
|Obra | Referência ao nome da obra do cliente que a proposta está relacionada. |
|Cliente/Contato| Este campo refere-se as informações do cliente (empresa) e contato (nome) que a proposta está relacionada. Há uma descrição mais detalhada no tópico [Cadastro de Clientes](#Rotina de Cadastro de Cliente e Contato)|
|Agente| Campo para informar o nome do agente que está realizando a proposta. |
| Controle Interno| Colaborador que está responsável pela proposta. |
|Orçamentista| Colaborador que está responsável pela elaboração e envio da proposta. |

### Tela de Nova Proposta:
![Tela de Nova Proposta](img\tela_nova_proposta.png)


#### Rotina de Cadastro de Propostas

Para iniciar a rotina clique no botão "Nova Proposta" no canto superior direito da tela. Este botão abrirá uma tela com os principais campos da proposta descritos acima. Preencha os campos conforme avisos abaixo:

>Preencha o campo "Tipo" primeiramente, ele é responsavel por iniciar o gatilho de geração do número da proposta. O sistema possui numa lógica de reserva de números de proposta, para caso dois usuários simultâneos estiverem cadastrando proposta. O usuário tem 20 minutos para criar a proposta, caso contrário a tela é fechada e o número é liberado. Abaixo a relação de siglas:

>| TIPO     | Detalhe             |
| :------- | :------------------ |
| B        | Baixa               |
| F        | Força               |
| O        | Óleo                |
| P        | Pedestal            |
| S        | Seco                |
| AcessT   | Acessório Trafo     |
| ServT    | Serviço Trafo       |
| OutraT   | TRAFO               |
| Solar GD | UFV's para GD       |
| Solar GC | UFV's para GC       |
| SE       | Subestação          |
| PMT      | Painel Média Tensão |
| QE       | Quadro              |
| PE       | Painel              |
| EL       | Eletrocentro        |
| ServP    | Serviço Painel      |
| AcessP   | Acessório Painel    |
| OutraP   | Painel              |

>Preencha o campo "Obra" com o nome da obra que a proposta está relacionada, se houver.

>Clique no campo de "Cliente e Contato" e selecione o cliente e contato que a proposta está relacionada. Se não houver nenhum cliente ou contato cadastrado, clique no botão "Novo Cliente" ou "Novo Contato" para cadastrar. Mais detalhes [aqui](#Clientes).

>Preencha o campo "Agente" com o nome do agente que está realizando a proposta.

>Preencha o campo "Controle Interno" com o nome do colaborador que está responsável pela proposta.

> Preencha o campo "Orçamentista" com o nome do colaborador que está responsável pela elaboração e envio da proposta.

> Salve a proposta clicando no botão "Salvar".


### Rotina de Cadastro de Cliente e Contato

#### Cliente

#### Principais Campos e Parâmetros:

| Campo  | Descrição |
| ------ | --------- |
| Nome   | Nome da empresa. |
| CNPJ   | CNPJ da empresa. |
|Estado  | Estado da empresa. |
|Matriz  | Verdadeiro ou falso, indica se a empresa é matriz ou filial. |


#### Tela de Novo Cliente:
![Tela de Novo Cliente](img\tela_novo_cliente.png)

#### Rotina de Cadastro de Cliente
Para iniciar a rotina clique no botão "Novo Cliente" no canto superior direito da tela. Este botão abrirá uma tela com os principais campos do cliente descritos acima. Preencha os campos conforme avisos abaixo:

>Preencha o campo "Nome" com o nome da empresa. Escreva o nome completo da empresa, é por este campo que o sistema irá buscar o cliente e barrar quando o cliente já estiver cadastrado.

>Preencha o campo "CNPJ" com o CNPJ da empresa. Não é necessário colocar caracter especial, o sistema já irá tratar.

>Selecione o estado da empresa no campo "Estado".

> Marque o campo "Matriz" para indicar se a empresa é matriz ou filial.


#### Contato

#### Principais Campos e Parâmetros:

| Campo  | Descrição |
| ------ | --------- |
| Nome   | Nome do contato dentro da empresa, nome da pessoa física. |
| Email  | Email do contato. |
| Telefone| Telefone do contato. |

#### Tela de Novo Contato:
![Tela de Novo Contato](img\tela_novo_contato.png)

#### Rotina de Cadastro de Contato
Para iniciar a rotina clique no botão "Novo Contato" no canto superior direito da tela. Este botão abrirá uma tela com os principais campos do contato descritos acima. Preencha os campos conforme avisos abaixo:
> Preencha o campo "Nome" com o nome e sobrenome do contato. Não é necessário colocar o nome completo, apenas garanta que o nome esteja escrito corretamente.

> Preencha o campo "Email" com o email do contato. Escreva o email com o caracter especial "@".

> Preencha o campo "Telefone" com o número do telefone do contato. Não é necessário colocar caracter especial, o sistema já irá tratar.

!!! Atenção, só é possível cadastrar um contato se o cliente estiver selecionado, conforme abaixo:
![Cliente_Selecionado](img\tela_cliente_selecionado.png)

### Revisões

Há uma secção somente para tratar de revisões de propostas. Para acessar clique [aqui](revisao.md).


### Follows

Há uma secção somente para tratar de revisões de propostas. Para acessar clique [aqui](follow.md).




