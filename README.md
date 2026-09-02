# QuimiPort - Sistema de Gestão de Cargas Químicas Portuárias

## Contexto do Problema

O Porto de Santos possui um papel vital no comércio exterior, movimentando um volume expressivo de cargas químicas que exigem monitoramento rigoroso, controle documental e acompanhamento técnico especializado.

Atualmente, parte desse processo ocorre de forma descentralizada ou manual, dificultando a rastreabilidade das informações, aumentando o risco operacional e tornando mais lentas as validações necessárias para garantir a segurança das operações.

Para solucionar esse cenário, foi concebido o QuimiPort, uma plataforma que centraliza o fluxo operacional e automatiza regras críticas relacionadas à movimentação de cargas químicas em ambiente portuário.

---

## Objetivo da Aplicação

O QuimiPort é uma solução Full Stack projetada para gerenciar cargas químicas portuárias.

A aplicação permitirá:

- Cadastro de produtos químicos;
- Registro de cargas químicas;
- Classificação de risco;
- Controle documental;
- Gerenciamento de inspeções;
- Gestão de armazenamento;
- Controle de bloqueios e liberações;
- Rastreabilidade operacional;
- Validação automática de regras de segurança.

---

## Entendimento do Domínio

A operação portuária exige elevado controle devido ao risco associado ao transporte, armazenamento e movimentação de substâncias químicas.

O sistema deverá apoiar diversas etapas do processo operacional, reduzindo falhas humanas e aumentando a confiabilidade das informações.

---

## Perfis de Usuários

### Operador Portuário

Responsável pelo recebimento inicial da carga e pelo registro da operação.

### Responsável Técnico

Profissional habilitado que valida aspectos técnicos e emite pareceres de segurança.

### Analista de Documentação

Responsável pela validação documental e conferência regulatória.

### Analista de Qualidade

Responsável pela execução de inspeções e validação de conformidade.

### Gestor Operacional

Responsável pelo monitoramento das operações e tomada de decisões logísticas.

### Administrador do Sistema

Responsável pelas parametrizações gerais e gestão de acessos.

---

## Processos da Operação

### 1. Triagem e Cadastro

Registro inicial da carga e associação ao produto químico.

### 2. Auditoria Documental

Validação dos documentos obrigatórios.

### 3. Inspeção Técnica

Análise física, visual e operacional da carga.

### 4. Liberação Operacional

Autorização para movimentação.

### 5. Armazenamento

Controle de ocupação das áreas de armazenagem.

---

## Decisões Automatizadas pelo Sistema

- Bloquear produtos inativos.
- Impedir cargas com documentação pendente.
- Validar responsáveis técnicos obrigatórios.
- Impedir movimentação de cargas bloqueadas.
- Impedir liberação sem inspeção aprovada.

---

## Riscos e Restrições

### Incompatibilidade Química

Produtos incompatíveis podem representar risco operacional.

### Armazenamento Incorreto

Pode causar acidentes ambientais ou operacionais.

### Vencimento Regulatório

Documentos vencidos inviabilizam a movimentação.

### Movimentação Indevida

Cargas não aprovadas não podem entrar em circulação.

---

## Estrutura da Documentação

Este repositório está organizado nos seguintes documentos técnicos:

- [`DOMINIO.md`](DOMINIO.md) → Modelagem do domínio utilizando conceitos de Domain Driven Design.
- [`CASOS_DE_USO.md`](CASOS_DE_USO.md) → Principais fluxos operacionais e comportamentos esperados do sistema.
- [`ARQUITETURA.md`](ARQUITETURA.md) → Arquitetura proposta, decisões técnicas e aplicação de TypeScript.
- [`QUALIDADE.md`](QUALIDADE.md) → Plano de qualidade, cenários de teste e roadmap de evolução.

---

## Navegação

- [Modelagem do Domínio](DOMINIO.md)
- [Casos de Uso](CASOS_DE_USO.md)
- [Arquitetura](ARQUITETURA.md)
- [Plano de Qualidade](QUALIDADE.md)

---

## Tecnologias e Conceitos Aplicados

A proposta foi construída com base nos conceitos estudados durante a Fase 1 da Pós-Tech Full Stack Development:

- Domain Driven Design (DDD)
- Clean Architecture
- JavaScript Avançado
- TypeScript
- Planejamento de Qualidade de Software
- Boas práticas de modelagem de domínio
- Arquitetura evolutiva

---

## Roadmap de Evolução

### Fase 1

- Modelagem do domínio
- Casos de uso
- Arquitetura
- Planejamento de qualidade

### Fase 2

- Desenvolvimento da API Backend utilizando Node.js

### Fase 3

- Persistência de dados utilizando PostgreSQL e Prisma ORM

### Fase 4

- Desenvolvimento da interface Web utilizando React

### Fase 5

- Desenvolvimento da aplicação Mobile utilizando React Native

### Fase 6

- Evolução para microsserviços e integrações externas

---

## Visão Geral da Solução

O QuimiPort foi concebido para servir como base de uma plataforma escalável para gestão de cargas químicas em ambiente portuário.

A solução foi modelada utilizando Domain Driven Design (DDD), organizada através de Clean Architecture e preparada para futura evolução para backend, frontend web, aplicativo mobile e microsserviços.

O objetivo desta primeira fase é estabelecer uma base sólida de negócio, arquitetura e qualidade que permitirá a evolução incremental da aplicação nas próximas etapas do projeto.