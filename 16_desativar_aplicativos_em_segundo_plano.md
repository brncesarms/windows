---
title: "Windows Otimização: Desativar Aplicativos em Segundo Plano"
date_created: 2026-08-17
tags:
  - windows/otimizacao
---

# ⚡ Windows Otimização: Desativar Aplicativos em Segundo Plano

> [!info] Otimiza o uso de processador e memória RAM desativando aplicativos que executam de forma oculta em background.

---

### 🔌 Desativar aplicativos em segundo plano
```powershell
reg add "HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\BackgroundAccessApplications" /v GlobalUserDisabled /t REG_DWORD /d 1 /f
```

> [!tip] Reverter
> Use `/d 0` para permitir que aplicativos rodem em segundo plano novamente.


## 🔗 Notas Relacionadas
- [Windows: Guia Principal de Referência de Conhecimento](README.md) — Índice principal de tópicos de Windows.
- [Windows Privacidade: Desativar Histórico de Atividades](15_desativar_historico_atividades_do_windows.md) — Desativação do histórico de atividades de privacidade do Windows.
- [Windows Otimização: Desativar Gerenciamento de Energia da CPU](3_desativar_gerenciador_de_energia.md) — Configurações de otimização de energia da CPU.
