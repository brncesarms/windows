---
title: "Windows Manutenção: Desfragmentação e Otimização"
date_created: 2026-08-17
author: "Bruno César"
privacy: public
tags:
  - publico
  - windows/manutencao
  - windows/otimizacao
---

# 🛠️ Windows Manutenção: Desfragmentação e Otimização

> [!info] Execução manual da otimização e desfragmentação de partições e unidades de disco via utilitário de console do Windows.

---

### 🛠️ Desfragmentar HD
```powershell
defrag C: /v
```

> [!tip] Alternativa via PowerShell
> ```powershell
> Optimize-Volume -DriveLetter C -Defrag -TierOptimize -Verbose
> ```

### ⚡ Otimizar SSD (Trim)
> [!info] Em SSDs use `ReTrim` em vez de desfragmentar, para não desgastar a unidade sem ganho.
> ```powershell
> Optimize-Volume -DriveLetter C -ReTrim -Verbose
> ```


## 🔗 Notas Relacionadas
- [Windows: Guia Principal de Referência de Conhecimento](README.md) — Índice principal de tópicos de Windows.
- [Windows Manutenção: Ferramentas SFC e DISM](10_sfc_dism.md) — Diagnóstico e reparo lógico de arquivos de sistema corrompidos.
- [Windows Manutenção: Comando CHKDSK](08_chkdsk.md) — Inspeção e correção de integridade física de discos com CHKDSK.
