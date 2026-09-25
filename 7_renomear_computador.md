---
title: "Windows Gerenciamento: Renomear Computador"
date_created: 2026-08-17
tags:
  - windows/gerenciamento
---

# 👤 Windows Gerenciamento: Renomear Computador

> [!info] Instruções e comando sconfig ou PowerShell para renomear e alterar o hostname local do computador.

---

### 👤 Renomear computador
> [!info] A reinicialização automática é opcional — remova `-Restart` se preferir reiniciar manualmente.
```powershell
Write-Host "Renomeando computador..."
$RENAME = Read-Host "Digite o novo nome do computador"
Rename-Computer -NewName $RENAME -Restart
```

### ⚙️ Alternativa via sconfig
```powershell
sconfig
```
> No menu do `sconfig`, escolha a opção **"Renomear este computador"**.


## 🔗 Notas Relacionadas
- [Windows: Guia Principal de Referência de Conhecimento](README.md) — Índice principal de tópicos de Windows.
- [Windows Usuários: Exibir Nome do Computador e Contas](2_exibir_nome_computador_e_usuarios.md) — Exibição do nome do computador e contas ativas locais.
