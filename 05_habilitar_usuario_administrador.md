---
title: "Windows Usuários: Habilitar Conta Interna de Administrador"
date_created: 2026-08-17
author: "Bruno César"
privacy: public
tags:
  - publico
  - windows/usuarios
  - windows/seguranca
---

# 👤 Windows Usuários: Habilitar Conta Interna de Administrador

> [!info] Ativa a conta interna e oculta de Administrador do Windows e define uma senha forte de acesso via console.

---

### 🔑 Habilitar usuário administrador
```powershell
Enable-LocalUser -Name "Administrador"
```

### 🔑 Definir senha do administrador
> [!warning] Escolha uma senha forte e exclusiva.
> ```powershell
> Set-LocalUser -Name "Administrador" -Password (ConvertTo-SecureString -String "TROQUE_POR_UMA_SENHA_FORTE" -AsPlainText -Force)
> ```


## 🔗 Notas Relacionadas
- [Windows: Guia Principal de Referência de Conhecimento](README.md) — Índice principal de tópicos de Windows.
- [Windows Usuários: Comandos de Gerenciamento de Contas](06_gerenciar_usuarios.md) — Comandos de terminal para criação, edição e exclusão de contas.
