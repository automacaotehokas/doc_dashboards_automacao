# Tabela-resumo

Bem-vindo à documentação da Tabela-resumo do TrackFlow. Esta ferramenta foi desenvolvida para consolidar informações de múltiplas tabelas em uma única interface, melhorando a usabilidade e oferecendo funcionalidades avançadas para o usuário.

## Conteúdo

* [Visão Geral](#visão-geral)
* [Atualizações](#atualizações)
* [Preferências do Usuário](#preferências-do-usuário)
* [Interface da Tabela](#interface-da-tabela)
* [Parâmetros](#parâmetros)
* [Comentários](#comentários)
* [Filtros](#filtros)

## Visão Geral

A Tabela-resumo substitui a visualização de 4 tabelas separadas, consolidando todas as informações em uma única interface interativa. Além da consolidação, o aplicativo oferece recursos avançados de filtros, organização e personalização que não estavam disponíveis anteriormente.

## Atualizações

Os dados da tabela são atualizados automaticamente três vezes ao dia:
• 07:00
• 12:00
• 17:00

## Preferências do Usuário

O sistema salva automaticamente as preferências configuradas pelo usuário:

• Colunas visíveis
• Ordenação das colunas
• Posicionamento das colunas
• Parâmetros selecionados (quando aplicável)

As preferências são mantidas mesmo após o usuário sair do aplicativo, garantindo uma experiência personalizada em cada acesso.

## Interface da Tabela

### Navbar

A barra de navegação superior contém:

#### Card de Valor Total
• Exibe a soma da coluna "valor_total_item" 
• Mostra a contagem de linhas visíveis
• Atualiza dinamicamente conforme os filtros aplicados

#### Botão de Parâmetros
Abre o menu de configuração de parâmetros (detalhes na seção [Parâmetros](#parâmetros))

#### Botão Exportar Excel
• Permite exportar os dados visíveis para um arquivo Excel
• Exporta as linhas conforme os filtros aplicados

#### Botão Configurar Colunas
• Exibe um painel com checkbox para cada coluna disponível
• Permite selecionar/deselecionar colunas individualmente
• Inclui botões para selecionar/deselecionar todas as colunas
• Oferece botão de "Reordenação Padrão" para restaurar a ordem original das colunas

#### Botão Limpar Filtros
Remove todos os filtros aplicados na tabela

#### Botão do Usuário
• Exibe o primeiro nome do usuário logado
• Permite deslogar da conta quando clicado

### Botão Carregar Comentários
Localizado abaixo da navbar, este botão carrega as colunas de comentários para a tabela

## Parâmetros

O menu de parâmetros possui as seguintes seções:

### Geral
• **Visão Geral**: Configura a tabela com as colunas essenciais: ID, Divisão, Tipo Produto, Gestor, OV, OP, Cliente, Obra, Desc Produto, Qtde, Etapa, Dt Etapa, Status Etapa, Dt Operacional, Dt Contratual, Dt Repac
• Este parâmetro não é salvo nas preferências do usuário

### GC (Gestão de Contratos)
• **Meus Projetos**: Filtra para mostrar apenas projetos do gestor logado
• **Status Projeto**: Permite selecionar entre projetos Abertos, Fechados ou Suspensos
• **Reunião**: Filtra projetos por tipo de produto (BxBx, Seco, Óleo, Eng Ele, Eng Mec, Service)
• Os parâmetros "Meus Projetos" e "Status Projeto" podem ser salvos nas preferências do usuário
• O parâmetro "Reunião" não é salvo nas preferências

## Comentários

### Funcionalidade
• Acessível através do botão "Carregar Comentários"
• Permite aos gestores documentar informações de reuniões

### Colunas de Comentários
• Etapa
• Setor Responsável
• Dt Etapa Alinhada
• Comentário

### Regras de Salvamento
• Apenas gestores da Gestão de Contratos podem salvar comentários
• Para salvar Etapa, Setor e Data, todas as três colunas devem estar preenchidas
• O Comentário pode ser salvo independentemente
• É possível salvar as quatro colunas simultaneamente
• Campos previamente preenchidos podem ser apagados deixando-os vazios

## Filtros

• Todas as colunas possuem filtros
• Filtros textuais: ordem alfabética, crescente ou decrescente
• Filtros de data: seleção por ano, mês e dia
• Os filtros afetam a exibição de dados e o cálculo do Valor Total