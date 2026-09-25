---
title: "Windows Gerenciamento: Atualizar Políticas de Grupo (GPUpdate)"
date_created: 2026-08-17
tags:
  - windows/politica-usuario
  - windows/gerenciamento
---

# 👤 Windows Gerenciamento: Atualizar Políticas de Grupo (GPUpdate)

> [!info] Força a atualização imediata das GPOs de usuário e computadores locais sem necessidade de logoff ou reinicialização.

---

### 🔑 Atualizar políticas de grupo
```powershell
gpupdate /force
```

> [!info] `-Force` aplica todas as políticas sem aguardar, dispensando logoff ou reinicialização.


## 🔗 Notas Relacionadas
- [Windows: Guia Principal de Referência de Conhecimento](README.md) — Índice principal de tópicos de Windows.
- [Windows Usuários: Comandos de Gerenciamento de Contas](6_gerenciar_usuarios.md) — Comandos de terminal para gerenciamento de contas de usuários.
