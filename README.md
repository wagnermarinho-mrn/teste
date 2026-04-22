# CRM Arquitetos V2 (Consultores + Gerente)

Versão 2 do CRM com controle de acesso por perfil:

- **Consultor:** vê e gerencia apenas arquitetos que ele cadastrou.
- **Gerente:** visão geral completa, gestão de consultores e de toda a plataforma.

## Funcionalidades entregues

1. **Autenticação por usuário e senha** (local, para operação inicial).
2. **Perfis de acesso**:
   - `manager` (gerente)
   - `consultant` (consultor)
3. **Gestão de consultores pelo gerente**:
   - criação de novos consultores
   - desativação de consultores
4. **Governança da carteira**:
   - cada arquiteto possui campo de proprietário (`owner_consultor_id`)
   - consultor só enxerga/edita/exclui registros da própria carteira
   - gerente pode ver e administrar todos
5. **Dashboard operacional**:
   - arquitetos na carteira
   - com projeto ativo
   - próximos contatos
   - contatos em atraso
   - total de consultores (gerente)
6. **Cadastro com os campos estratégicos solicitados**:
   - número de seguidores
   - primeiro contato
   - próximo contato
   - tem projeto
7. **Busca, edição, exclusão e exportação da carteira em JSON**.

## Acesso inicial

- Usuário: `admin`
- Senha: `admin123`

## Como usar

1. Abra `index.html` no navegador.
2. Entre com o usuário gerente inicial.
3. Cadastre consultores no painel de administração.
4. Cada consultor acessa com seu login e visualiza apenas sua carteira.

## Próxima evolução recomendada (produção enterprise)

- Backend com API e banco relacional (PostgreSQL).
- Senhas com hash (Argon2/Bcrypt), JWT e refresh token.
- Controle de permissões com trilha de auditoria.
- Agenda de follow-up com notificações automáticas.
- Pipeline de vendas e relatório de conversão por consultor.
