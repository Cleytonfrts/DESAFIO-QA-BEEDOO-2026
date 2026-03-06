# Análise da aplicação

A aplicação disponibilizada no desafio consiste em um sistema simples para cadastro e gerenciamento de cursos.

Através da interface é possível cadastrar novos cursos informando os seguintes dados:

- Nome do curso
- Descrição do curso
- Instrutor
- URL da imagem de capa
- Data de início
- Data de fim
- Número de vagas
- Tipo de curso (online ou presencial)

Após o cadastro, os cursos são exibidos em uma lista em formato de cards contendo as principais informações do curso.

## Fluxos principais identificados

Durante a análise exploratória da aplicação foram identificados os seguintes fluxos principais:

### Cadastro de curso
Permite cadastrar um novo curso preenchendo os campos do formulário.

### Listagem de cursos
Exibe os cursos cadastrados na aplicação.

### Exclusão de curso
Permite remover um curso da lista através do botão "Excluir curso".

## Pontos críticos para teste

Durante a análise da aplicação foram identificados alguns pontos considerados críticos para garantir a qualidade do sistema:

- Validação de campos obrigatórios
- Validação de datas (data final não deve ser anterior à data inicial)
- Validação de valores numéricos (ex: número de vagas)
- Funcionamento correto da exclusão de cursos
- Consistência das mensagens exibidas ao usuário
- Exibição correta das informações na listagem