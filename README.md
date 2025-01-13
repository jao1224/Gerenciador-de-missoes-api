API de Gerenciamento de Missões

Visão Geral

A API de Gerenciamento de Missões foi desenvolvida para facilitar a administração de missões, oferecendo funcionalidades completas para criar, atualizar, excluir e buscar informações. Esta documentação apresenta os endpoints disponíveis e seus respectivos propósitos.

Endpoints

1. Criar Missão

Rota: /create

Método HTTP: POST

Descrição: Permite criar uma nova missão no sistema.

Exemplo de Requisição:

{
    "titulo": "Missão Espacial",
    "descricao": "Explorar a superfície de Marte",
    "dataInicio": "2025-01-15",
    "dataFim": "2025-02-15",
    "status": "pendente"
}

2. Atualizar Missão

Rota: /update

Método HTTP: PUT

Descrição: Atualiza as informações de uma missão existente no sistema.

Exemplo de Requisição:

{
    "id": 123,
    "titulo": "Missão Espacial Atualizada",
    "descricao": "Exploração detalhada da superfície de Marte",
    "status": "em andamento"
}

3. Deletar Missão

Rota: /delete

Método HTTP: DELETE

Descrição: Remove uma missão do sistema.

Exemplo de Requisição:

{
    "id": 123
}

4. Pesquisar Missões

4.1 Pesquisa por ID

Rota: /id

Método HTTP: GET

Descrição: Busca uma missão específica através do seu identificador único.

Parâmetros de URL:

id (obrigatório): O identificador único da missão.

Exemplo de Requisição:

GET /id?id=123

4.2 Pesquisa por Intervalo de Data

Rota: /date

Método HTTP: GET

Descrição: Busca missões que estejam dentro de um intervalo de datas.

Parâmetros de URL:

dataInicio (obrigatório): Data inicial do intervalo.

dataFim (opcional): Data final do intervalo.

Exemplo de Requisição:

GET /date?dataInicio=2025-01-01&dataFim=2025-12-31

5. Mostrar Todo o Banco de Missões

Rota: /all

Método HTTP: GET

Descrição: Retorna todas as missões cadastradas no banco de dados.

Exemplo de Requisição:

GET /all

Observações Gerais

Autenticação: Para garantir a segurança, todos os endpoints exigem autenticação via token JWT.

Formato de Respostas: Todas as respostas são fornecidas em JSON.

Códigos de Status:

200: Sucesso.

400: Requisição inválida.

401: Não autorizado.

404: Recurso não encontrado.

500: Erro interno do servidor.
