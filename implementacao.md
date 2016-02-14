# Implementação das rotinas de Backup do banco de dados
> v: 1.0

## Sobre este documento

Este documento constata as implementações e rotinas de backup feitas por Eduardo F. Mendes aos sistemas de informação da empresa Quality Digital, supervisionadas por Rogério Farah.

## Sobre as rotinas

As backup consistem em três rotinas:

   1. Backup incremental, local, realizado a cada 12 horas (06:00h e 18:00h) com uma semana de retenção no diretório Z:/bkp. Que só pode ser modificado pelo usuário ServerAdmin
   2. Backup total, armazenado no Dropbox, realizado diariamente as 00:00, com sete dias de retenção.
   3. Backup total, local, realizado a cada 24 horas (03:00h) com uma semana de retenção no diretório Z:/bkp. Que só pode ser modificado pelo usuário ServerAdmin

### Rotinas a serem implementadas

Embora as rotinas implementadas se mostrem eficientes, uma rotina de armazenamento *out-off-box* deve ser efetuada por um funcionário responsável, a função, que deverá, como a política recomenda, persistir os dados em uma mídia de armaznamento externa.

## Sobre a implementação

As rotinas foram implementadas usando o SQL Backup Master (Free Version) no Windows Server. O armazenamento local foi executado no diretório *Z:/bkp* em conjunto ao armazenamento em *cloud*, Dropbox, usando a API fornecida pelo SQL Backup Master.

## Plano de continuidade

Caso ocorra um crescimento constante de dados, de uma maneira que não seja possível armazenar os dados em *cloud*, a aquisição de um plano privado no Dropbox pode ser adquirida. Também, como alternativa, pode ser adquirida a versão *non-free* do SQL Backup Master para um armazenamento guiado pela API do Google Drive.

## Gestão de riscos e Recuperação de desastres

Essa seção é destinada a riscos encontrados na implementação e a recuperação dos mesmos.

1. A porta de acesso aos dados do banco de dados é a *default*. Caso ocorram futuros problemas, as modificações em todas as aplicações que fazem uso do servidor devem ser alteradas
2. As políticas de senhas devem ser aplicadas no tempo previsto pela política de segurança, como prevenção a futuros desastres.
3. Em caso de perda de dados, os backups deve ser restaurados no tempo mínimo contido na cláusula de contrato do cliente.
4. Os backups devem ser revisados após o seu armazenamento *out-off-box* e deve estar sempre disponível para recuperação.


## Considerações finais

Este documento, como conta na primeira seção, foi escrito por Eduardo F. Mendes e deve ser analisado por Rogério Farah. Quem dará as diretrizes de aprovação.
