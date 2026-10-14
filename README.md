# Testes de API - Hub de Leitura (Catálogo de Livros)

Collection do Postman com testes da funcionalidade Catálogo de Livros
da API Hub de Leitura (EBAC-QE/hub-de-leitura-api).

## Como executar
1. Suba a API local (`npm install` e `npm start`).
2. No Postman, importe os dois arquivos .json deste repositório.
3. Selecione o environment "Hub Local".
4. Execute a collection com o Collection Runner.

## Cenários cobertos
**Positivos**
- Login de admin e de usuário comum
- Listar livros (GET)
- Cadastrar livro (POST)
- Consultar livro por ID (GET)
- Atualizar livro (PUT)
- Excluir livro (DELETE)

**Negativos**
- Cadastrar sem token: 401 (MISSING_TOKEN)
- Cadastrar com usuário comum: 403 (ADMIN_REQUIRED)
- Consultar livro excluído: 404

## Validações
Status HTTP, tempo de resposta, formato JSON, campos do corpo
e regras de negócio (permissão de admin e estoque inicial).
