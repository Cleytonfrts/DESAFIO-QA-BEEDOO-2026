## BUG 01 — Sistema permite cadastrar curso sem nome

**Descrição**

O sistema permite cadastrar um curso mesmo quando o campo "Nome do curso" não é preenchido.

**Passos para reproduzir**

1. Acessar a página "Cadastrar curso"
2. Deixar o campo "Nome do curso" vazio
3. Preencher os demais campos
4. Clicar em "Cadastrar curso"

**Resultado atual**

O sistema cadastra o curso normalmente e o exibe na lista.

**Resultado esperado**

O sistema deveria impedir o cadastro e exibir uma mensagem de validação informando que o campo "Nome do curso" é obrigatório.

**Severidade**

Média

**Evidência**

print_02_cadastro_sem_nome.png

## BUG 02 — Sistema permite cadastro com data final menor que data inicial

**Descrição**

O sistema permite cadastrar cursos mesmo quando a data final é anterior à data de início.

**Passos para reproduzir**

1. Acessar a tela "Cadastrar curso"
2. Preencher os campos normalmente
3. Informar data de início posterior à data final
4. Clicar em "Cadastrar curso"

**Resultado atual**

O curso é cadastrado normalmente e exibido na lista com datas inconsistentes.

**Resultado esperado**

O sistema deveria impedir o cadastro e exibir mensagem informando que a data final deve ser posterior à data inicial.

**Severidade**

Média

**Evidência**

print_03_datas_invalidas.png

## BUG 03 — Campo "Número de vagas" permite valores negativos

**Descrição**

O campo "Número de vagas" permite valores negativos ao utilizar as setas de incremento/decremento.

**Passos para reproduzir**

1. Acessar a tela "Cadastrar curso"
2. No campo "Número de vagas", utilizar a seta para diminuir o valor
3. Continuar diminuindo até o valor ficar negativo

**Resultado atual**

O sistema permite valores negativos (ex: -1, -2).

**Resultado esperado**

O campo deveria limitar o valor mínimo em 0 ou 1.

**Severidade**

Baixa

**Impacto**

Pode gerar inconsistência de dados e confusão para o usuário.

**Evidência**

print_04_vagas_negativas.png

## BUG 04 — Curso não é removido após clicar em "Excluir curso"

**Descrição**

Ao clicar no botão "Excluir curso", o sistema exibe a mensagem "Curso excluído com sucesso", porém o curso continua visível na lista.

**Passos para reproduzir**

1. Acessar a página "Lista de cursos"
2. Clicar no botão "Excluir curso" em qualquer curso listado
3. Observar a lista após a mensagem de sucesso

**Resultado atual**

O sistema exibe a mensagem de sucesso, porém o curso não é removido da lista.

**Resultado esperado**

O curso deveria ser removido da lista após a exclusão.

**Severidade**

Alta

**Impacto**

Usuários acreditam que o curso foi removido, porém ele permanece no sistema.

**Evidência**

print_05_exclusao_falha.png