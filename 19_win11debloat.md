---
title: "Windows 11: Script de Desbloat Win11Debloat"
date_created: 2026-09-04
author: "Bruno César"
privacy: public
tags:
  - publico
  - windows/debloat
---

# 🧹 Windows 11: Script de Desbloat Win11Debloat

> [!info] Remoção de bloatware, desativação de telemetria e limpeza de apps pré-instalados no Windows 10/11 usando o script open-source **Win11Debloat** (Raphire).

---

## 🏆 Por que usar o Win11Debloat

| Característica | Detalhe |
|---------------|---------|
| ⭐ Popularidade | ~56k estrelas no GitHub |
| 🗓️ Manutenção | Atualização recente (2026.08) |
| 📜 Linguagem | PowerShell (Windows 10/11) |
| ⚖️ Licença | MIT (livre) |
| 🔄 Reversível | ✅ Pode desfazer tudo |
| 🏷️ Simples | Sem instalação, roda direto |

### 🎯 O que ele faz

| Categoria | Função |
|-----------|--------|
| 🗑️ Remove bloatware | Candy Crush, Xbox, OneDrive, apps desnecessários |
| 📡 Desativa telemetria | Diagnóstico, rastreamento, anúncios direcionados |
| 🤖 Mata IA | Desativa **Copilot**, remove Windows Recall |
| 🎨 Limpa a UI | Menu de contexto antigo, widgets, taskbar, busca Bing |
| 🏢 Bloat OEM | HP, Dell, Lenovo, ASUS, Acer, MSI, Razer |
| 🎮 Jogos | Xbox Game Bar, gravação de tela |

## 🚀 Como executar

> ⚠️ **Importante:** requer **Windows PowerShell 5.1** (o `powershell.exe`, não o PowerShell 7/`pwsh`) — senão a remoção de apps falha silenciosamente.

```powershell
# ✨ Método rápido (PowerShell como admin)
& ([scriptblock]::Create((irm "https://debloat.raphi.re/")))

# 📦 Ou método tradicional (baixar o ZIP do GitHub e extrair)
Set-ExecutionPolicy Bypass -Scope Process -Force
.\Win11Debloat.ps1
```

## ⚙️ Exemplos com flags

```powershell
# 🏃 Modo CLI (sem interface gráfica)
.\Win11Debloat.ps1 -CLI -RemoveApps -DisableTelemetry

# 🔇 Silencioso (sem prompts)
.\Win11Debloat.ps1 -Silent -RunDefaults

# 💾 Cria ponto de restauração antes de aplicar
.\Win11Debloat.ps1 -CreateRestorePoint -RemoveApps

# 🎮 Remove apenas apps de jogos
.\Win11Debloat.ps1 -RemoveGamingApps
```

> ℹ️ O script fica salvo em [`scripts/windows/Win11Debloat.ps1`](../../guia-ia-local/scripts/windows/Win11Debloat.ps1) para uso offline.

## 🥈 Alternativa enterprise: SysAdminDoc/Debloat-Win11

| Característica | Detalhe |
|---------------|---------|
| ✅ Suporte | Win11 24H2/25H2/26H1 (Recall, Copilot, Teams, Phone Link) |
| 🧪 DryRun | Testa sem aplicar |
| ↩️ Undo | Manifest JSON de desfazer |
| 🛟 Restore | Ponto de restauração automático |
| 🖥️ Detecção | Hardware (laptop/desktop, SSD/HDD) |

## 🔗 Notas Relacionadas
- [Windows: Guia Principal de Referência de Conhecimento](README.md) — Índice principal de tópicos de Windows.
- [Windows Software: Gerenciador de Pacotes WinGet](17_winget.md) — Instalação e atualização em lote de softwares.
- 💻 [T.I. — Mapa de Conteúdo](README.md) — Índice geral de todas as áreas.

---

## 🔗 Fontes
- [Raphire/Win11Debloat (GitHub)](https://github.com/Raphire/Win11Debloat)
- [Site oficial debloat.raphi.re](https://debloat.raphi.re/)
- [SysAdminDoc/Debloat-Win11 (GitHub)](https://github.com/SysAdminDoc/Debloat-Win11)
