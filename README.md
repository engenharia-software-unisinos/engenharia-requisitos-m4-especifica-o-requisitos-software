# Instituição ABC - Especificação de Requisitos

| Nome do Projeto | Responsável | Data e Versão |
| :--- | :---: | :---: |
**Instituição ABC** | Tiago Ordesto Machado, Felipe Rodrigues de Almeida, Stephanie Pinheiro Brazil, Vinicius Rossoni Wagner e Ivo Aurélio da Silva | **Data Versão:** 11/06/2022

## RF001 - Tipos de usuário

O sistema deverá disponibilizar uma interface para possibilitar a manutenção dos usuários do sistema. O sistema irá autenticar e autorizar os usuários. A autenticação deverá ocorrer mediante senha pré cadastrada na interface de manutenção de usuário e a autorização através da validação de perfil. Serão disponibilizados os seguintes perfis:
- Aluno 
- Professor
- Coordenador
- Funcionário 

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Alta | Aprovado | 1 | Felipe de Almeida

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
- Tarefas (**##RF004**)
- Alunos (**RF005**)

Ao clicar em salvar, o sistema irá validar as informações para checar se nenhuma está vazia ou inválida.

**Alunos** poderão somente vizualizar as informações do curso, baixar materiais e interagir com as tarefas para ler e realizar entregas.

| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Médioa | Aprovado | 1 | Felipe de Almeida

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
Alta | Baixa | Aprovado | 1 | Felipe de Almeida

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
Alta | Média | Aprovado | 1 | Felipe de Almeida

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
- Notificar material adicionado a curso

O **Aluno** também podera vizualizar os cursos do qual faz parte juntamente do seu calendário. 
O Calendário deverá exibir todas as tarefas de todos os cursos assim como feriados e eventos da instituição.


| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Baixa | Aprovado | 1 | Felipe de Almeida

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

Após preencher os dados será enviado um e-mail contendo as informações para pagamento pagamento e um boleto para pagamento.

Após o **Aluno** realizar o pagamento da primeira parcela irá receber um e-mail contendo o login e senha provisória para o mesmo poder prosseguir com o curso.

Em caso de falha no pagamento, o **Aluno** irá receber um e-mail avisando que o pagamento falhou e um novo boleto para pagamento. Caso o **Aluno** falhe em pagar o segundo boleto enviado, a matrícula será abortada.


| Prioridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Alta | Aprovado | 1 | Felipe de Almeida
