# Guia de Instalação - Canvas App Power Platform DIO

## 🚀 Início Rápido

### Pré-requisitos
- Acesso ao Microsoft Power Platform (https://make.powerapps.com/)
- Ambiente Dynamics 365 CE criado
- Permissões de administrador
- Licença Power Apps Premium

### Instalação do Ambiente

#### Passo 1: Acessar Power Platform
1. Acesse https://make.powerapps.com/
2. Selecione o ambiente desejado
3. Clique em "+ Novo App"
4. Escolha "Canvas" como tipo de aplicativo

#### Passo 2: Criar Entidades
1. Vá para "Soluções"
2. Crie uma nova solução chamada "Gestão de Cursos"
3. Adicione as entidades:
   - Cursos
   - Instrutores
   - Estados

#### Passo 3: Importar Dados
1. Prepare um arquivo CSV com os dados
2. Use a funcionalidade "Importar" no Power Platform
3. Mapeie os campos corretamente

#### Passo 4: Criar o Aplicativo Canvas
1. Nova App > Canvas
2. Selecione "Tablet" como layout
3. Nomeie como "Gestão de Cursos"
4. Comece a projetar a interface

### Estrutura de Componentes

```
Tela Principal
├── Header (Título)
├── ComboBox_Cursos
├── Gallery_Cursos
│  └── ComboBox_Instrutores
├── Botões (Salvar, Cancelar, Limpar)
└── Rodapé
```

### Configuração de Fluxos Power Automate

1. Crie novo fluxo de nuvem
2. Configure o trigger: "Quando um novo registro é criado"
3. Adicione ação de envio de email
4. Configure o remetente e destinatário
5. Teste o fluxo

### Teste Funcional

Antes de publicar, verifique:
- [ ] Todos os ComboBox carregam dados corretamente
- [ ] Gallery exibe registros
- [ ] Emails são enviados com sucesso
- [ ] Não há erros de delegação

### Publicação

1. Clique em "Publicar"
2. Selecione os usuários que terão acesso
3. Configure permissões
4. Finalize a publicação

### Troubleshooting

**Problema**: ComboBox não carrega dados
**Solução**: Verifique a fórmula de origem de dados

**Problema**: Erro de delegação
**Solução**: Use funções delegadas ou limpe os dados

**Problema**: Email não é enviado
**Solução**: Verifique configurações SMTP e permissões

---

**Versão**: 1.0
**Data**: Janeiro 2025
