---
title: "Windows Usuários: Comandos de Gerenciamento de Contas"
date_created: 2026-08-17
author: "Bruno César / Antigravity"
privacy: public
tags:
  - publico
  - windows/usuarios
  - windows/gerenciamento
---

# 👤 Windows Usuários: Comandos de Gerenciamento de Contas

> [!info] Guia de comandos net user e net localgroup para criar, excluir e incluir contas de usuários no grupo de administradores.

---

### 🔑 Remover usuário do grupo de administradores
> [!info] Define o usuário "user" como padrão, removendo-o dos administradores.
> ```powershell
> net localgroup administrators user /delete
> net localgroup users user /add
> ```

### 🔑 Configurar senha do usuário (não expira e não alterável pelo usuário)
```powershell
wmic useraccount where "name='user'" set passwordexpires=false
net user user /passwordchg:no
```


## 🔗 Notas Relacionadas
- [Windows: Guia Principal de Referência de Conhecimento](README.md) — Índice principal de tópicos de Windows.
- [Windows Usuários: Habilitar Conta Interna de Administrador](05_habilitar_usuario_administrador.md) — Habilitação da conta integrada oculta de Administrador.
- [Windows Usuários: Exibir Nome do Computador e Contas](02_exibir_nome_computador_e_usuarios.md) — Exibição rápida do nome de computador e contas locais de usuários.
