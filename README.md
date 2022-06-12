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
- Tarefas (**##RF004**)
- Alunos (**RF005**)

Ao clicar em salvar, o sistema irá validar as informações para checar se nenhuma está vazia ou inválida.

Os **Professores** poderão agendar Eventos online que irão notificar todos os **Alunos** envolvidos no curso sobre quando o mesmo irá ocorrer.
Os **Professores** poderão adicionar todo tipo de arquivo digital a lista de materiais e os **Alunos** irão poder baixar os mesmos.

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

## RF004 Tarefas
**Coordenadores** e **Professores** podem adicionar tarefas em seus cursos. Uma terefa deve solicitar, obrigatoriamente, as seguintes informações:
- Nome
- Pontos
- Vencimento
- Forma de entrega
- Descrição

Ao salvar a nova tarefa a mesma é adicionada a lista de tarefas na tela de cursos (**RF002**)

Caso um **Aluno** esteja vinculado ao curso:
- O **Aluno** deverá receber notificações alertando o sobre a tarefa a nova tarefa.
- O **Aluno** deverá receber um lembrete no dia da entrega
- O **Aluno** deverá poder vizualizar em seu calendário a tarefa e clicar para ir a tela de tarefa.

Um **Coordenador** ou **Professor** também poderão clicar em uma tarefa na tela de cursos (**RF002**) para entrar na tela de vizualização da tarefa que deverá exibir nome e descrição da mesma, assim como a lista de alunos juntamente dos arquivos/textos enviados para a tarefa. Para cada aluno poderá ser adicionada uma nota a tarefa.

O **Aluno** ao entrar na tela de tarefas irá vizualizar o nome, descrição da tarefa juntamente do botão "enviar" que irá permitir a adição de um arquivo ou texto.

Caso o **Coordenador** ou **Professor** já tenham corrigido a tarefa, o **Aluno** irá receber uma notificação e a mesma será removida do calendário do mesmo. O **Aluno** também irá poder vizualizar na tela de tarefa a sua pontuação.

| Priridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Média | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Média | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Média | Aprovado | 1 | Ivo Aurélio da Silva

## RF005 Alunos
Após realizar matrícula (**RF006**), o **Aluno** terá acesso ao canvas do aluno que possui uma tela onde o mesmo pode editar as suas informações:
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

O **Aluno** também podera vizualizar os cursos do qual faz parte juntamente do seu calendário. 
O Calendário deverá exibir todas as tarefas de todos os cursos assim como feriados e eventos da instituição.


| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Baixa | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Baixa | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Baixa | Aprovado | 1 | Ivo Aurélio da Silva

## RF006 Realizar Matrícula
Um **usuário anonimo** ao escolher um curso no na tela de Buscar Cursos (**RF003**) poderá realizar sua matrícula no mesmo.


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

Após preencher os dados será enviado um e-mail contendo as informações para pagamento pagamento e um boleto (**RF008**) para pagamento.

Após o **Aluno** realizar o pagamento da primeira parcela irá receber um e-mail contendo o login e senha provisória para o mesmo poder prosseguir com o curso.

Em caso de falha no pagamento, o **Aluno** irá receber um e-mail avisando que o pagamento falhou e um novo boleto para pagamento. Caso o **Aluno** falhe em pagar o segundo boleto enviado, a matrícula será abortada.


| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Alta | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Alta | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Alta | Aprovado | 1 | Ivo Aurélio da Silva

## RF007 Aula Online
O sistema deverá permitir que um professor agende um **Evento** (**RF002**) contendo o nome e a data do mesmo. Na data do evento, o sistema deverá criar e disponibilizar uma sala online onde tanto **Professores** quanto **Alunos** consigam conectar e utilizar seus periféricos de vídeo, áudio e captura de áudio para se comunicar por vídeo e voz.

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
Alta | Alta | Elaborado | 1 | Felipe de Almeida, Stephanie Pinheiro Brazil
Alta | Alta | Revisado | 1 | Vinicius Rossoni Wagner, Tiago Ordesto Machado
Alta | Alta | Aprovado | 1 | Ivo Aurélio da Silva

## RF008 Emitir Boleto
O sistema deverá contar com uma 



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
**Linux**
- 16.04
- 20.04
- 21.04
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
