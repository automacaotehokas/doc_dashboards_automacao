# Mapa de Produção

Bem-vindo à documentação do Mapa de Produção do TrackFlow. Esta ferramenta foi desenvolvida para programar e acompanhar o cronograma de expedição dos produtos, permitindo uma visualização clara do planejamento de produção.

## Conteúdo

* [Visão Geral](#visão-geral)
* [Funcionalidades](#funcionalidades)
* [Guia de Uso](#guia-de-uso)
* [Solução de Problemas](#solução-de-problemas)

## Visão Geral

O Mapa de Produção é uma tabela interativa que permite aferir e gerenciar as datas de expedição dos itens em programação. Esta ferramenta é essencial para o planejamento semanal da produção e para garantir que os prazos sejam cumpridos adequadamente.

## Funcionalidades

### Carregamento Automático de Dados

O sistema carrega automaticamente os dados JSON atualizados semanalmente ao iniciar a tabela.

### Salvamento e Correção

* **Salvamento Semanal**: O mapa deve ser salvo às sextas-feiras
* **Correção de Mapa Anterior**: Após o salvamento, o botão "Corrigir Mapa Anterior" é habilitado
  * Esta função carrega os dados do último mapa salvo no banco
  * Exemplo: Na semana 14 (S14), após salvar, o botão carregará os dados do mapa da S14 para correção

### Sistema de Avisos Visuais

A coluna **Dt Expedição** possui dois indicadores visuais:

1. **Indicador <span style="color:red">Vermelho</span>**: 

    * Aparece para datas de expedição iguais ou anteriores à data atual.
    * Impede o salvamento da linha

2. **Indicador <span style="color:orange">Laranja</span>**:

    * Aparece para datas de expedição maiores que a data do último mapa.
    * Permite o salvamento, funcionando apenas como alerta

3. **Há um parâmetro na toolbar que permite filtrar as linhas com o indicador que o usuário deseja.**

### Importação de Dados

A tabela permite importar dados de arquivos Excel:

1. **O botão "Importar Dados" é habilitado na toolbar após o carregamento da tabela**

2. **O arquivo Excel deve conter exatamente as seguintes colunas como está escrito:**

    * **OP**
    * **OV**
    * **Dt Expedição**
    * **Justificativa**

> **Nota**: O arquivo "excel_teste_random.xlsx" está disponível para download <a href="../assets/files/excel_teste_random.xlsx" style="color:blue;font-weight:bold;" download>aqui</a> como modelo para importação.

### Recursos da Tabela
1. **Filtros Personalizáveis**
    


## Guia de Uso

1. Na página inicial, clique no card **Gerar Mapa**
2. Aguarde o carregamento dos dados semanais
3. Se necessário, utilize o botão **Importar Dados** para carregar informações de um arquivo Excel
4. Ajuste as datas de expedição, observando os indicadores visuais
5. Salve o mapa (preferencialmente às sextas-feiras)
6. Para correções, utilize o botão **Corrigir Mapa Anterior**

## Solução de Problemas

### Problemas na Importação de Dados
* Verifique se o arquivo Excel contém todas as colunas necessárias: OP, OV, Dt Expedição e Justificativa
* Certifique-se de que o arquivo está no formato correto

### Linha não Pode Ser Salva
* Verifique se há indicador vermelho na coluna de data de expedição
* Ajuste a data para um valor futuro (posterior à data atual)