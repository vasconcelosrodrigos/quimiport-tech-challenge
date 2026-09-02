# Casos de Uso do Sistema QuimiPort

## UC01 - Cadastrar Produto Químico

Ator: Administrador

Objetivo:
Cadastrar novo produto químico.

Entrada:
- Nome do produto
- Classe de risco

Saída:
- Produto cadastrado com status Ativo

Exceções:
- Nome não informado
- Classe de risco não informada

---

## UC02 - Inativar Produto Químico

Ator: Administrador

Objetivo:
Inativar produto químico.

Entrada:
- ID do produto

Saída:
- Produto marcado como Inativo

Regra:
- Produtos inativos não podem ser utilizados em novas cargas.

---

## UC03 - Registrar Carga Química

Ator: Operador Portuário

Objetivo:
Registrar nova carga.

Entradas:
- Produto
- Quantidade
- Responsável Técnico

Saída:
- Carga criada com status Pendente

Exceções:
- Produto inativo
- Quantidade inválida
- Responsável técnico não informado

---

## UC04 - Validar Documentação

Ator: Analista de Documentação

Objetivo:
Validar documentação obrigatória da carga.

Entradas:
- ID da carga
- Documentos anexados

Saída:
- Documentação aprovada ou reprovada

Exceções:
- Documento vencido
- Documento ausente
- Documento inválido

---

## UC05 - Solicitar Inspeção

Ator: Operador Portuário ou Gestor Operacional

Objetivo:
Encaminhar carga para inspeção.

Entrada:
- ID da carga

Saída:
- Status alterado para Em Inspeção

---

## UC06 - Bloquear Carga

Ator: Analista de Qualidade

Objetivo:
Bloquear carga em não conformidade.

Entradas:
- ID da carga
- Justificativa do bloqueio

Saída:
- Status alterado para Bloqueada

---

## UC07 - Liberar Carga

Ator: Responsável Técnico

Objetivo:
Liberar movimentação da carga.

Entrada:
- ID da carga

Saída:
- Status alterado para Liberada

Regras:
- Inspeção aprovada.
- Documentação válida.
- Produto associado deve permanecer ativo.

Exceções:
- Inspeção reprovada.
- Documentação pendente.
- Carga bloqueada.
- Carga cancelada.

---

## UC08 - Atualizar Status da Carga

Ator: Motor do Sistema

Objetivo:
Atualizar automaticamente o status operacional da carga.

Entradas:
- Resultado da inspeção
- Resultado documental
- Eventos operacionais

Saídas:
- Novo status registrado
- Histórico atualizado

Regras:
- Apenas transições válidas.
- Não permitir retorno de carga cancelada.
- Cargas bloqueadas devem retornar para inspeção.

Exceções:
- Status inválido.
- Dados obrigatórios ausentes.

---

## UC09 - Cancelar Carga

Ator: Gestor Operacional

Objetivo:
Cancelar operação.

Entrada:
- ID da carga

Saída:
- Status alterado para Cancelada

Regra:
- Não permitir alterações posteriores.

---

## UC10 - Consultar Cargas por Status

Ator: Operador Portuário e Gestor Operacional

Objetivo:
Consultar cargas filtradas por situação operacional.

Entrada:
- Status desejado

Saída:
- Lista de cargas correspondentes ao filtro informado

---

## UC11 - Consultar Histórico da Carga

Ator: Todos os usuários operacionais

Objetivo:
Visualizar auditoria completa da carga.

Entrada:
- ID da carga

Saída:
- Histórico completo de alterações, inspeções e movimentações realizadas