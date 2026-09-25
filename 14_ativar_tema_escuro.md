---
title: "Windows Personalização: Ativar Tema Escuro"
date_created: 2026-08-17
author: "Bruno César"
privacy: public
tags:
  - publico
  - windows/personalizacao
---

# 🎨 Windows Personalização: Ativar Tema Escuro

> [!info] Alteração de registro de sistema para ativação rápida do tema escuro global do Windows.

---

### 🎨 Ativar tema escuro (apps e sistema)
```powershell
reg add "HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize" /v AppsUseLightTheme /t REG_DWORD /d 0 /f
```

> [!tip] Ativar também o tema escuro do sistema
> ```powershell
> reg add "HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize" /v SystemUsesLightTheme /t REG_DWORD /d 0 /f
> ```
>
> Use `/d 1` para reverter para o tema claro.


## 🔗 Notas Relacionadas
- [Windows: Guia Principal de Referência de Conhecimento](README.md) — Índice principal de tópicos de Windows.
