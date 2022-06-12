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

| Priridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Alta | Aprovado | 1 | Felipe de Almeida

## RF002 - Cadastrar curso


## RF003 - Procurar curso

Um usuário anonimo ou um **aluno** poderão buscar os **cursos** existentes dentro do sistema utilizando os seguintes critérios:
- Busca por palavra chave
- Busca por categoria de curso
- Busca por data do ínicio do curso

Se nenhuma informação for providenciada na busca, a mesma deverá retornar todos os cursos disponíveis páginados.

#### Em caso de sucesso:
Exibir a lista de cursos com os critérios de busca aplicados
#### Em caso de falha:
Exibir uma notificação na tela informando que houve uma falha em buscar os cursos
| Priridade | Complexidade | Status | Versão | Autor | 
| :--- | :---: | :---: | :---: | :---: |
Alta | Baixa | Aprovado | 1 | Felipe de Almeida

## RF004
