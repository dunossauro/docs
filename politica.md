# Política de segurança da informação
      Versão 0.1
      Baseado em:
               ISO27002
               Documentação Bacula

## 1. Introdução

A segurança é um dos assuntos mais importantes dentre as preocupações de qualquer empresa.
Nesse documento apresentaremos um conjunto de instruções e procedimentos para normatizar e melhorar nossa visão e atuação em segurança

## 1.1 Sobre este documento
O presente documento estabelece uma política de:

   - Gerenciamento de senhas;
   - Cópias de segurança (backup) e restauração de arquivos digitais armazenados no parque tecnológico desta empresa;
   - Controle de acesso a contas administrativas da empresa.

Os donos dos dados deverão ter ciência dos tempos de retenção aqui estabelecidos e para cada tipo de informação e os administradores/operadores de backup deverão zelar pelo cumprimento das diretrizes aqui estabelecidas.

## 2. Política de senhas

### 2.1 Tamanho mínimo da senha e Complexidade da senha:

Considere até 3 destas 4 regras de formação da senha:

   - Conter pelo menos uma letra minúscula;
   - Conter pelo menos uma letra maiúscula;
   - Conter números (0 a 9);
   - Conter símbolos incluindo: ! @ # $ % ^ & * - _ + = [ ] { } | \\ : ‘ , . ? / \` ~ “ < > ( ) ;
   - Tamanho mínimo de 8 caracteres;
   - Não é permitido usar partes do nome;

### 2.2 Troca periódica da senha:

As senhas devem ser alteradas a senha a cada 180 dias

### 2.3 Não repetição de senhas:

Não é permitido utilizar as 5 últimas senhas cadastradas

## 3. Backup e Restauração de Arquivos

### 3.1. Considerações iniciais

O serviço de backup deve ser orientado para a restauração das informações no menor tempo possível, principalmente havendo indisponibilidade de serviços que dependam da operação de restore.

Este documento deverá ter conhecimento e anuência da Diretoria.

_______pessoa0_______ e _______pessoa1_______ serão responsáveis pela administração dos backups e restaurações dos bancos de dados e máquinas virtuais. Tendo compromisso pleno e sendo notificados pela responsabilidade à ser exercida.

### 3.2. Orientações Gerais:

Cabem aos administradores prever a realização de testes periódicos de restauração, no intuito de averiguar os processos de backup e estabelecer melhorias.

A administração dos backups também deve ser orientada para que seus trabalhos respeitem as janelas para execução, inclusive realizando previsão para a ampliação da capacidade dos dispositivos envolvidos no armazenamento.

As mídias (ou dispositivos de armazenamento) deverão ser, preferencialmente, armazenadas em localidade diversa da origem dos dados (backup off-site).

As mídias defeituosas ou inservíveis serão encaminhadas para picotamento, incineração, procedimentos de sobrescrita de dados remanescentes (disco rígido) ou outro procedimento que impossibilite a recuperação dos dados por terceiros.

As solicitações de restauração de arquivos deverão ser abertas formalmente através de ferramentas de abertura de chamados e / ou formulário que deverá conter os nomes dos arquivos e pastas que deverão ser recuperados e, principalmente, a data do aquivo que se pretende ter acesso.

### 3.3. Estratégia Geral Backup:

De acordo com a natureza dos dados trazemos a seguinte classificação:

    Bancos de Dados;
    Máquinas Virtuais (imagem).

Por padrão será adotada o seguinte esquema de realização de backups para os bancos de dados:

1. Backups incrementais locais (denominados diários) todos os dias da semana, realizados a partir das 00:00h., seguidos de outro backup realizado a partir das 12:00h., com uma semana de retenção;
2. Backups incrementais na nuvem (denominados diários) todos os dias da semana, realizados a partir das 03:00h., com uma semana de retenção;
4. Backups transicionais (denominados semanais) em todas as quartas-feiras as 06:00h., com retenção até o próximo backup completo.
3. Backups completos (full – denominados quinzenais) nas primeiras e terceiras segundas-feiras do mês, realizados a partir das __ :00h., com um mês de retenção e realizado por um humano.

O backup das máquinas virtuais como imagem (adequado para fins de disaster recovery – ou seja: restauração da máquina como um todo), será feito apenas na seguinte periodicidade:

Backups completos (full – denominados mensais) na primeira sexta-feira do mês, realizados a partir das __ :00h., com um ano de retenção e realizados por um humano;

### 3.4. Armazenamento de backups:

Todos os backups realizados por autômatos devem ser armazenados em discos rígidos.

Os backups completos e realizados por humanos, devem ser armazenados em ___ , com a finalidade de fácil acesso e recuperação.


## 4. Política de controle de acesso ao servidor

O servidor deve conter no mínimo três usuários representativos:

   - Administrador: A conta administrativa deve ser restrita ao mantenedor do sistema (_____pessoa_____), que será responsável pela instalação de software e atualizações dos mesmos;
   - Usuários: A conta de usuários deve ser utilizada por todos que fazem uso de recursos do sistema, mas sem permissão de instalação ou deleção de programas e restrito a tarefas administrativas de aplicações;
   - Convidado: O usuário convidado, pode ter acesso somente a funções comuns do sistema e pode ter acesso a alguns diretórios previamente configurados a sua necessidade.
