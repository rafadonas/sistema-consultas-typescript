# Sistema de Gerenciamento de Consultas Médicas

Um sistema TypeScript completo para gerenciar consultas médicas, médicos, pacientes e especialidades de forma segura e tipada.

## 📋 Visão Geral

O **Sistema de Gerenciamento de Consultas Médicas** é uma aplicação desenvolvida em TypeScript que oferece uma solução robusta para o gerenciamento de consultas em clínicas e centros médicos. O sistema implementa tipos e interfaces bem definidas para garantir segurança de tipos e facilitar a manutenção do código.

## 👨‍💻 Autor

**Rafael do Nascimento Silva**  
RM: 566263

## 🎯 Funcionalidades Principais

### Gerenciamento de Pacientes
- Cadastro de pacientes com dados pessoais (nome, CPF, email, telefone)
- Validação de dados obrigatórios e opcionais
- Estrutura tipo para armazenar informações de pacientes

### Gerenciamento de Médicos
- Cadastro de médicos com informações profissionais (nome, CRM, especialidade)
- Status de atividade (ativo/inativo)
- Associação com especialidades médicas

### Especialidades Médicas
- Catálogo de especialidades (Cardiologia, Ortopedia, Pediatria, etc.)
- Descrição opcional para cada especialidade
- Fácil expansão para novos tipos de especialidades

### Gerenciamento de Consultas
- Criação de consultas com médico, paciente, data e valor
- Controle de status da consulta (agendada, confirmada, cancelada, realizada)
- Confirmação e cancelamento de consultas
- Observações opcionais para cada consulta
- Formatação de exibição com valores monetários em BRL

## 🛠️ Arquitetura

### Tipos de Dados (Types)

**Especialidade**: Define as especialidades médicas disponíveis, com ID, nome e descrição opcional.

**Paciente**: Armazena informações do paciente como ID, nome, CPF, email e telefone opcional.

**StatusConsulta**: Enumeração de estados possíveis de uma consulta (agendada, confirmada, cancelada, realizada).

### Interfaces

**Medico**: Interface que representa um profissional de saúde com ID, nome, CRM, especialidade e status de atividade.

**Consulta**: Interface principal que une médico e paciente, incluindo data, valor, status e observações opcionais.

**UsuarioAdmin**: Interface para administradores do sistema com diferentes níveis de acesso (total, operacional, financeiro).

## 📁 Estrutura do Projeto

```
sistema-consultas-typescript/
├── src/
│   ├── index.ts              # Arquivo principal com exemplo de uso
│   ├── interfaces/           # Interfaces TypeScript
│   │   ├── consulta.ts      # Interface de Consulta
│   │   ├── medico.ts        # Interface de Médico
│   │   └── usuarioAdmin.ts  # Interface de Usuário Admin
│   └── types/               # Tipos TypeScript
│       ├── especialidade.ts # Tipo de Especialidade
│       ├── paciente.ts      # Tipo de Paciente
│       └── statusConsulta.ts # Tipo de Status de Consulta
├── dist/                     # Saída compilada (gerada automaticamente)
├── tsconfig.json            # Configuração do TypeScript
└── README.md                # Este arquivo
```

## ⚙️ Configuração TypeScript

O projeto utiliza as seguintes configurações de compilação:

- **Target**: ES6
- **Mode Strict**: Ativado (garante tipagem rigorosa)
- **Output Directory**: `./dist`
- **Root Directory**: `./src`

## 🔧 Operações Principais

**Criar Consulta**: Função que cria uma nova consulta associando um médico e um paciente com data e valor definidos.

**Confirmar Consulta**: Altera o status da consulta para confirmada, garantindo a reserva da agenda do profissional.

**Cancelar Consulta**: Cancela uma consulta existente, com validação para impedir cancelamento de consultas já realizadas.

**Exibir Consulta**: Formata as informações da consulta para exibição em formato legível, com valores monetários em BRL.

## 📊 Exemplo de Execução

Ao executar o arquivo `index.ts`, você verá uma saída formatada com os detalhes da consulta criada, mostrando informações do médico, paciente, especialidade, data e valor em reais.

## 🔐 Características de Segurança

- ✅ **Tipagem Rigorosa**: Todas as operações são type-safe
- ✅ **Validação de Tipos**: Prevenção de erros em tempo de compilação
- ✅ **Imutabilidade**: Uso de spread operator para criar novos objetos
- ✅ **Interfaces Bem Definidas**: Contrato claro entre componentes

## 📝 Notas de Desenvolvimento

- Todos os valores monetários devem ser inseridos em reais (BRL)
- Datas devem ser do tipo `Date` do JavaScript
- Status de consulta são literais e predefinidos
- CRM é necessário para identificar médicos
- CPF é necessário para identificar pacientes

## 🚀 Próximas Melhorias

- Implementar persistência em banco de dados
- Adicionar validações mais rigorosas (CPF, CRM, email)
- Criar API REST para acesso remoto
- Implementar autenticação e autorização
- Adicionar testes unitários e de integração
- Implementar filtros e buscas avançadas

## 📄 Licença

Este projeto foi desenvolvido para fins educacionais.

---

**Desenvolvido com ❤️ em TypeScript**
