# Aplicativo de Justificativas

Bem-vindo à documentação do Aplicativo de Justificativas do TrackFlow. Esta ferramenta foi desenvolvida para registrar e acompanhar as justificativas referentes aos itens não concluídos nos mapas de produção anteriores.

## Conteúdo

* [Visão Geral](#visão-geral)
* [Modos de Operação](#modos-de-operação)
* [Funcionalidades](#funcionalidades)
* [Guia de Uso](#guia-de-uso)
* [Notificações](#notificações)

## Visão Geral

O Aplicativo de Justificativas permite que os programadores do PCP registrem as razões pelas quais determinados itens dos mapas de produção não foram concluídos conforme o planejado. A ferramenta oferece diferentes modos de visualização e edição, com acesso controlado por dia da semana.

## Modos de Operação

O aplicativo possui três modos distintos:

### Modo Semanal
* Disponível apenas às segundas-feiras
* Permite justificar itens não concluídos do mapa da semana anterior
* Todos os campos devem ser preenchidos para salvamento

### Modo Mensal
* Disponível apenas no início do mês
* Exibe todas as justificativas de acordo com a meta inicial
* Permite adicionar novas justificativas mensais
* Todos os campos devem ser preenchidos para salvamento

### Modo Histórico
* Disponível todos os dias da semana
* Exibe todas as justificativas registradas no sistema
* Permite filtrar por tipo (semanal/mensal)
* Possibilita a atualização de registros anteriores

## Funcionalidades

### Campos Editáveis

O aplicativo possui os seguintes campos editáveis:

• Setor
• Motivo
• Observação

### Seleção Dependente

O sistema implementa seleção dependente:

* O campo "Motivo" só é liberado após a seleção do "Setor"
* Os motivos disponíveis variam de acordo com o setor selecionado

### Validação de Campos

* Todos os campos editáveis devem ser preenchidos
* Todas as linhas devem ser completadas
* O sistema não permite salvamento parcial

## Guia de Uso

### Justificativas Semanais

1. Acesse o aplicativo na segunda-feira
2. Selecione o modo "Semanal"
3. Para cada item não concluído:
   * Selecione o setor responsável
   * Escolha o motivo apropriado (liberado após selecionar o setor)
   * Preencha a observação com detalhes relevantes
4. Clique em "Salvar" após preencher todos os campos

### Justificativas Mensais

1. Acesse o aplicativo no início do mês
2. Selecione o modo "Mensal"
3. Visualize as justificativas do mês corrente
4. Adicione novas justificativas conforme necessário
5. Preencha todos os campos (Setor, Motivo, Observação)
6. Clique em "Salvar" após preencher todos os campos

### Consulta de Histórico

1. Acesse o aplicativo em qualquer dia da semana
2. Selecione o modo "Histórico"
3. Escolha o tipo de justificativa (Semanal ou Mensal)
4. Visualize todas as justificativas registradas
5. Se necessário, selecione um registro para atualização
6. Edite os campos desejados
7. Clique em "Salvar" para atualizar o registro no banco de dados

## Notificações

O sistema envia notificações automáticas:

* Sempre que a tabela de justificativas semanal for atualizada
* Sempre que a tabela de justificativas mensal for atualizada
* As notificações são enviadas ao usuário responsável