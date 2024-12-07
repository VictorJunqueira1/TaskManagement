### *Requisitos Funcionais*

- [ ] O sistema deve permitir que o usuário realize login com e-mail e senha.
- [ ] O sistema deve emitir um token JWT após a autenticação bem-sucedida.
- [ ] O sistema deve permitir que o usuário crie novas tarefas com título, descrição, data de vencimento e prioridade.
- [ ] O sistema deve listar todas as tarefas do usuário autenticado.
- [ ] O sistema deve permitir a edição de tarefas já existentes.
- [ ] O sistema deve permitir a exclusão de tarefas.
- [ ] O sistema deve permitir alterar o status de uma tarefa entre "pendente" e "concluída".
- [ ] O sistema deve permitir que o usuário filtre tarefas por:
    - [ ] Data de vencimento.
    - [ ] Prioridade.
    - [ ] Status (pendente/concluída).
- [ ] O sistema deve enviar respostas de erro detalhadas para requisições inválidas.

----------

### *Requisitos Não Funcionais*

- [ ] O sistema deve ser implementado utilizando o framework *ASP.NET Core 9*.
- [ ] O sistema deve armazenar dados em um banco de dados *MySQL*.
- [ ] O sistema deve garantir a segurança das senhas utilizando hashing (ex.: *BCrypt*).
- [ ] O sistema deve utilizar autenticação baseada em *JWT*.
- [ ] A API deve seguir os padrões RESTful, com endpoints claros e bem definidos.
- [ ] O sistema deve ter documentação básica dos endpoints utilizando *Swagger*.
- [ ] O tempo de resposta das requisições à API deve ser menor que 500ms em condições normais.
- [ ] A aplicação deve estar configurada para deploy na *Render* com HTTPS.
- [ ] O código deve seguir boas práticas de Clean Code e princípios SOLID.

----------

### *Regras de Negócio*

- [ ] Apenas usuários autenticados podem acessar e manipular dados de tarefas.
- [ ] Cada tarefa deve estar associada a um único usuário (relacionamento um para muitos).
- [ ] Um usuário não pode acessar tarefas de outro usuário.
- [ ] Tarefas devem ser criadas com status inicial "pendente".
- [ ] O título das tarefas deve ter no máximo 100 caracteres.
- [ ] A data de vencimento de uma tarefa não pode ser anterior à data atual.
- [ ] O sistema deve rejeitar qualquer alteração ou criação de tarefas com dados inválidos.
- [ ] O token JWT deve expirar após 24 horas de emissão.