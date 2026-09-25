---
title: "Windows Manutenção: Ferramentas SFC e DISM"
date_created: 2026-08-17
author: "Bruno César"
privacy: public
tags:
  - publico
  - windows/manutencao
  - windows/otimizacao
---

# 🛠️ Windows Manutenção: Ferramentas SFC e DISM

> [!info] Comandos de diagnóstico e reparo de imagens e arquivos corrompidos de sistema do Windows com SFC e DISM.

---

### 🛠️ SFC - Verificar integridade dos arquivos de sistema
```powershell
sfc /scannow
```

### 🛠️ DISM - Reparar imagem do Windows
```powershell
DISM /Online /Cleanup-Image /RestoreHealth
```

> [!tip] Alternativa via PowerShell
> ```powershell
> Repair-WindowsImage -Online -StartComponentCleanup -RestoreHealth
> ```

> [!info] Ordem recomendada
> Rode primeiro o **SFC**. Se ele apontar corrupção que não consegue reparar, execute o **DISM** em seguida e rode o SFC novamente.


## 🔗 Notas Relacionadas
- [Windows: Guia Principal de Referência de Conhecimento](README.md) — Índice principal de tópicos de Windows.
- [Windows Manutenção: Comando CHKDSK](08_chkdsk.md) — Diagnóstico e reparo físico de discos com a ferramenta CHKDSK.
- [Windows Manutenção: Desfragmentação e Otimização](09_desfragmentar.md) — Otimização e desfragmentação manual de unidades de armazenamento.
