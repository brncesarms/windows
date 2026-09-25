---
title: "Windows Otimização: Desativar Gerenciamento de Energia da CPU"
date_created: 2026-08-17
author: "Bruno César"
privacy: public
tags:
  - publico
  - windows/energia
  - windows/otimizacao
---

# ⚡ Windows Otimização: Desativar Gerenciamento de Energia da CPU

> [!info] Desativa políticas agressivas de suspensão e gerenciamento energético da CPU para maximizar a estabilidade operacional.

---

### ⚡ Desativar o Gerenciador de Energia
> [!warning] Execute como Administrador.
> ```powershell
> powercfg.exe /SETACVALUEINDEX SCHEME_CURRENT SUB_VIDEO VIDEOIDLE 0
> powercfg.exe /SETDCVALUEINDEX SCHEME_CURRENT SUB_VIDEO VIDEOIDLE 0
> powercfg.exe /SETACVALUEINDEX SCHEME_CURRENT SUB_SLEEP STANDBYIDLE 0
> powercfg.exe /SETDCVALUEINDEX SCHEME_CURRENT SUB_SLEEP STANDBYIDLE 0
> powercfg.exe /SETACVALUEINDEX SCHEME_CURRENT SUB_SLEEP HIBERNATEIDLE 0
> powercfg.exe /SETDCVALUEINDEX SCHEME_CURRENT SUB_SLEEP HIBERNATEIDLE 0
> ```
>
> **AC** = energia na tomada · **DC** = energia na bateria. O valor `0` desativa o tempo limite (nunca suspender/hibernar).


## 🔗 Notas Relacionadas
- [Windows: Guia Principal de Referência de Conhecimento](README.md) — Índice principal de tópicos de Windows.
- [Windows Otimização: Desativar Aplicativos em Segundo Plano](16_desativar_aplicativos_em_segundo_plano.md) — Desativação de aplicativos ocultos em background para desempenho.
