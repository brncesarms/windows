---
title: "Windows PowerShell: Habilitar Execução de Scripts"
date_created: 2026-08-17
author: "Bruno César"
privacy: public
tags:
  - publico
  - windows/powershell
  - windows/scripts
---

# 💻 Windows PowerShell: Habilitar Execução de Scripts

> [!info] Configuração da ExecutionPolicy no PowerShell para permitir a execução de scripts e utilitários administrativos locais.

---

> [!warning] Sobre `Unrestricted`
> `Unrestricted` desativa praticamente todas as proteções. Prefira opções menos permissivas, como `RemoteSigned`, que permite scripts locais e exige assinatura apenas para scripts baixados da internet.

### 🔌 Habilitar execução de scripts locais (recomendado)
```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```

### ⚙️ Opção menos restritiva (apenas quando necessário)
```powershell
Set-ExecutionPolicy Unrestricted -Scope CurrentUser
```

### 🔍 Verificar política atual
```powershell
Get-ExecutionPolicy -List
```


## 🔗 Notas Relacionadas
- [Windows: Guia Principal de Referência de Conhecimento](README.md) — Índice principal de tópicos de Windows.
- [Windows Privacidade: Desativar Histórico de Atividades](15_desativar_historico_atividades_do_windows.md) — Desativação de logs e histórico de atividades do Windows.
