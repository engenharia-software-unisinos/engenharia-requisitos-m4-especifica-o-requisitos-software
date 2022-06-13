# Instituição ABC - Especificação de Requisitos

# 1. Especificação de Requisitos Funcionais

| Nome do Projeto | Responsável | Descrição | Data e Versão |
| :--- | :---: | :---: | :---: |
**Instituição ABC - Requisitos Funcionais** | Tiago Ordesto Machado, Felipe Rodrigues de Almeida, Stephanie Pinheiro Brazil, Vinicius Rossoni Wagner e Ivo Aurélio da Silva | Criação do documento | 11/06/2022

## RF001 - Tipos de usuário

O sistema deverá disponibilizar uma interface para possibilitar a manutenção dos usuários do sistema. O sistema irá autenticar e autorizar os usuários. A autenticação deverá ocorrer mediante senha pré cadastrada na interface de manutenção de usuário e a autorização através da validação de perfil. Serão disponibilizados os seguintes perfis:
- Aluno 
- Professor
- Coordenador
- Funcionário 

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Alta | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Alta | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Alta | Aprovado | 1 | Ivo Aurélio da Silva

## RF002 - Cursos
**Funcionários** e **Coordenadores** podem cadastrar um um curso ou a edição de um existente. 

Para o cadastro de um curso, serão necessárias, as seguintes informações:
- Nome*
- Professor responsável*
- Turno*
- Decrição

_As informações com '*' são obrigatórias_

Após inserir as informações o usuário terá a opção de salvar o novo curso ou cancelar a operação. Caso salve, será redirecionado para a tela do curso recém criado.

Na tela do curso, existirá um botão que permitirá a edição dos seguintes dados:
- Nome
- Professor responsável
- Decrição
- Turno 
- Materiais (Arquivos que disponibilizados para o **Aluno**)
- Eventos (Aulas marcadas pelo **Professor**)
- Tarefas 
- Alunos 

Ao clicar em salvar, o sistema irá validar as informações para checar se nenhuma está vazia ou inválida.

**Alunos** poderão somente vizualizar as informações do curso, baixar materiais e interagir com as tarefas para ler e realizar entregas.

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Média | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Média | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Média | Aprovado | 1 | Ivo Aurélio da Silva

## RF003 - Buscar curso

Um usuário anonimo ou um **aluno** poderão buscar os **cursos** existentes dentro do sistema utilizando os seguintes critérios:
- Busca por palavra chave
- Busca por categoria de curso
- Busca por data do ínicio do curso

Se nenhuma informação for providenciada na busca, a mesma deverá retornar todos os cursos disponíveis páginados.

#### Em caso de sucesso:
Exibir a lista de cursos com os critérios de busca aplicados
#### Em caso de falha:
Exibir uma notificação na tela informando que houve uma falha em buscar os cursos

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Baixa | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Baixa | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Baixa | Aprovado | 1 | Ivo Aurélio da Silva

## RF004 Cadastrar Tarefa no curso
**Coordenadores** e **Professores** podem adicionar tarefas em seus cursos. Uma terefa deve solicitar, obrigatoriamente, as seguintes informações:
- Nome
- Pontos
- Vencimento
- Materiais
- Forma de entrega
- Descrição

Ao salvar a nova tarefa a mesma é adicionada a lista de tarefas na tela de cursos

Caso um **Aluno** esteja vinculado ao curso:
- O **Aluno** deverá receber notificações alertando o sobre a tarefa a nova tarefa.
- O **Aluno** deverá receber um lembrete no dia da entrega
- O **Aluno** deverá poder vizualizar em seu calendário a tarefa e clicar para ir a tela de tarefa.

Um **Coordenador** ou **Professor** também poderão clicar em uma tarefa na tela de cursos para entrar na tela de vizualização da tarefa que deverá exibir nome e descrição da mesma, assim como a lista de alunos juntamente dos arquivos/textos enviados para a tarefa. Para cada aluno poderá ser adicionada uma nota a tarefa.

| Priridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Média | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Média | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Média | Aprovado | 1 | Ivo Aurélio da Silva

## RF005 Entregar Tarefa
**Alunos** podem fazer upload de um arquivo ou adicionar um texto para realizar a entrega de uma Tarefa.

Ao ser entregue, deverá ser notificado para o **Professor** responsável via e-mail e sistema que a tarefa do **Aluno** foi concluída com sucesso e a mesma removida do seu calendário.


| Priridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Média | Baixa | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Média | Baixa | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Média | Baixa | Aprovado | 1 | Ivo Aurélio da Silva

## RF006 Avaliar Tarefa
O **Coordenador** ou **Professor** de um curso deverão poder avaliar uma tarefa atribuindo uma pontuação a mesma. O **Aluno** deverá ser notificado que a sua tarefa foi corrigida.

| Priridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Média | Baixa | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Média | Baixa | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Média | Baixa | Aprovado | 1 | Ivo Aurélio da Silva

## RF007 Editar Perfil Aluno
Após realizar matrícula, o **Aluno** terá acesso ao canvas do aluno que possui uma tela onde o mesmo pode editar as suas informações:
**Contato **
- Nome
- Nome de Exibição
- E-mail
- Idioma
- Celular
**Notificações** 
_O **Aluno** poderá ativar ou desativar as seguintes notificações_
- Notificar tarefa criada
- Notificar tarefa alterada
- Notificar tarefa pontuada
- Notificar curso criado
- Notificar curso alterado
- Notificar evento de curso criado
- Notificar material adicionado a curso

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Baixa | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Baixa | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Baixa | Aprovado | 1 | Ivo Aurélio da Silva

## RF008 Realizar Matrícula
Um **usuário anonimo** ao escolher um curso no na tela de Buscar Cursos poderá realizar sua matrícula no mesmo.

Para realizar a matrícula sera solicitada, de forma obrigatória, as seguintes informações:
- Nome Completo
- Idade
- RG
- CPF
- E-Mail
- Celular
- Motivo para a escolha do curso
- Número de parcelas

Também será exibido para o **Aluno** informações para o aluno, datas de aulas, professores e valor do curso.

Os dados irão ser válidados quando o **Aluno** clicar no botão **Prosseguir com a Matrícula**, que irá direcionar o **Aluno** para uma tela que irá solicitar que o mesmo cheque o e-mail para dar prosseguimento.

Após preencher os dados será enviado um e-mail contendo as informações para pagamento pagamento e um boleto para pagamento.

Após o **Aluno** realizar o pagamento da primeira parcela irá receber um e-mail contendo o login e senha provisória para o mesmo poder prosseguir com o curso.

Em caso de falha no pagamento, o **Aluno** irá receber um e-mail avisando que o pagamento falhou e um novo boleto para pagamento. Caso o **Aluno** falhe em pagar o segundo boleto enviado, a matrícula será abortada.


| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Alta | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Alta | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Alta | Aprovado | 1 | Ivo Aurélio da Silva

## RF009 Aula Online
O sistema deverá permitir que um professor agende um **Evento** contendo o nome e a data do mesmo. Na data do evento, o sistema deverá criar e disponibilizar uma sala online onde tanto **Professores** quanto **Alunos** consigam conectar e utilizar seus periféricos de vídeo, áudio e captura de áudio para se comunicar por vídeo e voz.

A funcionalidade de Aula Online deverá suportar as seguintes ações para todos os usuários:
- Mutar ou desmutar a si mesmo
- Ligar/Desligar vídeo
- Compartilhar/Descompartilhar tela

A funcionalidade de Aula Online deverá suportar as seguintes ações para os **Professores**:
- Mutar/Desmutar **Aluno** específico
- Mutar/Desmutar todos os **Alunos**
- Criar salas secundárias para dividir os **Alunos** em grupos
- Descriar salas secundárias e trazer todos as **Alunos** de volta a sala original
- Criar enquetes e exibir os resultados da mesma
- Desenhar na tela durante o compartilhamento de tela

Antes de um usuário conectar, deverá ser perguntado ao usuário se os periféricos selecionados estão corretos.

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Média | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Média | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Média | Aprovado | 1 | Ivo Aurélio da Silva

## RF010 Emição de Boleto
O sistema deverá contar com um sistema de pagamento que permita a emissão de boletos de forma manual pelos **Funcionários** ou automática para os **Alunos**.

A funcionalidade de emissão de boleto poderá acontecer nas seguintes situações:
- Quando o **Aluno** realizar a matrícula, devera ser emitido de forma automática uma cobrança com o custo do curso para o e-mail de destino.
- Quando o **Funcionário** enviar uma cobrança de forma manual para um **Aluno**.
- Quando o método de pagamento do **Aluno** for débito automático, será enviada uma cobrança de forma automática.

Quando o **Aluno** realizar o pagamento, o sistema deverá atualizar a cobrança do boleto paga pago.

Caso o boleto não seja pago na data ou o pagamento falhe, deverá ser reenviado o boleto da cobrança com o custo da multa definida pelo **Funcionário** para o **Aluno** via e-mail. Caso o boleto falhe em ser pago novamente a mátricula irá ser cancelada ou o curso irá ser automáticamente trancado para o **Aluno**.

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Média | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Média | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Média | Aprovado | 1 | Ivo Aurélio da Silva

## RF011 Emitir carta de cobrança para clientes inadiplemntes 
Para todo **Aluno** que esteja inadiplente, deverá ser possível a emissão da carta de cobrança através do sistema. O resultado da emissão será a carta impressa, que será posteriormente despachada por correrios ou outro agende de entrega.

Os critérios para definir se um cliente é ou não inadiplente devem estar cadastrados no sistema utilizando regras de negócio específicas. Nem todo cliente com pagamento em atraso será considerado inadimplente, pos deverá ser levado em consideração o score de crédito do cliente, sua renda mensal, patrimônio etc.

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Média | Média | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Média | Média | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Média | Média | Aprovado | 1 | Ivo Aurélio da Silva

## RF012 Fazer upload de material
O **Coordenador** ou **Professor** poderá fazer upload de materiais de qualquer tipo para um curso. O mesmo irá ser listado nos materiais disponíveis de um curso.

O **Aluno** deverá ser notificado sempre que um material relativo a um curso do qual é membro for adicionado.

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Média | Média | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Média | Média | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Média | Média | Aprovado | 1 | Ivo Aurélio da Silva

## RF013 Agendar eventos
O **Coordenador** ou **Professor** podem agendar eventos dentro de seus cursos.

O evento irá solicitar, obrigatóriamente, as seguintes informações:
- Nome
- Data
- Tipo (Presencial, Remoto)
- Local (se presencial, endereço; se remoto, link da vídeo chamada)
- Descrição

Quando o evento for criado:
- Deverá aparecer no calendário de todos os alunos do curso.
- Deverá notificar todos os alunos do curso.


| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Média | Média | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Média | Média | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Média | Média | Aprovado | 1 | Ivo Aurélio da Silva

## RF014 Gerar relatórios
**Funcionários** podem gerar relatórios para vizualizar dados sobre o sistema
- Númmero de alunos por curso
- Número de professores por curso
- Número de usuários utilizando o sistema agora
- Número de alunos inadimplentes
- Número de matrículas por período
- Comparação quantidade de alunos por mês, dia, ou ano

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Baixa | Média | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Baixa | Média | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Baixa | Média | Aprovado | 1 | Ivo Aurélio da Silva

## RF015 Monitorar saúde
**Funcionários** deverão poder monitorar o estado de saúde de todos os usuários e a sua localização dentro da instituição via sistema para conseguir responder melhor a crises em função da pandemia.

Ao identificar uma pessoa contaminada, deverá ser emitido um alerta aos responsáveis pelo monitoramento para isolar todos os que estiveram próximos da pessoa. Todas as pessoas que tiveram contato deverão receber um alerta via e-mail solicitando teste e informando afastamento temporário até o resultado do teste surgir.

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Alta | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Alta | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Alta | Aprovado | 1 | Ivo Aurélio da Silva


# 2. Especificação de Requisitos Não Funcionais

| Nome do Projeto | Responsável | Descrição | Data e Versão |
| :--- | :---: | :---: | :---: |
**Instituição ABC - Requisitos Não Funcionais** | Tiago Ordesto Machado, Felipe Rodrigues de Almeida, Stephanie Pinheiro Brazil, Vinicius Rossoni Wagner e Ivo Aurélio da Silva | Criação do documento | 11/06/2022

## Usabilidade
## RNF001 - Design Responsivo nas interfaces gráficas

O sistema da Instituição ABC será construído para rodar em ambiente web. Deverá possuir um design responsivo (https://en.wikipedia.org/wiki/Responsive_web_design).

A interface do sistema deverá se comportar adequadamente independente do front-end que será utilizado para acesso - Browser, Smartphone ou Tablet.

Este requisito será validado utilizando-se de testes de usabilidade. 

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Baixa | Baixa | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Baixa | Baixa | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Baixa | Baixa | Aprovado | 1 | Ivo Aurélio da Silva

## RNF002 - Velocidade de Uso de Interface
O sistema da Instituição ABC deverá ter um tempo de respostá de menos de 0.200ms para a tela ficar interágivel. Elementos que necessitem de mais tempo para carregarem deverão ser carregados em segundo plano.

Este requisito será validado utilizando-se de testes de usabilidade e usando a ferramenta do Google Developers, Page Speed insights (https://pagespeed.web.dev/) com o objetivo de atender o modelo de usabilidade da ISO/IEC 9126.

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Baixa | Baixa | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Baixa | Baixa | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Baixa | Baixa | Aprovado | 1 | Ivo Aurélio da Silva

## RNF003 - Facilidade de Uso

O sistema da Instituição ABC deverá ser de fácil utilização, todas as tarefas devem ser simples e intuitivas de serem concluídas por todos os usuários no primeiro uso.

Este requisito será validado utilizando-se de testes de usabilidade com o objetivo de atender o modelo de usabilidade da ISO/IEC 9126.

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Média | Baixa | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Média | Baixa | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Média | Baixa | Aprovado | 1 | Ivo Aurélio da Silva

## RNF004 - Compatibilidade com sistemas operacionais Windows, Mac e Linux
O sistema deverá suportar as seguintes versões de cada sistema operacional:
**Windows**
- XP
- Vista 7
- Vista 8
- Windows 10
- Windows 11
- 
**Linux**
- 16.04
- 20.04
- 21.04
- 
**Mac**
- Monteray
- Big Sur
- Catalina
- High Sierra
- Sierra
- El Captain
- Yosemite

Este requisito será atendido por uma série de testes de usabilidade e deverá garantir que todos os testes passem em todos os sistemas para garantir a retrocompatibilidade com os sistemas operacionais.

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Alta | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Alta | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Alta | Aprovado | 1 | Ivo Aurélio da Silva

## Confiabilidade
## RNF005 - Tempo de Recuperação
O sistema da Instituição ABC deverá possuir monitoramento da saúde do sistema para identificar quando o sistema está indisponível ou com problemas em suas dependências. 

Ao identificar com sucesso um problema, o sistema deverá ser reiniciado.

Este requisito será validado utilizando-se de testes de carga e testes de integração que irão forçar situações de exeção colocando o servidor em estresse com o objetivo de atender o modelo de confiabilidade da ISO/IEC 9126.

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Alta | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Alta | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Alta | Aprovado | 1 | Ivo Aurélio da Silva

## RNF006 - Tolerância a Falhas
O sistema da Instituição ABC deverá ser desenvolvido sempre pensando que suas dependências podem apresentar falhas e prosseguir o funcionamento normal ou restrito para as funcionalidades afetadas.

Uma funcionalidade restringida deverá exibir um aviso informando que o sistema está com alguma instabilidade não permitindo o uso da mesma.

Este requisito será validado utilizando-se de testes de usuário e testes de integração que irão forçar situações de exeção colocando o servidor em estresse com o objetivo de atender o modelo de confiabilidade da ISO/IEC 9126.

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Baixa | Alta | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Baixa | Alta | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Baixa | Alta | Aprovado | 1 | Ivo Aurélio da Silva

## RNF007 Disponibilidade Esperada
O sistema por ter alunos que irão ficar no sistema assistindo aulas, buscando materiais e realizando tarefas por várias horas, deverá possuir uma disponibilidade de 99.0%.

Este requisito será validado mensalmente e mudanças na infraestrutura podem ser aplicadas para manter a métrica em 99% ou acima.

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Alta | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Alta | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Alta | Aprovado | 1 | Ivo Aurélio da Silva

## Segurança
## RNF008 Autenticação e Autorização
Todas as partes do sistema expostas, que exijam controle de acesso, poderão ser acessadas por usuários cadastrados no sistema web utilizando-se de OAuth2.

O sistema deverá permitir login via conta Facebook, Google ou Apple.

O sistema não deverá permitir cache de senha, salvamento de senha ou qualquer outro recurso do tipo.
Deverá haver uma política de segurança que assegure que, a cada mês, a senha de cada um dos usuários citados expire e precise ser renovada, e que tenha critérios de complexidade para fortalecer as senhas.

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Média | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Média | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Média | Aprovado | 1 | Ivo Aurélio da Silva

## RNF009 Bloqueio de IPs fora do Brasil
Por os usuários serem brasileiros, a exceção de **alunos**, **professores**, **coordenadores** e **funcionários** fora do brasil, usuários não cadastrados fora do brasil devem ter acesso ao sistema bloqueado.

Este requisito será validado utilizando-se de testes de segurança de simulando acesso de usuários anonimos de fora do Brasil para antender o módulo de segurança da ISO/IEC 9126.

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Baixa | Média | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Baixa | Média | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Baixa | Média | Aprovado | 1 | Ivo Aurélio da Silva

## RNF010 Identificação e bloqueio de Ataques de Negação (Denial of Service) individuais
O sistema deve conseguir identificar e bloquear ips que tenham como alvo vítimas individuais, como por exemplo, deliberadamente colocar uma senha errada várias vezes para bloquear o acesso de uma vítima.

Este requisito será validado utilizando-se de testes de segurancá simulando ataques para antender o módulo de segurança da ISO/IEC 9126.

## Restrições
## RNF011 Restrição de linguagem de programação
O sistema deverá ser desenvolvindo utilizando-se das seguintes tecnologias:
- Framework Vue.js para o front-end utilizando-se de JavaScript
- Framework .NET 6 para o back-end utilizando-se de C#

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Baixa | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Baixa | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Baixa | Aprovado | 1 | Ivo Aurélio da Silva

## RNF012 Restrição de banco de dados
O sistema deverá ser desenvolvindo utilizando o banco de dados SQL Server providenciado pela Azure. 

Para os seguintes ambientes de desenvolvimento serão utilizados os seguintes níveis de bancos:
| Ambiente | Nível |
| :--- | :---: |
Desenvolvimento | B1
Homologação | S1
Produção | P3V2


| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Baixa | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Baixa | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Baixa | Aprovado | 1 | Ivo Aurélio da Silva

## RNF013 Restrições de padrões de desenvolvimento
O sistema deverá ser desenvolvindo atendendo os seguintes padrões: 
- CQS - Command Query Separation (https://www.wellingtonjhn.com/posts/cqs---command-query-separation/) tanto no front-end quanto no back-end
- Atomic Design (https://evertonstrack.com.br/atomic-design/) para o desenvolvimento de componentes no front-end.
- Padrão Estrangulamento (https://medium.com/codigorefinado/strangle-design-pattern-o-padr%C3%A3o-estrangulamento-f93c05e9061d) para a utilização de funcionalidades do sistema legado enquanto novas estão sendo desenvolvidas.


| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Baixa | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Baixa | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Baixa | Aprovado | 1 | Ivo Aurélio da Silva

## RNF014 Restrição de provedor de nuvem Azure
O sistema deverá ser desenvolvido utilizando somente serviços disponibilizados pela Microsoft Azure.

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Baixa | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Baixa | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Baixa | Aprovado | 1 | Ivo Aurélio da Silva

## RNF015 Restrição de sistema legado
O sistema deverá suportar todas as funcionalidades que o sistema legado suportava.
Todos os dados de alunos, professores, coordenadores e funcionários existentes deverão ser migrados para o banco de dados SQL Server na Azure.

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Baixa | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Baixa | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Baixa | Aprovado | 1 | Ivo Aurélio da Silva
