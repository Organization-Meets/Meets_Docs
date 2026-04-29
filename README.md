# 🚀 Meets

**Plataforma social centralizada para comunidades** - Conectando usuários através de eventos, interações e networking.

---

## 📋 Visão Geral

**Meets** é uma aplicação de rede social comunitária desenvolvida para centralizar a divulgação e organização de eventos, grupos de estudo e atividades sociais. A plataforma unifica um ambiente historicamente descentralizado, promovendo engajamento contínuo e fortalecendo laços comunitários.

### 💡 O Problema
A comunidade enfrentava desorganização na divulgação de atividades:
- Eventos espalhados em murais físicos, emails e grupos isolados
- Usuários, especialmente ingressantes, desconhecem iniciativas existentes
- Fragmentação da comunicação reduz engajamento e oportunidades de networking
- Ausência de canal unificado e centralizado

### ✅ A Solução
Meets oferece:
- **Canal único centralizado** para todos os eventos e atividades
- **Rede social interativa** com posts, enquetes e comentários
- **Gerenciamento de eventos** com confirmação de presença
- **Sistema de reputação** baseado em participação (pontuação)
- **Moderação comunitária** para garantir ambiente seguro

### 🏗️ Stack Tecnológico

| Camada | Tecnologia |
|--------|-------------|
| **Frontend Mobile** | Kotlin |
| **Frontend Web** | React |
| **Backend** | Java with SpringBoot (MVC) |
| **Banco de Dados** | PostgreSQL |
| **ORM** | JPA/Hibernate |
| **Hospedagem** | Cloud (AWS) |

---

## 📊 Status do Projeto - Kanban

### 🎯 To Do
- [ ] Requisitos do Mobile - Documentação completa
- [ ] Wireframe Figma - Design da interface mobile
- [ ] Scripts SQL - Implementação final no BD
- [ ] Testes de integração - Mobile + Backend

### 🔄 In Progress
- [ ] MER/DER do Banco - Diagramas finalizados
- [ ] Padrão MVC - Refatoração do projeto web
- [ ] SpringBoot - Migração do backend

### ✅ Done
- ✅ Modelagem conceitual - Completa
- ✅ Diagramas de caso de uso - Documentados
- ✅ Diagramas de sequência - Mapeados
- ✅ Diagramas de máquina de estados - Implementados
- ✅ Design no Figma - Base pronta
- ✅ Monografia - Documentação inicial

---

## 🏗️ Arquitetura

### Camadas

```
┌─────────────────────────────────────────┐
│         Apresentação (UI)               │
│  • Mobile (Kotlin)                      │
│  • Web (React)                          │
└──────────────┬──────────────────────────┘
               │
┌──────────────▼──────────────────────────┐
│         Controladores (MVC)             │
│  • SpringBoot REST API                  │
└──────────────┬──────────────────────────┘
               │
┌──────────────▼──────────────────────────┐
│         Serviços & Lógica               │
│  • Autenticação                         │
│  • Gerenciamento de eventos             │
│  • Notificações                         │
└──────────────┬──────────────────────────┘
               │
┌──────────────▼──────────────────────────┐
│         Persistência (ORM)              │
│  • JPA/Hibernate                        │
└──────────────┬──────────────────────────┘
               │
┌──────────────▼──────────────────────────┐
│         Banco de Dados                  │
│  • PostgreSQL                           │
│  • Schema MER/DER estruturado           │
└─────────────────────────────────────────┘
```

---

## 📁 Estrutura do Repositório

```
Meets_Docs/
├── README.md                              # Este arquivo
├── SCRIPT SQL/                            # Scripts de inicialização do BD
├── Diagramas/                             # Diagramas UML (ASTA)
│   ├── CasodeUso.asta
│   ├── Modelo Conceitual.asta
│   ├── modelo de dominio.asta
│   ├── Diagramas de Atividade/
│   ├── Diagramas de Máquina de Estados/
│   └── Diagramas de Sequencia/
├── Draw.io/                               # Diagramas entidade-relacionamento
│   ├── modelo_entidade_relacionamento.drawio
│   ├── modelo_relacional_ES.drawio
│   └── diagrama_entidade_relacionamento_ES.drawio
├── Tabelas/
│   ├── Casos de uso.xlsx
│   └── TabelaDeRelacionamento_FatecMeets.docx
└── Recursos/
    ├── Monografia_FATECMEETS_Colin.docx
    ├── Green Minimalist Login Page Delivery Mobile APP.pptx
    └── Figma: https://www.figma.com/design/6u1bTRKTHtNI4QE8XvkotK/

```

---

## 👥 Atores do Sistema

### 👤 Usuário (Padrão)
- Criar e editar perfil
- Visualizar feed de notícias
- Publicar posts e enquetes
- Comentar e curtir posts
- Visualizar eventos e confirmar presença
- Criar novos eventos
- Participar do sistema de pontuação (AACC)
- Denunciar conteúdo inadequado

### 🛡️ Moderador
Herda TODAS as funcionalidades do Usuário, além de:
- Analisar denúncias do sistema
- Excluir conteúdo inadequado
- Aplicar penalidades e deduzir pontuação
- Garantir ambiente seguro e produtivo

---

## 🎯 Funcionalidades Principais

### 🔐 Autenticação & Perfil
- Cadastro e login seguros
- Perfis customizáveis
- Histórico de atividades do usuário
- **[Mobile]** Login biométrico
- **[Mobile]** Autenticação offline

### 📰 Feed Social
- Timeline com posts da comunidade
- Curtidas e comentários interativos
- Enquetes comunitárias
- Compartilhamento de conteúdo
- Histórico visualizável

### 📅 Gerenciamento de Eventos
- Criar e editar eventos comunitários
- Filtrar por categoria, localização e data
- Sistema de inscrição (confirmar presença)
- Visualizar participantes
- Converter eventos em AACC (Atividades de Complementação Academica)

### 🔔 Sistema de Notificações
- Notificações em tempo real
- **[Mobile]** Push notifications nativas
- Preferências customizáveis
- Alertas de eventos e interações

### ⭐ Sistema de Reputação
- Pontuação baseada em participação
- Reconhecimento público via score
- Histórico convertível em AACC
- Penalidades por violação de regras

### 📍 Funcionalidades Mobile Exclusivas
- **Geolocalização** - Descobrir eventos próximos
- **Login Biométrico** - Autenticação rápida
- **Modo Offline** - Acesso a conteúdo em cache
- **Push Notifications** - Alertas em tempo real
- **Otimização de Bateria** - Performance eficiente

### ⚠️ Moderação & Segurança
- Sistema de denúncias comunitárias
- Verificação de conteúdo inadequado
- Penalidades progressivas
- Políticas de uso comunitário
- Restrições por idade e email válido



---

## � Requisitos do Sistema

### 🔷 Requisitos Funcionais (RF)
| ID | Descrição |
|---|---|
| RF-01 | Usuário deve poder se registrar na plataforma |
| RF-02 | Usuário deve poder fazer login com email e senha |
| RF-03 | Usuário deve poder visualizar feed de posts |
| RF-04 | Usuário deve poder curtir posts |
| RF-05 | Usuário deve poder comentar em posts |
| RF-06 | Usuário deve poder publicar enquetes |
| RF-07 | Usuário deve poder interagir com enquetes |
| RF-08 | Usuário deve poder visualizar eventos |
| RF-09 | Usuário deve poder confirmar presença em eventos |
| RF-10 | Usuário deve poder criar novos eventos |
| RF-11 | Moderador deve poder analisar denúncias |
| RF-12 | Moderador deve poder excluir conteúdo inadequado |
| RF-13 | Sistema deve calcular pontuação baseada em atividades |
| RF-14 | Sistema deve permitir converter atividades em AACC |

### ⚙️ Requisitos Não Funcionais (RNF)
| ID | Descrição |
|---|---|
| RNF-01 | Senhas devem ser criptografadas |
| RNF-02 | Interface deve ser responsiva e intuitiva |
| RNF-03 | Sistema deve responder em < 2 segundos |
| RNF-04 | Suporte para mínimo 1000 usuários simultâneos |
| RNF-05 | Disponibilidade mínima de 99.5% |
| RNF-06 | Logs de auditoria para todas as ações |
| RNF-07 | Backup automático diário |

### 🔑 Requisitos Funcionais Mobile (RF-M)
| ID | Descrição |
|---|---|
| RF-M-01 | Aplicativo deve suportar login biométrico |
| RF-M-02 | Implementar notificações push nativas |
| RF-M-03 | Geolocalização para descobrir eventos próximos |
| RF-M-04 | Modo offline com cache de conteúdo |
| RF-M-05 | Sincronização automática ao reconectar |

### 📱 Requisitos Não Funcionais Mobile (RNF-M)
| ID | Descrição |
|---|---|
| RNF-M-01 | Autenticação biométrica com latência < 500ms |
| RNF-M-02 | Consumo de bateria otimizado |
| RNF-M-03 | Compatibilidade com Android 8.0+ |
| RNF-M-04 | Precisão de geolocalização ≥ 50m |
| RNF-M-05 | Tamanho do aplicativo < 100MB |

### 📏 Regras de Negócio (RN)
| ID | Descrição |
|---|---|
| RN-01 | Usuários devem ter email válido para cadastro |
| RN-02 | Módulo de restrição de idade deve ser respeitado |
| RN-03 | Ex-usuários não podem efetuar o registro novamente |
| RN-04 | Dados pessoais sensíveis não podem ser exibidos publicamente |
| RN-05 | Sistema de pontuação deve ser transparente e auditável |
| RN-06 | Conteúdo denunciado deve ser analisado em 24h |
| RN-07 | Penalidades aplicadas devem ser reversíveis mediante análise |

---

## � Fluxo Geral do Sistema

O sistema funciona em ciclos contínuos de interação:

```
[Cadastro e Autenticação]
         ↓
[Usuário Autenticado]
    ↙      ↓      ↘
[Posts] [Eventos] [Enquetes]
    ↖     ↓      ↙
[Gera Log de Atividades]
         ↓
[Calcula Pontuação]
         ↓
[Exibe no Perfil]
         ↓
[Moderador Analisa Qualidade]
         ├→ [Denúncias Recebidas]
         ├→ [Aprova/Remove Conteúdo]
         └→ [Aplica Penalidades]
```

### Ciclo Principal:
1. **Autenticação**: Cadastro e login obrigatórios
2. **Exploração**: Navegação por áreas sociais e comunitárias
3. **Interação**: Postagens, enquetes, eventos geram registros
4. **Pontuação**: Log convertido em reconhecimento de participação
5. **Moderação**: Moderadores atuam sobre denúncias

---

## �📊 Diagramas UML & Modelagem

### 📍 Diagrama de Casos de Uso
Representa os atores (Usuário, Moderador) e suas interações com o sistema, como login, visualizar feed, criar eventos, e moderar conteúdo.

**Arquivo**: [Diagramas/CasodeUso.asta](Diagramas/CasodeUso.asta)

**Casos de Uso Mapeados**:
- UC01: Realizar Login
- UC02: Visualizar Feed
- UC03: Curtir Post
- UC04: Comentar Post
- UC05: Publicar Enquete
- UC06: Interagir com Enquete
- UC07: Denunciar Post
- UC08: Analisar Denúncias
- UC09: Definir Penalidade do Usuário
- UC10: Manter Usuário (CRUD)
- UC11: Visualizar Eventos
- UC12: Confirmar Presença
- UC13: Criar Evento
- UC14: Converter Atividade em AACC
- UC15: Analisar Histórico de Atividades

### 🏛️ Modelo Conceitual
Mostra as entidades abstratas do sistema e seus relacionamentos sem detalhes técnicos.

**Arquivo**: [Diagramas/Modelo Conceitual.asta](Diagramas/Modelo%20Conceitual.asta)

### 🎯 Modelo de Domínio
Descreve os conceitos principais do negócio (Usuário, Evento, Post, Comentário) e suas relações.

**Arquivo**: [Diagramas/modelo de dominio.asta](Diagramas/modelo%20de%20dominio.asta)

### 📈 Diagrama de Sequência
Mostra a ordem temporal das interações durante casos de uso críticos como login e criação de eventos.

**Arquivos**:
- [Manter Usuário](Diagramas/Diagramas%20de%20Sequencia/Manter%20Usuário%20–%20Diagrama%20de%20Sequência%201.asta)
- [Criar Evento](Diagramas/Diagramas%20de%20Sequencia/Criar%20Evento%20-%20Diagrama%20de%20Sequência%202.asta)

### 🔄 Diagrama de Máquina de Estados
Representa os diferentes estados pelos quais objetos (usuários, eventos) passam e suas transições.

**Arquivos**:
- [Manter Usuário - Estados](Diagramas/Diagramas%20de%20Máquina%20de%20Estados/Manter%20Usuário%20-%20Diagrama%20de%20Máquina%20de%20Estados%201.asta)
- [Criar Evento - Estados](Diagramas/Diagramas%20de%20Máquina%20de%20Estados/Criar%20Evento%20-%20Diagrama%20de%20Máquina%20de%20Estados%202.asta)

### 📊 Diagrama de Atividades
Descreve fluxos de trabalho e processos de negócio, como cadastro e criação de eventos.

**Arquivos**:
- [Manter Usuário - Atividades](Diagramas/Diagramas%20de%20Atividade/Manter%20Usuário%20-%20Diagrama%20de%20Atividade%201.asta)
- [Criar Evento - Atividades](Diagramas/Diagramas%20de%20Atividade/Criar%20Evento%20-%20Diagrama%20de%20Atividade%202.asta)

### 🗄️ Diagrama Entidade-Relacionamento (DER)
Modelo relacional que mostra como os dados estão organizados no banco de dados.

**Arquivos**:
- [modelo_entidade_relacionamento.drawio](Draw.io/modelo_entidade_relacionamento.drawio)
- [diagrama_entidade_relacionamento_ES.drawio](Draw.io/diagrama_entidade_relacionamento_ES.drawio)
- [modelo_relacional_ES.drawio](Draw.io/modelo_relacional_ES.drawio)

---

---

## 🔗 Links Importantes

### 🎨 Prototipagem
📌 **[Figma - Design do Projeto](https://www.figma.com/design/6u1bTRKTHtNI4QE8XvkotK/FatecMeets?m=auto&t=OgnCGWqrZdyfnBEg-1)**

Wireframes, protótipos interativos e componentes de UI para mobile e web.

### 📚 Documentação
- 📄 Monografia completa (Meets_Generic_Version.docx)
- 📊 Especificação de requisitos
- 🎯 Casos de uso detalhados
- 📋 Tabelas de relacionamento de dados

---

## 📈 Próximos Passos - Roadmap

1. ✏️ **Finalizar requisitos funcionais** do app mobile
2. 🎨 **Publicar wireframes finais** do Figma como referência
3. 🗄️ **Implementar scripts SQL** e criar banco de dados
4. 🔧 **Configurar ambientes** de desenvolvimento e produção
5. 🚀 **Iniciar sprints** de desenvolvimento das funcionalidades core
6. 📱 **Implementar autenticação** (login biométrico mobile)
7. 🔐 **Sistema de segurança** e criptografia
8. 🧪 **Testes de integração** entre plataformas

---

## 👥 Autores

- **Matheus Marinho** - matheus.marinho2@fatec.sp.gov.br
- **Nicolas Carvalho** - nicolas.carvalho5@fatec.sp.gov.br
- **Gabriel Rodrigues** - gabriel.rodrigues106@fatec.sp.gov.br
- **Luiz Oliveira** - luiz.oliveira176@fatec.sp.gov.br
- **Matheus Ferrari** - matheus.ferrari3@fatec.sp.gov.br

**Instituição**: Faculdade de Tecnologia de Ferraz de Vasconcelos  
**Curso**: Tecnólogo em Análise e Desenvolvimento de Sistemas

---

## 📞 Informações do Projeto

- **Status**: 🔄 Em Desenvolvimento
- **Versão**: 0.1.0-alpha
- **Última atualização**: Abril 2026
- **Repositório**: GitHub - Organization-Meets/Meets_Docs

---

**Meets** - Conectando pessoas através de eventos | [Voltar ao topo](#-meets)
