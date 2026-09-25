---
title: "Windows Privacidade: Desativar Histórico de Atividades"
date_created: 2026-08-17
tags:
  - windows/privacidade
  - windows/seguranca
---

# 🕵️ Windows Privacidade: Desativar Histórico de Atividades

> [!info] Desativa a coleta automática do histórico de atividades de aplicativos e navegação pelo Windows.

---

### 🕵️ Desativar o histórico de atividades do Windows
```powershell
reg add "HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Advanced" /v Start_TrackDocs /t REG_DWORD /d 0 /f
```

> [!tip] Reverter
> Use `/d 1` para reativar o rastreamento de atividades.


## 🔗 Notas Relacionadas
- [Windows: Guia Principal de Referência de Conhecimento](README.md) — Índice principal de tópicos de Windows.
- [Windows Otimização: Desativar Aplicativos em Segundo Plano](16_desativar_aplicativos_em_segundo_plano.md) — Desativação de aplicativos rodando em segundo plano.
