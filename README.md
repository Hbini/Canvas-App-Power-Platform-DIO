# Canvas-App-Power-Platform-DIO

## 🎯 Visão Geral do Projeto

Aplicativo Canvas com Power Platform - Projeto DIO. Criação de um aplicativo do tipo Canvas (Tela) integrado ao MS Dynamics 365 CE com funcionalidades de gestão de cursos, fluxos de automação e notificações por email.

### 📋 Descrição
Este projeto prático, oferecido pela Digital Innovation One (DIO), tem como objetivo criar um aplicativo Canvas integrado ao Microsoft Dynamics 365 Customer Engagement (CE), acessível através do aplicativo "Gestão de Cursos" a partir de um formulário já existente na entidade "Cursos".

---

## 🎓 Instrutor Especialista
**Luis Prado** - Arquiteto de Soluções na DIO
- LinkedIn: [luis-prado-b7a71427](https://www.linkedin.com/in/luis-prado-b7a71427/)

---

## 🔧 Requisitos Técnicos

### Tecnologias Utilizadas:
- **Microsoft Power Platform**: Power Apps Canvas
- **Microsoft Dynamics 365 CE**: Customer Engagement
- **Power Automate**: Fluxos de automação
- **Formulários e Entidades**: Cursos, Instrutores
- **Componentes**: Gallery, ComboBox, Headers, Detalhes

### Nível de Dificuldade:
- **Tipo**: Full-Stack
- **Nível**: Avançado

---

## 📝 Objetivos de Aprendizado

Ao concluir este projeto, você será capaz de:
1. Criar aplicativos Canvas no Power Platform
2. Integrar aplicativos com Dynamics 365 CE
3. Utilizar Model-Driven Apps com datasources dinâmicas
4. Implementar Power Automate Flows
5. Configurar notificações e workflows

---

## 🏗️ Estrutura do Projeto

### Etapa 1: Criação do Aplicativo Canvas
**Objetivo**: Criar aplicativo Model Driven com interface intuitiva

#### Requisitos:
- **Cabeçalho**: Seção de identificação visual do aplicativo
- **Campo ComboBox Cursos**: Seleção de curso com base na entidade "Cursos"
- **Galeria de Detalhes**: Componente Gallery para exibição de informações
- **Campo ComboBox Instrutores**: Seleção de instrutor da entidade "Instrutores"

#### Componentes Utilizados:
- ComboBox (Caixa de Combinação)
- Gallery (Galeria)
- Text Input
- Labels
- Buttons

### Etapa 2: Configuração do Power Automate Flow
**Objetivo**: Criar fluxos de automação para processos de negócio

#### Fluxos a Implementar:
- Fluxo de criação de registros
- Fluxo de validação de dados
- Fluxo de processamento de formulários

### Etapa 3: Notificações por Email
**Objetivo**: Implementar sistema de notificações automáticas

#### Funcionalidade:
Qui quando um novo registro de instrutor for criado, o sistema deve:
- Capturar o endereço de email do instrutor
- Enviar notificação de confirmação de cadastro
- Armazenar log de notificações

#### Dados Necessários:
- Campo Email na entidade Instrutores
- Template de email padronizado
- Configuração de destinatários

### Etapa 4: Publicação e Implantação
**Objetivo**: Disponibilizar o aplicativo no ambiente de produção

#### Atividades:
- Exportar aplicativo do Power Platform
- Postar no portal Classroom
- Incluir planilha de carga de dados (estados)
- Documentação de uso

---

## 📚 Entidades de Dados

### Entidade: Cursos
- **ID**: Identificador único
- **Nome**: Nome do curso
- **Descrição**: Detalhes do curso
- **Instrutor**: Referência para entidade Instrutores
- **Carga Horária**: Duração do curso
- **Data Início**: Data de início do curso
- **Data Fim**: Data de término do curso

### Entidade: Instrutores
- **ID**: Identificador único
- **Nome**: Nome completo do instrutor
- **Email**: Endereço de email (para notificações)
- **Telefone**: Contato telefônico
- **Especialidade**: Área de expertise
- **Data Cadastro**: Quando foi criado o registro

### Entidade: Estados
- **ID**: Identificador único
- **Sigla**: UF (SP, RJ, MG, etc.)
- **Nome**: Nome completo do estado

---

## 🔄 Fluxos de Automação (Power Automate)

### Fluxo 1: Notificação de Novo Instrutor
**Trigger**: Quando um novo registro é criado (Create)
**Ações**:
1. Obter dados do novo instrutor
2. Montar corpo do email com template HTML
3. Enviar email para o instrutor
4. Registrar log da notificação
5. Atualizar status do instrutor para "Notificado"

**Variáveis Utilizadas**:
- `Nome_Instrutor`: Nome do instrutor
- `Email_Instrutor`: Email do instrutor
- `Data_Notificacao`: Timestamp da notificação

---

## 📱 Interface do Usuário

### Layout Principal
```
┌─────────────────────────────────────┐
│      GESTÃO DE CURSOS               │ <- Header
├─────────────────────────────────────┤
│ Selecione um Curso:  [ComboBox ▼]  │
├─────────────────────────────────────┤
│ ┌──────────────────────────────────┐│
│ │ Curso 1                          ││
│ │  Instrutor: [ComboBox ▼]         ││
│ │  Carga Horária: 40h              ││
│ │  [Detalhes...]                   ││
│ ├──────────────────────────────────┤│
│ │ Curso 2                          ││
│ │  Instrutor: [ComboBox ▼]         ││
│ │  Carga Horária: 60h              ││
│ │  [Detalhes...]                   ││
│ └──────────────────────────────────┘│ <- Gallery
├─────────────────────────────────────┤
│ [Salvar]  [Limpar]  [Voltar]       │
└─────────────────────────────────────┘
```

---

## 📂 Estrutura de Arquivos

```
Canvas-App-Power-Platform-DIO/
├── README.md (este arquivo)
├── DOCUMENTACAO.md (Guia detalhado)
├── GUIA_INSTALACAO.md
├── EXEMPLO_DADOS.md
├── docs/
│   ├── arquitetura.md
│   ├── componentes.md
│   ├── fluxos.md
│   ├── entidades.md
│   └── requisitos.md
├── exemplos/
│   ├── formula_combobox.txt
│   ├── formula_gallery.txt
│   ├── template_email.html
│   └── dados_exemplo.csv
├── scripts/
│   ├── criar_entidades.ps1
│   ├── carregar_dados.ps1
│   └── configurar_fluxos.ps1
└── assets/
    ├── screenshots/
    ├── diagrama_arquitetura.png
    └── icones/
```

---

## 🚀 Como Usar Este Projeto

### Pré-requisitos
- Acesso ao Microsoft Power Platform (https://make.powerapps.com/)
- Ambiente Dynamics 365 CE configurado
- Permissões de administrador para criar aplicativos e fluxos
- Licença Power Apps ou Power Automate

### Passo 1: Preparação do Ambiente
1. Acesse o Power Platform
2. Crie um novo ambiente ou use um existente
3. Verifique se a entidade "Cursos" está disponível
4. Verifique se a entidade "Instrutores" está disponível
5. Crie a entidade "Estados" se não existir

### Passo 2: Criação do Aplicativo Canvas
1. No Power Platform, clique em "Novo App"
2. Selecione "Canvas"
3. Escolha layout vazio
4. Nomeie como "Gestão de Cursos"

### Passo 3: Adicionando Componentes
1. Adicione um Header com texto "GESTÃO DE CURSOS"
2. Insira ComboBox para Seleção de Curso
3. Adicione Gallery para exibir detalhes
4. Insira ComboBox para Seleção de Instrutor

### Passo 4: Criação de Fluxos
1. No Power Automate, crie novo fluxo
2. Configure trigger para "Quando um novo registro é criado"
3. Adicione ação de envio de email
4. Teste o fluxo

### Passo 5: Publicação
1. Publ o aplicativo no ambiente
2. Compartilhe com usuários finais
3. Exporte aplicativo para backup

---

## 💡 Fórmulas e Expressões Importantes

### ComboBox para Seleção de Curso
```excel
Primeiros([Cursos])
```

### Gallery com Detalhes
```excel
Table(Item, Instrutor, DataInicio, DataFim)
```

### Envio de Email via Power Automate
```json
{
  "subject": "Novo Instrutor Cadastrado",
  "body": "<h1>Bem-vindo!</h1><p>Um novo instrutor foi cadastrado.",
  "to": "email_instrutor"
}
```

---

## 📊 Dados de Exemplo

### Cursos
| ID | Nome | Instrutor | Carga Horária |
|---|---|---|---|
| 1 | Power Platform Avançado | Luis Prado | 40 |
| 2 | Dynamics 365 CE | Maria Silva | 60 |
| 3 | Power Automate | João Santos | 30 |

### Instrutores
| ID | Nome | Email | Especialidade |
|---|---|---|---|
| 1 | Luis Prado | luis@example.com | Power Platform |
| 2 | Maria Silva | maria@example.com | Dynamics 365 |
| 3 | João Santos | joao@example.com | Automação |

---

## ✅ Checklist de Conclusão

- [ ] Aplicativo Canvas criado
- [ ] Componentes ComboBox implementados
- [ ] Gallery configurada com dados
- [ ] Power Automate Flow criado
- [ ] Notificações por email testadas
- [ ] Dados carregados nas entidades
- [ ] Aplicativo publicado
- [ ] Documentação completada
- [ ] Projeto entregue na plataforma DIO

---

## 🔗 Links Úteis

- [Microsoft Power Platform](https://make.powerapps.com/)
- [Documentação Power Apps](https://docs.microsoft.com/power-apps/)
- [Documentação Power Automate](https://docs.microsoft.com/power-automate/)
- [Dynamics 365 CE Docs](https://docs.microsoft.com/dynamics365/customer-engagement/)
- [DIO - Digital Innovation One](https://www.dio.me/)

---

## 📝 Notas de Desenvolvimento

### Desafios Enfrentados
- Integração de datasources dinâmicas entre Canvas Apps e Dynamics 365
- Configuração de notificações de email com validação
- Performance de Gallery com grandes volumes de dados

### Soluções Implementadas
- Uso de Delegação de Consultas para otimizar queries
- Implementação de cache local para melhorar performance
- Estruturação de fluxos com tratamento de erros

---

## 👨‍💻 Autor
Desenvolvido para o Projeto Prático da DIO - Plataforma de Educação em Tecnologia

**Período**: 2024-2025
**Plataforma**: Microsoft Power Platform
**Nível de Proficiência**: Avançado

---

## 📄 Licença
Este projeto é fornecido como material de educação e treinamento da Digital Innovation One.

---

## 🤝 Contribuições
Este projeto foi criado como parte do programa educacional da DIO e segue os padrões e requisitos estabelecidos.

---

## 📞 Suporte
Para dúvidas sobre o projeto, consulte:
- Plataforma DIO: https://www.dio.me/
- Fórum da Comunidade DIO
- Documentação oficial da Microsoft Power Platform
