# 📚 Sincronizando para GitLab

## Instruções para Sincronizar o Projeto Canvas-App-Power-Platform-DIO no GitLab

Este documento fornece instruções passo-a-passo para sincronizar este projeto do GitHub para o GitLab.

---

## ✅ Pré-requisitos

- [x] Conta GitLab ativa (https://gitlab.com)
- [x] Git instalado localmente
- [x] Acesso ao repositório GitHub
- [x] Token de acesso pessoal ou SSH configurado no GitLab

---

## 🚀 Método 1: Clone e Push (Recomendado)

### Passo 1: Clonar o repositório do GitHub

```bash
git clone https://github.com/Hbini/Canvas-App-Power-Platform-DIO.git
cd Canvas-App-Power-Platform-DIO
```

### Passo 2: Criar novo repositório no GitLab

1. Acesse https://gitlab.com/projects/new
2. Preencha os detalhes:
   - **Project name**: Canvas-App-Power-Platform-DIO
   - **Visibility**: Public
   - **Initialize repository with a README**: Não (deixe vazio)
3. Clique em "Create project"

### Passo 3: Adicionar GitLab como novo remote

```bash
git remote add gitlab https://gitlab.com/SEU_USUARIO/Canvas-App-Power-Platform-DIO.git
```

*Substitua `SEU_USUARIO` pelo seu nome de usuário do GitLab*

### Passo 4: Fazer push para GitLab

```bash
git push -u gitlab main
```

---

## 🔄 Método 2: Mirror Repository (Sincronização Automática)

### Passo 1: Criar repositório vazio no GitLab

1. Acesse https://gitlab.com/projects/new
2. Crie um novo projeto com o mesmo nome
3. **NÃO** inicialize com README

### Passo 2: Sincronizar usando mirror

```bash
git clone --mirror https://github.com/Hbini/Canvas-App-Power-Platform-DIO.git
cd Canvas-App-Power-Platform-DIO.git
git push --mirror https://gitlab.com/SEU_USUARIO/Canvas-App-Power-Platform-DIO.git
cd ..
rm -rf Canvas-App-Power-Platform-DIO.git
```

---

## 📋 Conteúdo Sincronizado

Os seguintes arquivos e pastas serão sincronizados:

```
Canvas-App-Power-Platform-DIO/
├── README.md (Documentação completa)
├── INSTALL.md (Guia de instalação)
├── GITLAB-SYNC.md (Este arquivo)
├── .gitignore (Configurações Power Platform)
└── exemplos/
    └── power-apps-formulas-otimizadas.md
```

---

## 🔐 Autenticação via Token (Se necessário)

### Gerar Token no GitLab

1. Acesse https://gitlab.com/-/user_settings/personal_access_tokens
2. Clique em "Add new token"
3. Configure:
   - **Token name**: Canvas-App-Platform-Token
   - **Scopes**: `api`, `read_repository`, `write_repository`
   - **Expires at**: Escolha uma data futura
4. Clique em "Create personal access token"
5. Copie o token (não será mostrado novamente!)

### Usar Token na URL

```bash
git remote add gitlab https://oauth2:SEU_TOKEN@gitlab.com/SEU_USUARIO/Canvas-App-Power-Platform-DIO.git
```

---

## 🔑 Configurar SSH (Alternativa)

### Gerar Chave SSH

```bash
ssh-keygen -t ed25519 -C "seu_email@example.com"
```

### Adicionar Chave Pública no GitLab

1. Copie o conteúdo de `~/.ssh/id_ed25519.pub`
2. Acesse https://gitlab.com/-/user_settings/ssh_keys
3. Cole a chave e salve

### Usar SSH na URL

```bash
git remote add gitlab git@gitlab.com:SEU_USUARIO/Canvas-App-Power-Platform-DIO.git
```

---

## ✨ Verificar Sincronização

Acesse seu repositório no GitLab:
https://gitlab.com/SEU_USUARIO/Canvas-App-Power-Platform-DIO

Verifique se todos os arquivos foram sincronizados:

- ✅ README.md
- ✅ INSTALL.md
- ✅ GITLAB-SYNC.md
- ✅ .gitignore
- ✅ exemplos/ (pasta com power-apps-formulas-otimizadas.md)

---

## 📝 Atualizar GitLab com Novos Commits

Depois de fazer novos commits no GitHub, sincronize com GitLab:

```bash
git fetch origin
git push gitlab
```

---

## 🆘 Troubleshooting

### Erro: "fatal: remote gitlab already exists"

```bash
git remote remove gitlab
git remote add gitlab https://gitlab.com/SEU_USUARIO/Canvas-App-Power-Platform-DIO.git
```

### Erro: "Permission denied (publickey)"

Verifique se sua chave SSH está adicionada corretamente no GitLab.

### Erro: "403 Forbidden"

Verifique se seu token ou credenciais estão corretas.

---

## 📞 Suporte

Para dúvidas sobre sincronização Git:
- [Git Documentation](https://git-scm.com/doc)
- [GitLab Documentation](https://docs.gitlab.com/)
- [GitHub to GitLab](https://docs.gitlab.com/ee/user/project/import/github.html)

---

**Data de Atualização**: 18 de Janeiro de 2026
**Status**: Projeto sincronizado e pronto para uso
